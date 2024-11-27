#include <stdio.h>

struct Marks {
    int maths;
    int science;
    int english;
};

struct Student {
    int roll_no;
    char name[50];
    struct Marks marks;
};

int main() {
    struct Student students[5];
    int i;
    float average;

    // Input data for 5 students
    for (i = 0; i < 5; i++) {
        printf("Enter details for Student %d:\n", i + 1);
        printf("Roll No: ");
        scanf("%d", &students[i].roll_no);
        printf("Name: ");
		printf("Name: ");
		fgets(students[i].name, sizeof(students[i].name), stdin);
        printf("Enter marks (Maths, Science, English): ");
        scanf("%d %d %d", &students[i].marks.maths, &students[i].marks.science, &students[i].marks.english);

        printf("\n");
    }

    printf("Student Details and Average Marks:\n");
    for (i = 0; i < 5; i++) {
        printf("Student %d:\n", i + 1);
        printf("  Roll No: %d\n", students[i].roll_no);
        printf("  Name: %s\n", students[i].name);
        average = (students[i].marks.maths + students[i].marks.science + students[i].marks.english) / 3.0;
        printf("  Marks: Maths = %d, Science = %d, English = %d\n",students[i].marks.maths, students[i].marks.science, students[i].marks.english);
        printf("  Average Marks: %.2f\n\n", average);
    }

}
