# Singly Linked List - Insert At Head

```cpp
#include <bits/stdc++.h>
using namespace std;

class Node{
    public:
        int val;
        Node *next;

        Node(int val)
        {
            this->val = val;
            this->next = NULL;
        }
};

void indert_at_head(Node* &head, int val)
{
    Node *newNode = new Node(val);
    newNode->next = head;
    head = newNode;
}

void print_list(Node *head)
{
    Node* temp = head;
    while (temp!=NULL)
    {
        cout << temp->val << " ";
        temp = temp->next;
    }
}

int main()
{
    Node *head = NULL;

    int val;
    while (true)
    {
        cin >> val;
        if(val == -1)
        {
            break;
        }

        indert_at_head(head,val);
    }
    
    print_list(head);

    return 0;
}
```


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.