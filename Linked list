#include<stdio.h>
#include<stdlib.h>

typedef struct node{
int data;
struct node *link;
}aa;
aa *head,*p;
int i;

void begin();
void end();
void middle();
void insert();
int length();
void print();
void nstart();
void nend();
void searchk();
void searchi();
void deletek();
void reverse();
void deletei();
void deletelist();


int main(){
int m,a,n;
do{printf("\n0.Make linked list.\n1.Insert an element at beginning of the list.\n2.Insert an element at the end of the list.\n");
printf("3.Insert an element at a particular index position of the list.\n4.Delete an element from the list given the key.\n");
printf("5.Delete an element from the list given the index of the node.\n6.Search an element from the list given the key.\n");
printf("7.Delete the linked list.\n8.Search an element from the list given the index of the node.\n");
printf("9.Get the nth node of the list.\n10.Get the nth node from the end of the list.\n11.Count the number of nodes of the list.\n");
printf("12.Get the middle element of the list.\n13.Print the list.\n14.Reverse the list.\n  -1 to exit\n");
scanf("%d",&n);
if(n==0){
    aa *temp=NULL;
    printf("enter no. of elements\n");
    scanf("%d",&m);
for(i=0;i<m;i++){
    temp=(aa*)malloc(sizeof(aa));
    printf("enter data\n");
    scanf("%d",&(temp->data));
    temp->link=NULL;
    if(head==NULL){
        head=temp;
    }
    else{
        p=head;
        while(p->link!=NULL){
            p=p->link;
        }
        p->link=temp;
    }
}
}

if(n==1){
    begin();
}
if(n==2){
    end();
}
if(n==3){
    insert();
}
if(n==4){
    deletek();
}
if(n==5){
    deletei();
}
if(n==6){
    searchk();
}
if(n==7){
    deletelist();
}
if(n==8){
    searchi();
}
if(n==9){
    nstart();
}
if(n==10){
    nend();
}
if(n==11){
    a=length();
    printf("%d\n",a);
}
if(n==12){
    middle();
}
if(n==13){
    print();
}
if(n==14){
    reverse();
}

}while(n!=-1);
return 0;
}
void begin(){
    aa *temp;
    temp=(aa*)malloc(sizeof(aa));
    printf("enter element\n");
    scanf("%d",&(temp->data));
    temp->link=head;
    head=temp;
}

void end(){
    aa *temp;
    if(length()==0){
        begin();
    }
    else{
    temp=(aa*)malloc(sizeof(aa));
    temp->link=NULL;
    printf("enter element\n");
    scanf("%d",&(temp->data));
    p=head;

        while(p->link!=NULL){
        p=p->link;
    }
        p->link=temp;
}
}

void insert(){
    int v;
    aa *temp,*q;
    temp=(aa*)malloc(sizeof(aa));
    printf("place of element\n");
    scanf("%d",&v);
    if(v==1){
        begin();
    }
    else{
    printf("enter element\n");
    scanf("%d",&(temp->data));
    p=head;
    for(i=0;i<v-2;i++){
        p=p->link;
    }
    q=p->link;
    p->link=temp;
    temp->link=q;
}
}
void deletek(){
    int o=0,k,c=length();
    aa *p=head;
    aa *q=head;
    printf("enter the key\n");
    scanf("%d",&k);
    while(p->data!=k){
        p=p->link;
        o+=1;
    }
    if(o==0){
        head=p->link;
        free(p);
    }
    if(o<=c && o>0){
        p=head;
        while(o>0)
    {q=p;
    p=p->link;
    o--;}
    q->link=p->link;
    free(p);
    }
}

void deletei(){
int a,c=length();
aa *p=head;
aa *q=head;
printf("enter the index\n");
scanf("%d",&a);
if(a<=c){if(a==1){
    head=p->link;
    free(p);
}
else{
   while(a>1)
    {q=p;
    p=p->link;
    a--;}
    q->link=p->link;
    free(p);

}
}
}


void deletelist()
{
   aa *current = head;
   aa *link;

   while (current != NULL)
   {
       link = current->link;
       free(current);
       current = link;
   }
    head = NULL;
}

void nstart(){
int k;
p=head;
printf("enter node no.\n");
scanf("%d",&k);
for(i=0;i<k-1;i++){
    p=p->link;
}
printf("\n%d\n",p->data);
}

void middle(){
aa *p=head;
int x=(length())/2;
while(x){
    p=p->link;
    x--;
    }
printf("\n%d\n",p->data);
}

void searchi(){
int k,c=length();
p=head;
printf("enter index\n");
scanf("%d",&k);
if(k>c){
    printf("error\n");
}
else{
for(i=0;i<k-1;i++){
    p=p->link;
}
printf("\n%d\n",p->data);
}
}

void searchk(){
int k,count=0,b=0,c=length();
p=head;
printf("enter key\n");
scanf("%d",&k);
while(b!=c){
    if(k==p->data){
        printf("\npresent\n");
        count+=1;
        break;
    }
    b+=1;
    p=p->link;
}
if(!count){
    printf("\nnot present\n");
}
}

void nend(){
int k,m,c=length();
p=head;
printf("enter node no.\n");
scanf("%d",&k);
m=c-k;
for(i=0;i<m;i++){
    p=p->link;
}
printf("\n%d\n",p->data);
}

int length(){
    int count=0;
    p=head;
    while(p!=NULL){
        count++;
        p=p->link;
    }
    return count;
}

void print(){
    p=head;
    while(p!=NULL){
        printf("%d\n",p->data);
        p=p->link;
}
}

void reverse()
    {
        aa *current = head;
        aa *prev = NULL, *link = NULL;
        while (current != NULL)
        {
            link = current->link;
            current->link=prev;
            prev = current;
            current = link;
        }
        head = prev;
    }







