from decimal import *
getcontext().prec = 100

def nilakantha(reps):
        result = Decimal(3.0)
        op = 1
        n = 2
        for n in range(2, 2*reps+1, 2):
                result += 4/Decimal(n*(n+1)*(n+2)*op)
                op *= -1
        return result

print("How many repetitions?")
repetitions = int(input())
print(nilakantha(repetitions))
print("3.1415926535897932384626433832795028841971693993751058209749445923078164062862089986280348253421170679")