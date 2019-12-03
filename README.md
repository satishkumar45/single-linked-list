# single-linked-list
just linking nodes
#logic code for single linked list

#creating a structure 
struct List
{
   int number;
   struct List *link; 
};

#write a main function 

main()
{
   #create a structure pointer for header
   struct List *header=NULL;
   stack(&header,10);
   stack(&header,20);
   linkedlist(&header);
}
void stack(struct List **h,int n)
{
   struct List *t=NULL;
   t=(struct List *)malloc(sizeof(struct List));
   t->number=n;
   t->link=NULL;
   if(*h==NULL)
   printf("no link is occurred\n");
   else
   {
      *h=t;
      t->link =*h;
   
   }

}
void linkedlist(struct List **m)
{
   struct List *k=NULL;
   k=*m;
   while(k!=NULL)
   {
      printf("%d\n",k->number);
      k=k->link;
   
   }

}
