import tkinter as tk

def calculate():
    try:
        expression = entry.get()
        result = eval(expression)
        result_label.config(text="Result: " + str(result))
    except Exception as e:
        result_label.config(text="Error")

# Create a new window
window = tk.Tk()
window.title("Calculator")

# Create an entry field for user input
entry = tk.Entry(window, width=30)
entry.grid(row=0, column=0, columnspan=4)

# Create buttons for numbers and operators
buttons = [
    '7', '8', '9', '/',
    '4', '5', '6', '*',
    '1', '2', '3', '-',
    '0', '.', '=', '+'
]

row, col = 1, 0
for button_text in buttons:
    if button_text == '=':
        tk.Button(window, text=button_text, padx=20, pady=20, command=calculate).grid(row=row, column=col)
    else:
        tk.Button(window, text=button_text, padx=20, pady=20, command=lambda text=button_text: entry.insert(tk.END, text)).grid(row=row, column=col)
    col += 1
    if col > 3:
        col = 0
        row += 1

# Create a label to display the result
result_label = tk.Label(window, text="", padx=20, pady=20)
result_label.grid(row=row, column=0, columnspan=4)

# Run the application
window.mainloop()
