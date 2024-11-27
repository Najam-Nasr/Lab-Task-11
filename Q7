#include <stdio.h>

struct Company {
    char name[50],departments[5][50];
    int year_established;

};

int main() {
    struct Company c;
    int n;

    printf("Enter company name: ");
    fgets(c.name, sizeof(c.name), stdin);

    printf("Enter year established: ");
    scanf("%d", &c.year_established);
    getchar();

    printf("Enter number of departments (max 5): ");
    scanf("%d", &n);
    getchar();

    for (int i = 0; i < n; i++) {
        printf("Enter department %d: ", i + 1);
        fgets(c.departments[i], sizeof(c.departments[i]), stdin);
    }

    printf("\nCompany Details:\n");
    printf("Name: %s", c.name);
    printf("Year Established: %d\n", c.year_established);
    printf("Departments:\n");
    for (int i = 0; i < n; i++) {
        printf("  %s", c.departments[i]);
    }

}
