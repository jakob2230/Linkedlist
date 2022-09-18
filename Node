# Linkedlist


import javax.swing.JOptionPane;

public class Node {
    private int data;//actual value
    private Node head, next; //address

    Node(){
        head = next=null; //empty node
    }

    public boolean isEmpty(){
        return head == null;
    }

    public void error_message(String msg){
        JOptionPane.showMessageDialog(null,msg,"ERROR", JOptionPane.ERROR_MESSAGE);
    }

    //operations
    public void addFirst(int value){
        Node newNode = new Node();
        if(isEmpty()){
            newNode.data = value;
            newNode.next = null;
            head = newNode;
        }else{
            newNode.data = value;
            newNode.next = head;
            head = newNode;
        }
    }//end of addFirst

    public String traversal(){
        String hold = "";
        if(isEmpty()){
            System.out.println("List is empty");
        }else{
            Node link = head;
            while(link != null){
                //hold += "[" + link.data + "|" + link.next + "] ->";
                hold += link.data + " ";
                link = link.next;
            }
        }
        return head + "->" + hold;
    }

    public void addLast(int value){
        if(isEmpty()){
            addFirst(value);
        }else{
            Node link = head;
            while (link.next != null){
                link = link.next; //transversal toward the list
            }//loop guarantees the end of the list
            Node newNode = new Node();//create new node
            newNode.data = value;
            newNode.next = null;
            link.next = newNode;//make the Node a new Node 
        }
    }

    public int currentSize(){
        int counter = 1;
        if(isEmpty()){
            error_message("List is empty");
        }else{
            Node link = head;
            while(link.next != null){
                link = link.next;
                counter++;
            }
        }
        return counter;
    }

    public void addAtPosition(int value, int position){
        if(isEmpty()){
            error_message("List is empty. Node is added at the beginning");
            addLast(value);
        }else if (position == 0){
            error_message("Node is added at the beginning");
            addFirst(value);
        }else if (position < 0 && position > currentSize()){
            error_message(position + " IS NOT VALID");
        }else{
            Node visit, link;
            visit = link = head;
            int ctr = 1;
            while (ctr!=position){
                visit = visit.next;
                ctr++;
            }
            while(link.next!=visit){
                link = link.next;
            }
            Node newNode = new Node();
            newNode.data = value;
            newNode.next = visit;
            link.next = newNode;
        }
    }

    public void deleteAtFirst(){
        if(isEmpty()){
            error_message("Deleting not allowed. List is empty");
        }else{
            Node link = head;
            head = link.next;
            System.out.println("Deleting successful");
        }
    }

    public void deleteAtLast(){
        if (isEmpty()){
            error_message("Deleting not allowed. List is empty");
        }else{
            Node visit, link;
            visit = link = head;
            while(visit.next != null){
                visit = visit.next;
            }while(link.next != visit){
                link = link.next;
            }
            link.next = null;
            System.out.println("Deleting successful!");
        }
    }

    public void deleteAtPosition(int position){
        if(isEmpty()){
            error_message("The list is empty. Try to add value");
        }else if (position == 0){
            deleteAtFirst();
        }else if (position < 0 || position >= currentSize()){
            error_message("Position not VALID");
        }else{
            Node visit, link, pointer;
            visit = link = pointer = head;
            int ctr = 0;
            while (ctr!=position-1){
                visit = visit.next;
                ctr++;
            }while(link.next!=visit){
                link = link.next;
            }
            ctr = 1;
            while (ctr!=position){
                pointer = pointer.next;
                ctr--;
            }
            visit = next;
        }
    }

    
}
