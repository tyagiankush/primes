# Primes
Get prime numbers using multiple algorithms

We have created an application based on Spring Boot to get prime numbers till a limit passed in request URL.

There are 3 Algorithms implemented, to use them use below examples -
1. Divide (divide) - Uses simple trial division
    - https://hostname/prime?num=10&algorithm=divide

2. Sieve (sieve) - Uses Sieve of Eratosthenes
   - https://hostname/prime?num=10&algorithm=sieve

3. Miller-Rabin (mr) - Uses Miller-Rabin primality test
   - https://hostname/prime?num=10&algorithm=mr

**Note:** If no algorithm is passed in the request URL, then 'Divide' algorithm is used by default.

### Output - 
    {
        initial: // number passed in the input
        primes: // list of primes till the initial value
        message: // Contains error messages, if present
    }
    eg -
        Request1 - https://hostname/prime?num=10&algorithm=divide
        Response1 - 
        {
            initial: 10
            Primes: [2,3,5,7]
            message: ""
        }

        Request2 - https://hostname/prime?num=10&algorithm=wrong
        Response2 -
        {
            initial: 10
            Primes: []
            message: "Algorithm not yet implemented."
        }

