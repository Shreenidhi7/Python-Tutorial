
- In this section, we shall continue understanding for loops
- Specifically in this section, we will look at some functionalities like how find minimum number, maximum number and sum/total of the numbers or integers present in the list.


1. Finding the total 
- Using Traditional Way
```
scores = [2, 45, 102, 4, 9, 12, 45, 90, 1, 0, 1]  
print(f"Length of the list - {len(scores)}")  
  
# Finding Total -> Traditional Way  
# total = 0  
# for score in scores:  
#     total = total + score  
# print(f"Total runs scored {total}")

Output Response -
Length of the list - 11
Total runs scored 311
```

- Using Sum Function
```
scores = [2, 45, 102, 4, 9, 12, 45, 90, 1, 0, 1]  
print(f"Length of the list - {len(scores)}")  
  
# Finding Total -> Using Sum  
total = sum(scores)  
print(f"Total - {total}")

Output Response -
Length of the list - 11
Total - 311
```


---
---

2. Highest Score
- Using Traditional Way
```
scores = [2, 45, 102, 4, 9, 12, 45, 90, 1, 0, 1]  
print(f"Length of the list - {len(scores)}")

# Finding Highest  
highest = scores[0]  
for score in scores:  
    if highest < score:  
        highest = score  
print(f"Highest score - {highest}")

Output Response -
Length of the list - 11
Highest score - 102
```

- Using Max function
```
scores = [2, 45, 102, 4, 9, 12, 45, 90, 1, 0, 1]  
print(f"Length of the list - {len(scores)}")
  
highest = max(scores)  
print(f"Highest value - {highest}")

Output Response -
Length of the list - 11
Highest value - 102
```

---
---

3. Lowest/Minimum
- Using Traditional Way
```
scores = [2, 45, 102, 4, 9, 12, 45, 90, 1, 0, 1]  
print(f"Length of the list - {len(scores)}")

lowest = scores[0]  
for score in scores:  
    if score < lowest:  
        lowest = score  
print(f"The lowest score is {lowest}")

Output Response -
Length of the list - 11
The lowest score is 0
```

- Using Min Function
```
scores = [2, 45, 102, 4, 9, 12, 45, 90, 1, 0, 1]  
print(f"Length of the list - {len(scores)}")

lowest = min(scores)  
print(f"Lowest value - {lowest}")

Output Response -
Length of the list - 11
Lowest value - 0
```


---
---
