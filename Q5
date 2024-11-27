#include <stdio.h>

struct Date {
    int day,month,year;
};

struct Event {
    char event_name[50];
    char location[50];
    struct Date date;

};

int main() {
    struct Event e;

    printf("Enter event name: ");
    fgets(e.event_name, sizeof(e.event_name), stdin);

    printf("Enter date (day month year): ");
    scanf("%d %d %d", &e.date.day, &e.date.month, &e.date.year);
    getchar();

    printf("Enter location: ");
    fgets(e.location, sizeof(e.location), stdin);

    printf("\nEvent Details:\n");
    printf("Name: %s", e.event_name);
    printf("Date: %02d-%02d-%04d\n", e.date.day, e.date.month, e.date.year);
    printf("Location: %s", e.location);

    return 0;
}
