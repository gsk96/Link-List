#include <bits/stdc++.h>
using namespace std;

class node
{
    public:
    int data;
    node* next_address;
};

void push(node** first, int new_data)  
{  
    node* new_node = new node();  
    new_node->data = new_data;  
    new_node->next_address = (*first);  
    (*first) = new_node;  
}  

void print_list(node* n)
{
    while(n != NULL)
    {
    	cout<<n -> data<<" ";
    	n = n -> next_address;	
	}
    
}

int main()
{
    node* first = NULL;
    node* second = NULL;    
    node* third = NULL;

    first = new node();
    second = new node();
    third = new node();

    
    first -> data = 13;
    first -> next_address = second;
    push(&first, 9);
    second -> data = 26;
    second -> next_address = third;
    third -> data = 52;
    third -> next_address = NULL;
	print_list(first);
	return 0;
}