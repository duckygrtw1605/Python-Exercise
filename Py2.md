# Python-Exercise
exercises 2 on runstoneacademy

# Many people keep time using a 24 hour clock (11 is 11am and 23 is 11pm, 0 is midnight). 
# If it is currently 13 and you set your alarm to go off in 50 hours, it will be 15 (3pm). 
# Write a Python program to solve the general version of the above problem. 

def alarm():
   while True:
       x = int(input("What time is it: ")) # 24 hour clock
       if x >= 0 and x <= 24:
           break
   y = int(input("Set your alarm to go off in: ")) 
# Your program should output what the time will be on the clock when the alarm goes off.
   time_on_the_clock = x + y
   time_of_the_day = time_on_the_clock % 24 

   return("It is now: " + str(time_of_the_day))  
alarm()
 

# It is possible to name the days 0 through 6 where day 0 is Sunday and day 6 is Saturday. 
# If you go on a wonderful holiday leaving on day number 3 (a Wednesday) and you return home after 10 nights you would return home on a Saturday (day 6) 
# Write a general version of the program 

def days_of_the_week():
   while True:
       x = int(input("Your starting day:")) #From 0 to 6 
       if x >= 0 and x <= 24:
           break
   y = int(input("Length of your stay:")) #length of your stay
   z = x + y

# Conversion:
   list_day = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]
   modulo = z%7 # Range from 0 to 6 
   result = list_day[modulo] 
    
   return result

days_of_the_week()
