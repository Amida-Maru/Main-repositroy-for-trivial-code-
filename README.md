import time
time1 = 5
counter = 3
flag = True


print("""
|^^^^^^^^^^^^^^^^^^^^^^^^^^^^|
|  Welcome to Cisco router!  |                      
| Use the default credentials|                         
|         to log in!         |
**--------------------------**
""")
while flag == True: #main loop

    if True: #always True to start conditional statements
        login = input("Enter your login: ")
        haslo = input("Enter your password: ")
        if login != "admin": # meets condition if different that admin
           print("User", login, "does not exist, try another login")

        elif haslo != "admin": #meets condition jezeli roznce od admin
           warning = input("Wrong password,you have 3 attempts left before we suspend your account, ENTER: ")

           while counter >= 1:
            haslo = input("Please re-enter your password now: ")
            if haslo != "admin":
             counter -= 1
             print("Wrong password, only ", counter, "attempts left")
            if counter == 0:
             print("The number of attempts has been exceeded, now your account will be suspended for",time1, "seconds")
             time.sleep(time1)
             time1 += 5
             print("\n\n\n\n\n\n\n\nThe program will restart now")
             counter = 3
            if haslo == "admin":
             print("Welcome to the system", "Mr", login)
             flag = False # Can I avoid using flag here and use break or continue
             break

        else:
            print("Welcome to the system", "Mr",login)
            break
