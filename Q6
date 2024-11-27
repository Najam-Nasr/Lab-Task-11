#include <stdio.h>
#include <stdlib.h>

struct Address {
    char city[50];
    int zip_code;
};

struct Employee {
    char name[50];
    int id;
    float salary;
    struct Address addr;
};

int main() {
    struct Employee emp[3];
    FILE *file = fopen("employees.txt", "w");
    for (int i = 0; i < 3; i++) {
        printf("Enter name: ");
        fgets(emp[i].name, sizeof(emp[i].name), stdin);

        printf("Enter id: ");
        scanf("%d", &emp[i].id);

        printf("Enter salary: ");
        scanf("%f", &emp[i].salary);
        getchar();

        printf("Enter city: ");
        fgets(emp[i].addr.city, sizeof(emp[i].addr.city), stdin);

        printf("Enter zip code: ");
        scanf("%d", &emp[i].addr.zip_code);
        getchar();

        fprintf(file, "%s%d\n%.2f\n%s%d\n", emp[i].name, emp[i].id, emp[i].salary, emp[i].addr.city, emp[i].addr.zip_code);
    }
    fclose(file);

    file = fopen("employees.txt", "r");
    printf("\nEmployee Details from File:\n");
    char buffer[100];
    while (fgets(buffer, sizeof(buffer), file)) {
        printf("%s", buffer);
    }
    fclose(file);
}
