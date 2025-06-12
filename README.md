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
