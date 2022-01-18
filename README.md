#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int r_p_s(char you ,char computer)
{
    if (computer==you)
        return 0 ;
    else if (computer=='r'&&you=='p')
        return 1;
      else if (computer=='p'&&you=='r')
        return -1;
          else if (computer=='p'&&you=='s')
        return 1;
          else if (computer=='s'&&you=='p')
        return -1;
          else if (computer=='s'&&you=='r')
        return 1;
          else if (computer=='r'&&you=='s')
        return -1;
}
int main()
{
    char computer ,you;
    int decision,randnum;
    printf("choose 'r' for rock ,'p' for paper ,'s' for scissor ,");
    scanf("%c",&you);
    srand(time(0));
    randnum=rand()%100;
    if(randnum<=35)
        computer='r';
    else if(randnum>35&&randnum<66)
    computer='p';
    else
        computer='s';
     decision=r_p_s(you,computer);

    if(decision==0)
    printf("Draw !");
    else if (decision==1)
        printf("you win ! ");
    else
        printf("you lose !");
        printf("\nyou choose %c and computer choose %c ",you,computer);
    return 0;
}
