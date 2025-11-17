
#include <stdio.h>
#include <string.h>

int main() {
    char command[20];
    int hasKey = 0;

    printf("You are in a dark room.\n");
    printf("Commands: 'move', 'look', 'findkey', 'explore', 'open', 'run'\n");

    while (1) {
        printf("\nWhat do you want to do? ");
        scanf("%s", command);

        if (strcmp(command, "move") == 0) {
            printf("You move forward...\n");
            printf("  O\n");
            printf(" /|\\\n");
            printf(" / \\\n");
        } else if (strcmp(command, "look") == 0) {
            printf("You see an old treasure chest!\n");
        } else if (strcmp(command, "findkey") == 0) {
            printf("You found a key!\n");
            hasKey = 1;
        } else if (strcmp(command, "explore") == 0) {
            printf("You look around the room and see a locked door.\n");
        } else if (strcmp(command, "open") == 0) {
            if (hasKey) {
                printf("You unlocked the door and escaped! You are free!\n");
                break;
            } else {
                printf("The door is locked. You need a key.\n");
            }
        } else if (strcmp(command, "run") == 0) {
            printf("You try to run, but the door is locked!\n");
        } else {
            printf("I don't understand that command.\n");
        }
    }

    return 0;
}
