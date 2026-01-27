#include <stdio.h>
#include <math.h>

int main() {
    int n;
    int root;

    printf("Enter an integer: ");
    scanf("%d", &n);

    if (n < 0) {
        printf("Not a perfect square.\n");
        return 0;
    }

    root = sqrt(n);

    if (root * root == n)
        printf("%d is a perfect square.\n", n);
    else
        printf("%d is not a perfect square.\n", n);

    return 0;
}
