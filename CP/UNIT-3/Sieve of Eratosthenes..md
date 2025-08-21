Algorithm sieveOfEratosthenes(n):

    // Step 1: create array
    boolean[] prime = new boolean[n+1]

    // Step 2: mark all as true
    for i = 0 to n:
        prime[i] = true

    // Step 3: 0 and 1 are not prime
    prime[0] = false
    prime[1] = false

    // Step 4: eliminate multiples
    for p = 2 to sqrt(n):
        if prime[p] == true:
            for multiple = p*p to n step p:
                prime[multiple] = false

    // Step 5: print primes
    for i = 2 to n:
        if prime[i] == true:
            print i
