# Linked-list-traversing-
Traversing a singly linked list in C++



     // Traversing a singly linked list in C++

    # include <iostream>
    using namespace std;

    struct Node
    {
        int data;
        Node *next;
        Node(int x)
        {
            data = x;
            next = NULL;
        }
    };

    void printlist(Node *head)
    {
        Node *curr = head;
        while(curr!=NULL)
        {
            cout<<curr->data<<" ";
            curr = curr->next;
        }
    }

    int main()
    {
        Node *head = new Node(10);
        Node *temp1 = new Node(20);
        Node *temp2 = new Node(30);
        head->next = temp1;
        temp1->next = temp2;
        printlist(head);
        return 0;
    }
   
   
   
output

10 20 30 


#linked list recursive traversing

     // Traversing a singly linked list in C++

     # include <iostream>
     using namespace std;

     struct Node
     {
         int data;
         Node *next;
         Node(int x)
         {
             data = x;
             next = NULL;
         }
     };

     void printlist(Node *head)
     {
         Node *curr = head;
         while(curr!=NULL)
         {
             cout<<curr->data<<" ";
             curr = curr->next;
         }
     }

     void rprint(Node *head)
     {
         if(head==NULL)
             return ;
         cout<<(head->data)<<" ";
         rprint(head->next);
     }
     int main()
     {
         Node *head = new Node(10);
         Node *temp1 = new Node(20);
         Node *temp2 = new Node(30);
         head->next = temp1;
         temp1->next = temp2;
         printlist(head);
         cout<<endl;
         rprint(head);
         return 0;
     }
     
     
 output
 
10 20 30 
10 20 30 
