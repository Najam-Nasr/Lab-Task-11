#include <stdio.h>
#include <string.h>

void replace_word_in_file(const char *filename, const char *old_word, const char *new_word) {
    FILE *file;
    char content[10000];
    char temp[10000];   
    char *pos;          
    int old_len, new_len;

    file = fopen(filename, "r");
    if (file == NULL) {
        printf("Error: Could not open the file.\n");
        return;
    }

    content[0] = '\0';
    while (fgets(temp, sizeof(temp), file) != NULL) {
        strcat(content, temp);
    }
    fclose(file); 

    temp[0] = '\0';
    char *current = content;
    old_len = strlen(old_word);
    new_len = strlen(new_word);

    while ((pos = strstr(current, old_word)) != NULL) {
        strncat(temp, current, pos - current);
        strcat(temp, new_word);
        current = pos + old_len;
    }
    strcat(temp, current);

    file = fopen(filename, "w");
    if (file == NULL) {
        printf("Error: Could not open the file for writing.\n");
        return;
    }
    fputs(temp, file);
    fclose(file);

    printf("Word replacement successful.\n");
}

int main() {
    char filename[] = "data.txt";
    char old_word[] = "babar"; 
    char new_word[] = "rizwan"; 

    replace_word_in_file(filename, old_word, new_word);

    return 0;
}
