
- If we try to run loop on a dictionary and we are trying to change the same dictionary. -> That will not work in python
	- It will give a runtime error.
- Same with lists -> if we run a loop on lists and trying to change the same list, that also will give runtime error 
- Instead
	- Rather than running the loop on the dictionary that we want to change, it better to run it on a another data type
		- In our case, we had list and we have to think through that logic 

```
"""  
Problem Statement -  
We have the following dictionary containing details:  
user = {  
    "user_name" : "my_user",    "password" : "test@123",    "email": "my_user@example.com",    "address": "ABC road, 11111",    "country": "Australia"}  
  
Delete the sensitive information from the dictionary present in a list  
Delete password and address keys from the dictionary  
sensitive_info = ["password", "address"]  
"""  
  
user = {  
    "user_name" : "my_user",  
    "password" : "test@123",  
    "email": "my_user@example.com",  
    "address": "ABC road, 11111",  
    "country": "Australia"  
}  
sensitive_info = ["password", "address"]  
  
for i in sensitive_info:  
    print(f"{i} : {user[i]}")  
    user.pop(i)  
print(user)

Output Response -
password : test@123
address : ABC road, 11111
{'user_name': 'my_user', 'email': 'my_user@example.com', 'country': 'Australia'}
```

---
---

What if a key which is not present in the dictionary, what will happen?
- We are trying to "phone" which is not present in the list.
	- What happens if we use a pop function which is not present in the list.
Answer
- It will give an error -> Key Error
- It encounter it, we could have an condition to check if the key is present in the list, if yes we will delete, else print a message saying key is not present in the list

```
user = {  
    "user_name" : "my_user",  
    "password" : "test@123",  
    "email": "my_user@example.com",  
    "address": "ABC road, 11111",  
    "country": "Australia"  
}  
sensitive_info = ["password", "address", "phone"]  
  
for i in sensitive_info:  
    if i in user:  
        print(f"{i} present in the list \n So Deleting the Key and value from the dictionary => {i} and {user[i]}.")  
        user.pop(i)  
    else:  
        print(f"{i} not present in the list")  
  
print(user)

Output Response -
password present in the list 
 So Deleting the Key and value from the dictionary => password and test@123.
address present in the list 
 So Deleting the Key and value from the dictionary => address and ABC road, 11111.
phone not present in the list
{'user_name': 'my_user', 'email': 'my_user@example.com', 'country': 'Australia'}
```

----
---

