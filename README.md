# octanet_june01
ATM interface

The ATMs in our cities are built on Python, as we have all seen them. It is a console-based application with five
different classes. In order to use the system, the user must enter his or her user ID and pin when it starts. 
Once the details are entered successfully, ATM functionality is unlocked. As a result of the project, 
the following operations can be performed:

Transactions History
Withdraw
Deposit
Transfer
Quit


===========================================================================================================================
SOURCE CODE:
===========================================================================================================================
import time
print("please insert your card")
time.sleep(5)
pin=8979
balance=9000
choice=0
password=int(input("Enter your pin:"))

if pin==password:
    while choice!=4:
        print("""   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit""")
        choice=int(input("Please enter your choice:"))
    
        if choice==1:
            withdraw=int(input("Enter withdrawal amount:"))
            if balance<withdraw:
                print("insufficient balance")
            else:
                balance-=withdraw
                print(f"leftout amount is {balance}")
        elif choice==2:
            deposit=int(input("Enter the deposit amount:"))
            balance+=deposit
            print(f"deposited amount is {balance}")
        elif choice==3:
            recipient_name=input("enter the recipient name")
            recipient_acc_no=int(input("enter the recipient_acc_no:"))
            transfer=int(input(" Enter the amount you want to tansfer:"))
            if balance<transfer:
                print("insufficient balance")
            else:
                balance-=transfer
                print(f" An amount of {transfer} is transferred to {recipient_name}\n")
                print(f" your current blance is {balance}")
        elif choice ==4:
            print("QUIT")
else:
    print("Wrong pin Try Again")    

=================================================================================================================================
OUTPUT:
===================================================================================================================================
please insert your card
Enter your pin:8979
   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit
Please enter your choice:1
Enter withdrawal amount:5000
leftout amount is 4000
   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit
Please enter your choice:1
Enter withdrawal amount:5000
insufficient balance
   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit
Please enter your choice:2
Enter the deposit amount:4000
deposited amount is 8000
   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit
Please enter your choice:3
enter the recipient namekhishore
enter the recipient_acc_no:4569
 Enter the amount you want to tansfer:8000
 An amount of 8000 is transferred to khishore

 your current blance is 0
   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit
Please enter your choice:3
enter the recipient namekhishore
enter the recipient_acc_no:5469
 Enter the amount you want to tansfer:6900
insufficient balance
   1==Withdraw 
                  2==Deposit
                  3==Transfer
                  4==Quit
Please enter your choice:4
QUIT


