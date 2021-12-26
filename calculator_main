def add(n1, n2):
    return n1 + n2

def subtract(n1, n2):
    return n1 - n2

def multiply(n1, n2):
    return n1 * n2

def divide(n1, n2):
    return n1 / n2

operations = { # assign the function to its relative operation
    "+": add,
    "-": subtract,
    "*": multiply,
    "/": divide
}

def calculator():
    print('''
     __________
    | ________ |
    ||12345678||
    |""""""""""|
    |[M|#|C][-]|
    |[7|8|9][+]|
    |[4|5|6][x]|
    |[1|2|3][%]|
    |[.|O|:][=]|
    "----------"
    ''')

    num1 = float(input("What is the first number? "))
    op = input("+\n-\n*\n/\nPick an operation: ")
    num2 = float(input("What is your second number? "))

    calculation = operations[op] #pass the returned function to a variable to use it as a function
    answer = calculation(num1, num2)

    print(f"{num1} {op} {num2} = {answer}")

    another_calc = input(f"Type 'Y' to continue calculating with {answer} | ANYTHING ELSE to exit: ").lower()

    while another_calc == 'y': # perform another calcalation with the answer
        old_answer = answer
        
        op = input("Pick an operation: ")
        num3 = float(input("What's the next number? "))

        calculation = operations[op]
        answer = calculation(old_answer, num3)

        print(f"{old_answer} {op} {num3} = {answer}")
        
        another_calc = input(f"Type 'Y' to continue calculating with {answer} | ANYTHING ELSE to exit: ").lower()

    if input("Would you like to perform a NEW calculation? Type 'Y' for YES | ANYTHING ELSE for NO: ").lower() == 'y':
        calculator()

calculator()
