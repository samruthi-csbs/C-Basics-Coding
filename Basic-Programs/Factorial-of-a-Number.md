Factorial of a number n means:

n! = n × (n-1) × (n-2) × ... × 1

##SAMPLE CODE---



#include <stdio.h>

int main() {
    int n, i;
    long long fact = 1;

    printf("Enter a number: ");
    scanf("%d", &n);

    if (n < 0) {
        printf("Factorial of negative number is not defined.");
    } else {
        for (i = 1; i <= n; i++) {
            fact = fact * i;
        }
        printf("Factorial of %d is %lld", n, fact);
    }

    return 0;
}

Enter a number: 5
Factorial of 5 is 120
🧩 Trick to Remember the Logic
“FACT starts at ONE, multiplies EVERYONE”
Factorial always starts from 1

Loop multiplies each number
End at n
