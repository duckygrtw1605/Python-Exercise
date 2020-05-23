# Python-Exercise
exercises 2 on runstoneacademy

# Many people keep time using a 24 hour clock (11 is 11am and 23 is 11pm, 0 is midnight). 
# If it is currently 13 and you set your alarm to go off in 50 hours, it will be 15 (3pm). 
# Write a Python program to solve the general version of the above problem. 

def alarm():
# Ask the user for the time now (in hours)
    x = int(input("What time is it: ")) # 24 hour clock
    if x > 24 or x < 0:
        print("Wrong input - Please try again") 
        #how to ask users to re-input values until values are correct?
    
# Then ask for the number of hours to wait for the alarm. 
    if x >= 0 and x <= 24:
        y = int(input("Set your alarm to go off in: ")) 
# Your program should output what the time will be on the clock when the alarm goes off.
        time_on_the_clock = x + y
        time_of_the_day = time_on_the_clock % 24 

# Condition:
        return("It is now: " + str(time_of_the_day))
        
alarm()

# It is possible to name the days 0 through 6 where day 0 is Sunday and day 6 is Saturday. 
# If you go on a wonderful holiday leaving on day number 3 (a Wednesday) and you return home after 10 nights you would return home on a Saturday (day 6) 
# Write a general version of the program 

def days_of_the_week():
# The starting day number:
    x = int(input("Your starting day:")) #From 0 to 6 

# Conditions:
    if x > 6 or x < 0:
        print("Wrong input, please try again")
        #how to ask users to re-input values until values are correct?
    if x >= 0 and x <= 6:
        y = int(input("Length of your stay:")) #length of your stay
        z = x + y #Final Day

# Conversion:
        if (z % 7) == 0:
            return("Sun")
        if (z % 7) == 1:
            return("Mon")
        if (z % 7) == 2:
            return("Tue")
        if (z % 7) == 3:
            return("Wed")
        if (z % 7) == 4:
            return("Thu")
        if (z % 7) == 5:
            return("Fri")
        if (z % 7) == 6:
            return("Sat")

days_of_the_week()
