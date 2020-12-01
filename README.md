# prime-number
program checks if number is prime or not
#include<stdio.h>
int isPrime(int, int);
int main()
{
	int num, prime;
    printf("Enter a number: ");
    scanf("%d", &num);
    prime = isPrime(num, num/2);
    if(prime == 1)
    {
        printf("%d is a prime number\n\n", num);
    }
    else
    {
        printf("%d is not a prime number", num);
    }
    
    return 0;
}

int isPrime(int n, int i)
{
    if(i == 1)
        return 1; 
    else
    {
        if(n%i == 0)
            return 0;
        else
            isPrime(n, i-1);    
    }
}
