def find_prime(n, m):
    primes = []
    for num in range(2, n + 1):
        is_prime = True
        for i in range(2, int(num ** 0.5) + 1):
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            primes.append(num)

    if m > len(primes) or m < 1:
        return -1
    else:
        return primes[m - 1]

n = int(input())
m = int(input())

print(find_prime(n, m))
