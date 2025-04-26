#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <stdbool.h>
#include <string.h>
#include <unistd.h>

//1 start
void rock(){
    printf("ROCK:-\n");
    printf("    _______\n");
    printf("---'   ____)\n");
    printf("      (_____)\n");
    printf("      (_____)\n");
    printf("      (____)\n");
    printf("---.__(___)\n\n");
}
void paper()
{
    printf("PAPER:-\n");
    printf("    ________\n");
    printf("---'    ____)____\n");
    printf("           ______)\n");
    printf("          _______)\n");
    printf("         _______)\n");
    printf("---.__________)\n\n");
}
void scissors()
{
    printf("SCISSORS:-\n");
    printf("    _______\n");
    printf("---'   ____)____\n");
    printf("          ______)\n");
    printf("       __________)\n");
    printf("      (____)\n");
    printf("---.__(___)\n\n");
}
void lizard()
{
    printf("LIZARD:-\n");
    printf("    ---.___________\n");
    printf("           _______)\n");
    printf("    ---.________)\n\n");
}
void spock()
{
    printf("SPOCK:-\n");
    printf("    --\n");
    printf(" -- --  -- --\n");
    printf(" | || |  / // /\n");
    printf(" |_|| | /-//=/\n");
    printf(" | || |/ // /\n");
    printf(" ( || | // /\n");
    printf(" |         .______\n");
    printf(" |         __â««____)\n");
    printf("  |       |\n\n");
}


