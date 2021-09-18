# reverse-LinkedList-by-iterative-method-in-C
reverse LinkedList by iterative method in C

#include <stdio.h>
#include <stdlib.h>
struct node{
    int data;
    struct node *next;
};

void reverse(struct node *head){
    struct node *prev , *current ,*next;
    current = head;
    prev =NULL;
    while(current !=NULL){
        next=current->next;
        current->next=prev;
        prev=current;
        current=next;
        
    }
    head = prev;
    printf("reverse list");
    while(head !=NULL){
        printf("\n%d",head->data);
        head=head->next;
        
    }
    
}





int main()
{

    struct node *head , *first , *second , *third , *fourth , *fifth;
    head = (struct node*) malloc(sizeof(struct node));
    first = (struct node*) malloc(sizeof(struct node));
    second = (struct node*) malloc(sizeof(struct node));
    third = (struct node*) malloc(sizeof(struct node));
    fourth = (struct node*) malloc(sizeof(struct node));
    fifth = (struct node*) malloc(sizeof(struct node));
    
    head->data=1;
    head->next=first;
    
    first->data=2;
    first->next=second;
    
    second->data=3;
    second->next=third;
    
    third->data=4;
    third->next=fourth;
    
    fourth->data=5;
    fourth->next=fifth;
    
    fifth->data=6;
    fifth->next=NULL;
    
    reverse(head);
    

    return 0;
}

