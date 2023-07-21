#include <stdio.h>

// Function to generate Fibonacci series up to 'n' terms
void generateFibonacci(int n) {
    int num1 = 0, num2 = 1, nextTerm;

    printf("Fibonacci Series up to %d terms:\n", n);

    for (int i = 0; i < n; i++) {
        if (i <= 1)
            nextTerm = i;
        else {
            nextTerm = num1 + num2;
            num1 = num2;
            num2 = nextTerm;
        }
        printf("%d ", nextTerm);
    }
    printf("\n");
}

int main() {
    int n;

    printf("Enter the limit 'n' for the Fibonacci series: ");
    scanf("%d", &n);

    generateFibonacci(n);

    return 0;
}