int main()
{
    while (true)// pora program jeno cholte thake game modes sesh hoar por
    {
        int a;
        while (1)//jathe a er value always 1 ba 2 hoi, execption
        {
            printf("- Press '1' to play infinite mode\n");
            printf("- Press '2' to play WIN-LOSE mode\n");
            printf("\nEnter Your Choice:- ");
            scanf("%d", &a);
            if (a ==1 || a==2)
            {
                system("cls");// for screen clear er jonno, need stdlib library
                break;
            }
            else
            {
            system("cls");
            }

        }

//1 end

//2 start

        switch (a)//
        {
            case 1:// game mode 1 start

                while (true)//jathe game mode 1 bar bar cholte thake
                {
                    int choice;
                    while (true) //jar theke 1-6 er modde thake
                    {
                        printf("----------RULES:----------\n");
                        printf("1. Rock crushes Scissors and Lizard.\n");
                        printf("2. Paper covers Rock and disproves Spock.\n");
                        printf("3. Scissors cut Paper and decapitate Lizard.\n");
                        printf("4. Lizard eats Paper and poisons Spock.\n");
                        printf("5. Spock smashes Scissors and capoizes Rock.\n\n");

                        printf("**Enter 1 for ROCK.\n");
                        printf("**Enter 2 for PAPER.\n");
                        printf("**Enter 3 for SCISSOR.\n");
                        printf("**Enter 4 for LIZARD.\n");
                        printf("**Enter 5 for SPOCK.\n\n");
                        printf("**Enter 6 if you want to exit*\n");
                        printf("Enter your choise: ");
                        scanf("%d", &choice);
                        system ("cls");
                        if(choice>0 && choice<7) break;
                    }

                    printf("\n\n--------------------------------------------------------------------------------------------------------------------------------\n\n");
                    printf("You Choose:- \n"); //amar ba player er move
                    if(choice==6)
                    {
                        system ("cls");
                        break;
                    }
                    switch(choice)
                    {
                        case 1:
                        rock();
                        break;

                        case 2:
                        paper();
                        break;

                        case 3:
                        scissors();
                        break;

                        case 4:
                        lizard();
                        break;

                        case 5:
                        spock();
                        break;

                    }
//2 end
//3 start
                    printf("The Machine Choose: \n");
                    int random_num = (rand() % 5) + 1; //computer er choice generate korar jonno, rand function unistd library theke asche

                    switch(random_num)
                    {
                        case 1:
                        rock();
                            if(choice==random_num)
                            {
                            printf("\n\n------------");
                            printf("\n    DRAW\n");
                            printf("\n    DRAW\n");
                            printf("------------\n");
                            }
                                else if(choice==2)
                                {
                                    printf("\n\n---------------");
                                    printf("\n    YOU WON\n");
                                    printf("\n    YOU WON\n");
                                    printf("---------------\n");

                                }
                                else if(choice==3)
                                {
                                    printf("\n\n--------------------");
                                    printf("\n    COMPUTER WON\n");
                                    printf("\n    COMPUTER WON\n");
                                    printf("--------------------\n");
                                }
                                else if(choice==4)
                                {
                                    printf("\n\n--------------------");
                                    printf("\n    COMPUTER WON\n");
                                    printf("\n    COMPUTER WON\n");
                                    printf("--------------------\n");
                                }
                                else {
                                    printf("\n\n---------------");
                                    printf("\n    YOU WON\n");
                                    printf("\n    YOU WON\n");
                                    printf("---------------\n");
                                }
                        break;

                        case 2:
                        paper();
                            if(choice==random_num)
                            {
                            printf("\n\n------------");
                            printf("\n    DRAW\n");
                            printf("\n    DRAW\n");
                            printf("------------\n");
                            }
                            else if (choice==1)
                            {
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                            else if(choice==3)
                            {
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                            else if(choice==4)
                            {
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                            else{
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                        break;

                        case 3:
                        scissors();
                            if(choice==random_num)
                            {
                            printf("\n\n------------");
                            printf("\n    DRAW\n");
                            printf("\n    DRAW\n");
                            printf("------------\n");
                            }
                            else if (choice==1)
                            {
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                            else if (choice==2)
                            {
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                            else if(choice==4)
                            {
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                            else{
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                        break;

                        case 4:
                        lizard();
                            if(choice==random_num)
                            {
                            printf("\n\n------------");
                            printf("\n    DRAW\n");
                            printf("\n    DRAW\n");
                            printf("------------\n");
                            }
                            else if(choice==1)
                            {
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                            else if(choice==2)
                            {
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                            else if(choice==3)
                            {
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                            else{
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                        break;

                        case 5:
                        spock();
                            if(choice==random_num)
                            {
                            printf("\n\n------------");
                            printf("\n    DRAW\n");
                            printf("\n    DRAW\n");
                            printf("------------\n");
                            }
                            else if (choice==1){
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                            else if(choice==2){
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                            else if(choice==3){
                                printf("\n\n--------------------");
                                printf("\n    COMPUTER WON\n");
                                printf("\n    COMPUTER WON\n");
                                printf("--------------------\n");
                            }
                            else{
                                printf("\n\n---------------");
                                printf("\n    YOU WON\n");
                                printf("\n    YOU WON\n");
                                printf("---------------\n");
                            }
                        break;
                    }
 //3rd Ebd
 //4th start


                        printf("Back To Menu In:- ");
                        for(int i=5; i>0; i--) //timer er jonno
                        {
                            printf("%d ", i);
                            sleep(1); //ek sec er biroti
                        }


                        system ("cls");
                    }
                    break;
                    //gamemode 1 end

//5 start
                    case 2: //game mode 2 start
                                {int round=0;
                                while(round<2)
                                {
                                    system ("cls");
                                    printf("----ONLY ONE WINNER ARENA----\n\n");
                                    printf("[ Enter the amount of rounds one needs to win. The player that wins the choosen amount of Rounds first is the winner ]\n\n");
                                    printf("Note: Please enter at least 3 rounds.\n");
                                    printf("Enter how many rounds going to choose the winner?: ");
                                    scanf("%d", &round);
                                }
                                int comFlag=0, plaFlag=0;
                                while (true)
                                {

                                    int choice = 0;
                                            while (true)
                                            {
                                                system ("cls");
                                                printf("Current Score:-\n");
                                                printf("You: %d\n", plaFlag);
                                                printf("Computer Score: %d\n\n", comFlag);
                                                printf("----------RULES:----------\n");
                                                printf("1. Rock crushes Scissors and Lizard.\n");
                                                printf("2. Paper covers Rock and disproves Spock.\n");
                                                printf("3. Scissors cut Paper and decapitate Lizard.\n");
                                                printf("4. Lizard eats Paper and poisons Spock.\n");
                                                printf("5. Spock smashes Scissors and capoizes Rock.\n\n");
                                                printf("**Enter 1 for ROCK.\n");
                                                printf("**Enter 2 for PAPER.\n");
                                                printf("**Enter 3 for SCISSOR.\n");
                                                printf("**Enter 4 for LIZARD.\n");
                                                printf("**Enter 5 for SPOCK.\n\n");
                                                printf("*Enter 6 if you want to exit*\n");
                                                printf("Enter your choise: ");
                                                scanf("%d", &choice);
                                                if(choice>0 && choice<7) break;
                                            }
                                            printf("\n\n--------------------------------------------------------------------------------------------------------------------------------\n\n");
                                            printf("You Choose:- \n");
                                            if(choice==6)
                                            {
                                                system ("cls");
                                                break;
                                            }
                                            switch(choice)
                                            {
                                                case 1:
                                                rock();
                                                break;

                                                case 2:
                                                paper();
                                                break;

                                                case 3:
                                                scissors();
                                                break;

                                                case 4:
                                                lizard();
                                                break;

                                                case 5:
                                                spock();
                                                break;

                                            }
                                            printf("The Machine Choose: \n");
                                            int random_num = (rand() % 5) + 1;
                                            switch(random_num)
                                            {
                                                case 1:
                                                rock();
                                                    if(choice==random_num)
                                                    {
                                                    printf("\n\n------------");
                                                    printf("\n    DRAW\n");
                                                    printf("\n    DRAW\n");
                                                    printf("------------\n");
                                                    }
                                                        else if(choice==2)
                                                        {
                                                            printf("\n\n---------------");
                                                            printf("\n    YOU WON\n");
                                                            printf("\n    YOU WON\n");
                                                            printf("---------------\n");
                                                            plaFlag++; //to update player score

                                                        }
                                                        else if(choice==3)
                                                        {
                                                            printf("\n\n--------------------");
                                                            printf("\n    COMPUTER WON\n");
                                                            printf("\n    COMPUTER WON\n");
                                                            printf("--------------------\n");
                                                            comFlag++; //to update computer score
                                                        }
                                                        else if(choice==4)
                                                        {
                                                            printf("\n\n--------------------");
                                                            printf("\n    COMPUTER WON\n");
                                                            printf("\n    COMPUTER WON\n");
                                                            printf("--------------------\n");
                                                            comFlag++;
                                                        }
                                                        else {
                                                            printf("\n\n---------------");
                                                            printf("\n    YOU WON\n");
                                                            printf("\n    YOU WON\n");
                                                            printf("---------------\n");
                                                            plaFlag++;
                                                        }
                                                break;

                                                case 2:
                                                paper();
                                                    if(choice==random_num)
                                                    {
                                                    printf("\n\n------------");
                                                    printf("\n    DRAW\n");
                                                    printf("\n    DRAW\n");
                                                    printf("------------\n");
                                                    }
                                                    else if (choice==1)
                                                    {
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                    else if(choice==3)
                                                    {
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                    else if(choice==4)
                                                    {
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                    else{
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                break;

                                                case 3:
                                                scissors();
                                                    if(choice==random_num)
                                                    {
                                                    printf("\n\n------------");
                                                    printf("\n    DRAW\n");
                                                    printf("\n    DRAW\n");
                                                    printf("------------\n");
                                                    }
                                                    else if (choice==1)
                                                    {
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                    else if (choice==2)
                                                    {
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                    else if(choice==4)
                                                    {
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                    else{
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                break;

                                                case 4:
                                                lizard();
                                                    if(choice==random_num)
                                                    {
                                                    printf("\n\n------------");
                                                    printf("\n    DRAW\n");
                                                    printf("\n    DRAW\n");
                                                    printf("------------\n");
                                                    }
                                                    else if(choice==1)
                                                    {
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                    else if(choice==2)
                                                    {
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                    else if(choice==3)
                                                    {
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                    else{
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                break;

                                                case 5:
                                                spock();
                                                    if(choice==random_num)
                                                    {
                                                    printf("\n\n------------");
                                                    printf("\n    DRAW\n");
                                                    printf("\n    DRAW\n");
                                                    printf("------------\n");
                                                    }
                                                    else if (choice==1){
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                    else if(choice==2){
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                    else if(choice==3){
                                                        printf("\n\n--------------------");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("\n    COMPUTER WON\n");
                                                        printf("--------------------\n");
                                                        comFlag++;
                                                    }
                                                    else{
                                                        printf("\n\n---------------");
                                                        printf("\n    YOU WON\n");
                                                        printf("\n    YOU WON\n");
                                                        printf("---------------\n");
                                                        plaFlag++;
                                                    }
                                                break;

                                            } //amar score 1 - computer 3
//5 end
//6 start
                                    if(comFlag==round) {
                                        printf("\nYOU LOST SADLY!\n");
                                        printf("Back To Menu In:- ");
                                        for(int i=5; i<0; i++)
                                        {
                                            printf("%d ", i);
                                            sleep(1);
                                        }
                                        break;
                                    }
                                    if(plaFlag==round)
                                    {
                                        printf("\nCONGRTULATIONS YOU ARE THE WINNER\n");
                                        printf("Back To Menu In:- ");
                                        for(int i=5; i>0; i--)
                                        {
                                            printf("%d ", i);
                                            sleep(1);
                                        }
                                        system("cls");
                                        break;
                                    }
                                    else{
                                        printf("\n-NEXT ROUND IN: ");
                                        for(int i=5; i>0; i--)
                                        {
                                            printf("%d ", i);
                                            sleep(1);
                                        }
                                        system("cls");
                                    }
                                }
                            }
                    break;

            break;
        }
    }
}
// 6 finish
