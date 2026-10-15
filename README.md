import math

print("1 is addition")
print("2 is subtraction")
print("3 is multiplication")
print("4 is division")
num1 = int(input("Enter the first digit: "))
num2 = int(input("Enter the second digit: "))
op_usage = int(input("Enter the operation of choice: "))

def add_num(num1,num2):
    return num1 + num2
    
def sub_num(num1,num2):
    return num1 - num2
    
def mul_num(num1,num2):
    return num1 * num2
    
def div_num(num1,num2):
        if num2 == 0:
            return("Cannot divide by 0, invalid, change the number or operation!")
        else:
            return num1/num2
            
def ans_prob(op_usage,num1,num2):
    if 1<=op_usage<=4:
        if op_usage == 1:
            return add_num(num1,num2)
        elif op_usage == 2:
            return sub_num(num1,num2)
        elif op_usage == 3:
            return mul_num(num1,num2)
        else:
            return div_num(num1,num2)
    else:
        return("Invalid number choice! Choose a new one for valid operation!")

final_res = ans_prob(op_usage,num1,num2)

if isinstance(final_res,(int,float)):
    print(f"The final answer between those two numbers with your operation is {final_res:.2f}")
else:
    print(final_res)
