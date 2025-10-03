# Singly Linked List  - Insert At Any Position

```cpp
#include <bits/stdc++.h>
using namespace std;

class Node{
    public:
        int val;
        Node* next;

        Node(int val)
        {
            this->val = val;
            this->next = NULL;
        }
};

void insert_at_any_pos(Node *&head, int pos, int val)
{
    Node *newNode = new Node(val);

    if(pos == 0)
    {
        newNode->next = head;
        head = newNode;
        return;
    }

    Node *temp = head;
    int index = pos - 1;
    while (index--)
    {
        temp = temp->next;
    }

    newNode->next = temp->next;
    temp->next = newNode;
}

void pitn_list(Node *head)
{
    Node *temp = head;
    while (head!=NULL)
    {
        cout << temp->val << " ";
        temp = temp->next;
    }
}

int main()
{
    Node *head = new Node(10);
    Node *a = new Node(20);
    Node *b = new Node(30);
    Node *c = new Node(40);

    head->next = a;
    a->next = b;
    b->next = c;

    insert_at_any_pos(head,0,100);
    pitn_list(head);
    
    return 0;
}
```


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.