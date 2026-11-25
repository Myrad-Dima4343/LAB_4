#include <stdio.h>
#include <math.h>

int main() {
    //66
    double a, res = 1.0;
    int n1;
    printf("--- Завдання 66 ---\nВведіть a та n: ");
    scanf("%lf %d", &a, &n1);
    for (int i = 0; i < n1; i++) res *= a;
    printf("Результат: %.4lf\n\n", res);

    // 73
    int n2;
    double sum2 = 1.0, fact = 1.0;
    printf("--- Завдання 73 ---\nВведіть n: ");
    scanf("%d", &n2);
    for (int i = 1; i <= n2; i++) {
        fact *= i;
        sum2 += 1.0 / fact;
    }
    printf("Сума: %.6lf\n\n", sum2);

    //92
    int grade, sum3 = 0;
    printf("--- Завдання 92 ---\nВведіть 20 оцінок: ");
    for (int i = 0; i < 20; i++) {
        scanf("%d", &grade);
        sum3 += grade;
    }
    printf("Середній бал: %.2lf\n\n", sum3 / 20.0);

    //129
    printf("--- Завдання 129 ---\n");
    for (int num = 1000; num <= 9999; num++) {
        int t = num, sum4 = 0;
        while (t > 0) {
            int d = t % 10;
            sum4 += d * d * d * d * d;
            t /= 10;
        }
        if (sum4 == num) printf("Знайдено: %d\n", num);
    }
    printf("\n");

    //190
    double n5, sum5 = 1.0;
    int k = 1;
    printf("--- Завдання 190 ---\nВведіть n: ");
    scanf("%lf", &n5);
    while (sum5 <= n5) {
        k++;
        sum5 += 1.0 / k;
    }
    printf("Результат: %.6lf\n\n", sum5);

    //1
    long long n6, orig, rev = 0;
    printf("--- Завдання 1 ---\nВведіть натуральне число: ");
    scanf("%lld", &n6);
    orig = n6;
    while (n6 > 0) {
        rev = rev * 10 + n6 % 10;
        n6 /= 10;
    }
    printf("Зворотне: %lld\n", rev);
    if (rev > orig) printf("Зворотне більше\n\n");
    else if (rev < orig) printf("Зворотне менше\n\n");
    else printf("Числа рівні\n\n");

    //128
    printf("--- Завдання 128 ---\n");
    for (int num = 10; num <= 99; num++) {
        int tens = num / 10, units = num % 10;
        if (num == units * units + tens * tens * tens)
            printf("Знайдено: %d\n", num);
    }
    printf("\n");

    //17
    int n8;
    printf("--- Завдання 17 ---\nВведіть n: ");
    scanf("%d", &n8);
    for (int i = 1; i <= 10; i++)
        printf("%d * %d = %d\n", n8, i, n8 * i);
    printf("\n");

    //234
    double a9, b9, h9;
    printf("--- Завдання 234 ---\nВведіть a, b, h: ");
    scanf("%lf %lf %lf", &a9, &b9, &h9);
    for (double x = a9; x <= b9 + 1e-9; x += h9) {
        double c = cos(x);
        printf("%.3lf | %.4lf\n", x, sqrt(x) * c * c);
    }
    printf("\n");

    //225
    double a10, b10, h10;
    printf("--- Завдання 225 ---\nВведіть a, b, h: ");
    scanf("%lf %lf %lf", &a10, &b10, &h10);
    for (double x = a10; x <= b10 + 1e-9; x += h10) {
        double s = sin(x);
        printf("%.3lf | %.4lf\n", x, s * s);
    }

    return 0;
}
