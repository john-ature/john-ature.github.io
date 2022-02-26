#HELLO JOHN

##INSERTION AND CREATION IN SINGLE LINKED LIST
-------------------------------------
```
 ` #include<stdio.h>
  #include<conio.h>
  #include<stdlib.h>
  struct node
  {
  int info;
  struct node *link;
  };
  typedef struct node NODE;
  NODE *start=NULL,*cptr,*ptr,*NN;
  creation()
  {
  int data;
  printf("enter the data");
  scanf("%d",&data);
  if(start==NULL)
  {
  start=(NODE*)malloc(sizeof(NODE));
  start->info=data;
  start->link=NULL;
  cptr=start;
  }
  else
    {
     NN=(NODE*)malloc(sizeof(NODE));
     NN->info=data;
     NN->link=NULL;
     cptr->link=NN;
     cptr=NN;
    }
   }
   insertbeg()
    {
    int data;
    NN=(NODE*)malloc(sizeof(NODE));
    printf("entr the data ");
    scanf("%d",&data);
    NN->info=data;
    NN->link=start;
    start=NN;
    }
    insertend()
    {
    int data;
    cptr=start;
    while(cptr->link!=NULL)
    {
    cptr=cptr->link;
    }
    NN=(NODE*)malloc(sizeof(NODE));
    printf("Enter the data");
    scanf("%d",&data);
    NN->info=data;
    NN->link=NULL;
    cptr->link=NN;
    }
    insertpos()
     {
     int data,pos,i;
     printf("enter the position");
     scanf("%d",&pos);
     printf("enter the data");
     scanf("%d",&data);
     cptr=start;
     for(i=1;i<pos-1;i++)
     {
     cptr=cptr->link;
     }
     NN=(NODE*)malloc(sizeof(NODE));
     NN->info=data;
     NN->link=cptr->link;
     cptr->link=NN;
     }

   display()
   {
   if(start==NULL)
    printf("list is empty");
    else
      {
      cptr=start;
      while(cptr!=NULL)
        {
        printf("%d-> ", cptr->info);
        cptr=cptr->link;
        }
    }
  }
  void main()
   {
   int ch,choice;
    clrscr();
    do
     {
    printf("1.creation\n");
    printf("2.insertbeg\n");
    printf("3.insertend\n");
    printf("4.insertpos\n");
    printf("5.display\n");
    printf("6.exit\n");
    printf("enter your choice");
    scanf("%d",&ch);
    switch(ch)
     {
     case 1: creation();
     break;
     case 2: insertbeg();
     break;
     case 3:insertend();
     break;
     case 4: insertpos();
     break;
     case 5:
      display();
      break;
      case 6:
       exit(0);
       default:
       printf("invalid choice");
      }
      printf("do you want to continue press 1\n");
      scanf("%d",&choice);
     } while(choice==1);
    }

`
```

##DELETION IN SINGLE LINKED LIST
------------------------------------
```
`#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
struct node
{
int info;
struct node *link;
};
typedef struct node NODE;
NODE *start=NULL,*cptr,*prev,*NN;
creation()
{
int data;
printf("enter the data");
scanf("%d",&data);
if(start==NULL)
{
start=(NODE*)malloc(sizeof(NODE));
start->info=data;
start->link=NULL;
cptr=start;
}
else
  {
   NN=(NODE*)malloc(sizeof(NODE));
   NN->info=data;
   NN->link=NULL;
   cptr->link=NN;
   cptr=NN;
  }
 }
 delbeg()
  {
  if(start==NULL)
  printf("list is empty");
  else
    {
    cptr=start;
    printf("deleted element is %d",cptr->info);
    start=start->link;
    free(cptr);
    }
  }
  delend()
  {
  if(start==NULL)
  printf("list is empty");
  else
  {
  cptr=start;
  while(cptr->link!=NULL)
  {
  prev=cptr;
  cptr=cptr->link;
   }
   printf("deleted element is %d" ,cptr->info);
   free(cptr);
   prev->link=NULL;
    }
  }
  delpos()
   {
   int pos,i;
   printf("enter the position where to delete");
   scanf("%d",&pos);
   cptr=start;
   for(i=1;i<pos;i++)
   {
   prev=cptr;
   cptr=cptr->link;
   }
   printf("deleted element is %d ",cptr->info);
   prev->link=cptr->link;
   free(cptr);
   }

 display()
 {
 if(start==NULL)
  printf("list is empty");
  else
    {
    cptr=start;
    while(cptr!=NULL)
      {
      printf("%d-> ", cptr->info);
      cptr=cptr->link;
      }
  }
}
void main()
 {
 int ch,choice;
  clrscr();
  do
   {
  printf("1.creation\n");
  printf("2.delbeg\n");
  printf("3.delend\n");
  printf("4.delpos\n");
  printf("5.display\n");
  printf("6.exit\n");
  printf("enter your choice");
  scanf("%d",&ch);
  switch(ch)
   {
   case 1: creation();
   break;
   case 2: delbeg();
   break;
   case 3:delend();
   break;
   case 4: delpos();
   break;
   case 5:
    display();
    break;
    case 6:
     exit(0);
     default:
     printf("invalid choice");
    }
    printf("do you want to continue press 1\n");
    scanf("%d",&choice);
   } while(choice==1);
  }
  `
 ```
--------------------------------
