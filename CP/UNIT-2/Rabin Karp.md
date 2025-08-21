# Rabin karp

- It is a String searching algorithm which is used to find whether a pattern is there in the given string or not.
- Instead of checking each characters one by one, it uses a hashing function called **Rolling hashing function** to find the pattern match in the string quickly.

 ### Rolling hashing Function

 ```
hash value = A*(d^m-1)+A*(d^m-2)+........+A*(d^m-m)
hash new = 0
