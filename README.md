#include <stdio.h>

int calculateTotal(int marks[], int n) {
    int total = 0;
    for (int i = 0; i < n; i++) {
        total += marks[i];
    }
    return total;
}

float calculateAverage(int total, int n) {
    return (float)total / n;
}

void showPerformance(float avg) {
    printf("\nClass Performance: ");
    if (avg >= 90) {
        printf("Excellent 🌟\n");
    } else if (avg >= 75) {
        printf("Very Good 👍\n");
    } else if (avg >= 50) {
        printf("Average 🙂\n");
    } else {
        printf("Needs Improvement 😟\n");
    }
}

int main() {
    int marks[8];   
    int total;
    float average;
    printf("Enter marks of 8 students (out of 100):\n");
    for (int i = 0; i < 8; i++) {
        printf("Student %d: ", i + 1);
        scanf("%d", &marks[i]);
    }
    total = calculateTotal(marks, 8);
    average = calculateAverage(total, 8);
    printf("\nTotal Marks of Class = %d", total);
    printf("\nAverage Marks = %.2f", average);
    showPerformance(average);
    return 0;
}
