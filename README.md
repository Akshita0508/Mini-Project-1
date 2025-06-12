# Mini-Project-1
Python Assignment
# Initial list
L = [11, 12, 13, 14]

# (i) Add 50 and 60 to L
L.append(50)
L.append(60)
print("After adding 50 and 60:", L)

# (ii) Remove 11 and 13 from L
L.remove(11)
L.remove(13)
print("After removing 11 and 13:", L)

# (iii) Sort L in ascending order
L.sort()
print("Ascending order:", L)

# (iv) Sort L in descending order
L.sort(reverse=True)
print("Descending order:", L)

# (v) Search for 13 in L
if 13 in L:
    print("13 is present in L")
else:
    print("13 is not present in L")

# (vi) Count number of elements in L
print("Number of elements in L:", len(L))

# (vii) Sum all elements in L
print("Sum of all elements:", sum(L))

# (viii) Sum all ODD numbers in L
odd_sum = sum(x for x in L if x % 2 != 0)
print("Sum of odd numbers:", odd_sum)

# (ix) Sum all EVEN numbers in L
even_sum = sum(x for x in L if x % 2 == 0)
print("Sum of even numbers:", even_sum)

# (x) Sum all PRIME numbers in L
def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True

prime_sum = sum(x for x in L if is_prime(x))
print("Sum of prime numbers:", prime_sum)

# (xi) Clear all the elements in L
L.clear()
print("After clearing L:", L)

# (xii) Delete L
del L
# print(L)  # This will give an error if you uncomment, since L no longer exists

# Initial dictionary
D = {1: 5.6, 2: 7.8, 3: 6.6, 4: 8.7, 5: 7.7}

# (i) Add new entry: key=8 and value=8.8
D[8] = 8.8
print("After adding key 8:", D)

# (ii) Remove key=2
D.pop(2)
print("After removing key 2:", D)

# (iii) Check whether key=6 is present in D
if 6 in D:
    print("Key 6 is present in D")
else:
    print("Key 6 is not present in D")

# (iv) Count the number of elements present in D
print("Number of elements in D:", len(D))

# (v) Add all the values present in D
value_sum = sum(D.values())
print("Sum of all values:", value_sum)

# (vi) Update the value of key=3 to 7.1
D[3] = 7.1
print("After updating key 3 to 7.1:", D)

# (vii) Clear the dictionary
D.clear()
print("After clearing D:", D)

# Initial sets
S1 = set([10, 20, 30, 40, 50, 60])
S2 = set([40, 50, 60, 70, 80, 90])

# (i) Add 55 and 66 in Set S1
S1.add(55)
S1.add(66)
print("S1 after adding 55 and 66:", S1)

# (ii) Remove 10 and 30 from Set S1
S1.discard(10)
S1.discard(30)
print("S1 after removing 10 and 30:", S1)

# (iii) Check whether 40 is present in S1
print("Is 40 in S1?", 40 in S1)

# (iv) Union of S1 and S2
print("Union:", S1.union(S2))

# (v) Intersection of S1 and S2
print("Intersection:", S1.intersection(S2))

# (vi) S1 - S2
print("S1 - S2:", S1.difference(S2))

import random
import string

# (i) 100 random strings of length 6 to 8
print("Random Strings:")
for _ in range(100):
    length = random.randint(6, 8)
    random_str = ''.join(random.choices(string.ascii_letters, k=length))
    print(random_str)

# (ii) Prime numbers between 600 and 800
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True

primes = [x for x in range(600, 801) if is_prime(x)]
print("Prime numbers between 600 and 800:", primes)

# (iii) Numbers between 100 and 1000 divisible by 7 and 9
divisible = [x for x in range(100, 1001) if x % 7 == 0 and x % 9 == 0]
print("Numbers divisible by 7 and 9:", divisible)

# (i) Two random lists
list1 = [random.randint(10, 30) for _ in range(10)]
list2 = [random.randint(10, 30) for _ in range(10)]

print("List 1:", list1)
print("List 2:", list2)

# (i) Common numbers
common = list(set(list1) & set(list2))
print("Common numbers:", common)

# (ii) Unique numbers in both lists
unique = list(set(list1) ^ set(list2))
print("Unique numbers:", unique)

# (iii) Minimum in both lists
print("Min in List 1:", min(list1))
print("Min in List 2:", min(list2))

# (iv) Maximum in both lists
print("Max in List 1:", max(list1))
print("Max in List 2:", max(list2))

# (v) Sum of both lists
print("Sum of List 1:", sum(list1))
print("Sum of List 2:", sum(list2))

import random

# Generate list
L = [random.randint(100, 900) for _ in range(100)]
print("Random List:", L)

# (i) All odd numbers
odd_numbers = [x for x in L if x % 2 != 0]
print("Odd Numbers:", odd_numbers)
print("Count of Odd Numbers:", len(odd_numbers))

# (ii) All even numbers
even_numbers = [x for x in L if x % 2 == 0]
print("Even Numbers:", even_numbers)
print("Count of Even Numbers:", len(even_numbers))

# (iii) All prime numbers
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True

prime_numbers = [x for x in L if is_prime(x)]
print("Prime Numbers:", prime_numbers)
print("Count of Prime Numbers:", len(prime_numbers))

# Dictionary
D = {1: "One", 2: "Two", 3: "Three", 4: "Four", 5: "Five"}

# Write to file
with open("dictionary_output.txt", "w") as f:
    for key, value in D.items():
        f.write(f"{key}, {value}\n")

print("Dictionary written to dictionary_output.txt")

# List
L = ["One", "Two", "Three", "Four", "Five"]

# Write to file
with open("list_lengths.txt", "w") as f:
    for word in L:
        f.write(f"{word}, {len(word)}\n")

print("List with lengths written to list_lengths.txt")

import random
import string

# Generate and write random strings to file
with open("random_strings.txt", "w") as f:
    for _ in range(100):
        length = random.randint(10, 15)
        rand_str = ''.join(random.choices(string.ascii_letters, k=length))
        f.write(rand_str + "\n")

print("100 random strings written to random_strings.txt")

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5)+1):
        if n % i == 0:
            return False
    return True

with open("prime_600_800.txt", "w") as f:
    for num in range(600, 801):
        if is_prime(num):
            f.write(str(num) + "\n")

print("Prime numbers between 600 and 800 written to prime_600_800.txt")

