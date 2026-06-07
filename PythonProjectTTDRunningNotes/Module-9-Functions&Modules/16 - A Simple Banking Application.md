
- In this section, we will utilize the concepts that we have learned with funcitons and create a simple banking application
	- We will take user input to
		- To show balance in an account
		- To withdraw money from the account
		- To deposit money into the account
	- We will create function for the above 3 actions that we are going to perform
	- Take User Input and define these functions with some logic inside it.

```
balance_amount = 0  
kyc_documents = {} # empty dictionary  
  
def check_balance():  
    print("Checking your balance....")  
    print(f"Your current balance is {balance_amount}")  
    print(f"=========================")  
  
def deposit_money(deposit_amount):  
    global balance_amount  
    print("Depositing an amount")  
    print(f"Your current balance is {balance_amount}")  
    if deposit_amount > 0:  
        balance_amount = balance_amount + deposit_amount  
        print(f"Your newly deposited amount is {deposit_amount}")  
        print(f"Your total balance after depositing amount {deposit_amount} is {balance_amount}")  
        print(f"=========================")  
    else:  
        print("Cannot deposit an negative amount or zero amount")  
        print(f"=========================")  
  
def withdraw_money(withdraw_amount):  
    global balance_amount  
  
    if withdraw_amount > 0:  
        if balance_amount > 0 and withdraw_amount <= balance_amount:  
            print("withdrawing money from your account")  
            print(f"Your current balance is {balance_amount}")  
            print(f"Withdrawing money from your account is {withdraw_amount}")  
            balance_amount = balance_amount - withdraw_amount  
            print(f"Your total balance after withdrawing amount {withdraw_amount} is {balance_amount}")  
            print(f"=========================")  
        else:  
            print(f"Your current balance is {balance_amount}")  
            if balance_amount > 0 and withdraw_amount >= balance_amount:  
                print("Withdraw amount is more than balance amount, so its not possible to withdraw money")  
                print(f"=========================")  
            print("Cannot withdraw money from your account since its a zero balance")  
            print(f"=========================")  
    else:  
        print("Cannot withdraw zero or negative amount from the account")  
        print(f"=========================")  
  
def check_kyc():  
    if len(kyc_documents) == 0:  
        print("KYC not done yet")  
        print(f"=========================")  
    else:  
        for doc in kyc_documents:  
            print(f" {doc} : {kyc_documents[doc]}")  
            print(f"=========================")  
  
  
def update_kyc(docs):  
    global kyc_documents  
    kyc_documents.update(docs)  
  
if __name__ == "__main__":  
    print(f"=========================")  
    print("Welcome to the Banking App")  
    print(f"=========================")  
    while True:  
        print(f"1. Check your balance")  
        print(f"2. Deposit an amount")  
        print(f"3. Withdraw money")  
        print(f'4. Check KYC documents')  
        print(f"5. Update KYC documents")  
        print(f"6. Exit/Quit")  
        choice = input(f"Enter your choice number (1-6) :- ")  
        print(f"=========================")  
  
        if choice == "1":  
            check_balance()  
        elif choice == "2":  
            deposit_amount = float(input("Enter the amount you want to deposit into your account: "))  
            deposit_money(deposit_amount)  
        elif choice == "3":  
            withdrawal_amount = float(input("Enter the amount you want to withdraw from your account: "))  
            withdraw_money(withdrawal_amount)  
        elif choice == "4":  
            check_kyc()  
        elif choice == "5":  
            kyc_docs = {}  
            no_of_documents = int(input("Enter the number of documents you want to add: "))  
            for i in range(no_of_documents):  
                key = input("Enter the document type : ")  
                value = input("Enter the document value/number : ")  
                kyc_docs[key] = value  
            update_kyc(kyc_docs)  
            print(f"KYC documents added to your account: {kyc_docs}")  
            print(f"=========================")  
        elif choice == "6":  
            break  
        else:  
            print("Invalid Input/Choice!! Please Retry")  
            print(f"=========================")  
  
    print()  
    print(f"Thank you for banking with us!!")
```

---
---
