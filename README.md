# Agri-Shell-Code-In-C
<code>
''#include <stdio.h>
#include <stdlib.h>

void welcome();

void options();

void user();

void date();

void ip();

void list();

void path();

void newfolder();

int main()
{
    welcome();
    options();
    char choice = '0';

    while(choice != '9'){

        if(choice != '\n')
        printf("Aneebs's Shell#: ");
        scanf("%c",&choice);

        if(choice == '0')
            options();
        else if(choice == '1')
            user();
        else if(choice == '2')
            date();
        else if(choice == '3')
            ip();
        else if(choice == '4')
            list();
        else if(choice == '5')
            path();
        else if(choice == '6')
            newfolder();
        else if(choice == '9')
            exit(0);

        if(choice != '\n')
        printf("\n");

    }

    return 0;
}

void welcome()
{
    printf("                #               \n");
    printf("              ## ##             \n");
    printf("            ###  ###            \n");
    printf("           ###    ###           \n");
    printf("         ###   	###          \n");
    printf("        ###############         \n");
    printf("        ###         ###         \n");
    printf("        ###         ###         \n");
    printf("        ###         ###                #\n");
    printf("        ###         ###              ####\n");
    printf("        ###         ##hmad Jajja's  ## ##gri Shell\n");
    printf("Type command number to execute commands that are given below...\n");

}

void options()
{
    printf("\nCommands to execute...\n\n");
    printf("0. OPTIONS\n");
    printf("1. Check current username\n");
    printf("2. Check current date and time\n");
    printf("3. Check ip address of the machine\n");
    printf("4. List content of current directory\n");
    printf("5. Check current working directory path\n");
    printf("6. Create new folder\n");
    printf("9. Exit\n\n");

}


void user()
{
    printf("\n");
    system("whoami");

}

void date()
{
    printf("\n");
    system("date");

}

void ip()
{
    printf("\n");
    system("ip route");

}

void list()
{
    printf("\n");
    system("ls");
}

void path()
{
    printf("\n");
    system("pwd");
}

void newfolder()
{
    printf("\nEnter new folder name: ");
    char foldername[30];
    scanf("%s", foldername);
    char command[40];
    snprintf(command, sizeof command, "mkdir %s", foldername);
    system(command);
}
    ''
</code>
