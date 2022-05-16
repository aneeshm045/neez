
#include <stdio.h>
#include <stdlib.h>

typedef struct node node;

struct node{
    int data;
    node *link;
};



int main()
{
  node *head = NULL, *current = NULL, *temp = NULL, *ptr =NULL;
   int n = 5, d;
   head = malloc(sizeof(int));
   current = head;
   
   for(int i = 0; i< n; i++){
       //scaning the data we need to enter
       printf("Enter the data");
       scanf("%d", &d);
       //if the link list not the last node
       if (i!= n-1){
       
       current->data = d;
       temp = current;
       current = malloc(sizeof(node));
       temp->link = current;
       }
       //if thi node is the last we need to set the last address as null
       else{
           current-> data = d;
           current-> link = NULL;
       }
       
   }
   
   // to print the data that we entered
   ptr = head;
   while(ptr!=NULL){
       printf("%d ", ptr->data);
       ptr = ptr->link;
   }
   
   return 0;
    
}

