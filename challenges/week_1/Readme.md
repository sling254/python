# Bus Fare Challenge - Week 1

## Challenge

Write a program that does the following:

1. gets today's date and stores it in a variable `'date'`
2. uses today's date to get the name on the day of the week written in short form with the first letter capitalized eg. `'Fri'` if today were Friday and assigns it a variable `'day'`
3. uses if statements to determine the today's fare following these bus fare schedule:

   - monday - friday --> 100
   - saturday --> 60
   - sunday --> 80
4. Prints the results in this format  
    >Date:    2021-01-05  
    >Day:     Tue  
    >Fare:    100  

## Evaluation

Run the [Checker](checker.py) file to evaluate your code. If all tests pass, your code will be the correct solution. If any fail, check the error messages and make changes to your code and repeat.

## Note

1. Your solution must be written in the [bus_fare_challenge](bus_fare_challenge.py) file and its name should never be changed.  
2. Your program must make use of the following variable names:
   - `'date'`
   - `'day'`
   - `'fare'`  
*Failure to which all your tests will fail.*  
3. The **Checker** file should **never** be **altered** at any cost.


from datetime import datetime, timedelta, date

#Get todays date and store it in a variable 'date'

date = datetime.now()


"""
# Use todays date to get the name on the day of the week written in a short 
# form with the first letter capitalized (e.g) 'Fri' if today were Friday and 
# assigns it a variable 'day'
"""
day = datetime.date(date).strftime('%a')


"""
Uses if Statement to determine the todays fare following these bus fare shedule:
    Monday - Friday --> 100
    Saturdat --> 60
    Sunday --> 80

Prints the results in this exact formart
    Date: 2021-01-05
    Day:Tue
    Fare:100

"""
if day == "Mon" or day == "Tue" or day == "Wen" or day =="Thu" or day == "Fri":
    fare = 100
   
elif day == "Sat":
    fare = 60
    
else: 
    fare = 80
    

print("Date:", date.date())
print("Day:" + day)
print("Fare:", fare)
