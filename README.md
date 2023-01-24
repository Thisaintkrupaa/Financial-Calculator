import math 

#we have printed the following statements which allows user to understand they have to choose from the following options provided and what each calculations type are. 

print("choose either 'investment' or 'bond' from the menu below to proceed: ")
print("investment - to calculate the amount of interest you'll earn on your investment ")
print("bond - to calculate the amount youll have to pay on a home loan")

calculator_type = input(" Enter option from investment or bond: ") #we are asking user to enter option they would like to proceed with from the following options
calculator_type = calculator_type.lower() 


while (calculator_type != "investment" and calculator_type!= "bond" ): #if user does not type an option from the following options 
    print("Sorry you have not chosen the correct options please enter option again from the above ") #it will ask the user to re enter the calculation type
    calculator_type = input(" Enter option from investment or bond: ")
    calculator_type = calculator_type.lower()

if(calculator_type=="investment"): #if user has chosen the investment option they will be asked to enter answers to the following details
    amount=int(input("Enter amount: ")) #int is an integer type which allows users to enter whole numbers
    rate=float(input("Enter rate of interest: ")) #float type allows user to enter in decimals
    rate=rate/100.0
    time=int(input("Enter no of years: "))
    interest=input("Enter interest option from simple interest or compound interest: ")
    interest=interest.lower()
    while (interest != "simple" and interest!= "compound" ): #if user does not type an option from the following options 
        calculator_type = input("Sorry you have not chosen the correct options please enter option again from simple interest or compound interest: ") #it will ask the user to re enter the option
        interest=interest.lower()
    
    #The math.pow()method returns the value of x raised to power y.
    
    a=0
    if(interest=="simple"):
        a=amount*(1+rate*time)
    else:
        a=amount*(math.pow((1+rate),time)) 
    print(a)
else:
    p=int(input("Enter present value of house: "))
    i=float(input("Enter interest rate: "))
    i=i/12
    n=int(input("Enter no of months you plan to repay the bond: "))
    x=(i*p)/(1-(pow(1+i,-n)))
    print(x)

#* used for multiplication 
#+ addition 
#- subtraction 
#The pow() function returns the value of x to the power of y (xy).


