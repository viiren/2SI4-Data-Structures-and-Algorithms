package stack;

import java.util.EmptyStackException;

/**
 *
 * @author virenwaghela
 */
public class Stack1<E>{
    
    private Node<E> head;
    
    public Stack1(){ //Creates Empty Stack 
        head = null; //Theta(1) Runtime
    }
    public boolean isEmpty(){
        if(head==null) //Stack is empty if there are no nodes
            return true; //Theta(1) Runtime
        return false;       
    }
    
    public void push(int e){ //Stacks are LIFO
        head = new Node<E>(e,head); //Theta(1) Runtime
    }
    
    public E pop() throws EmptyStackException{ //Deletes First Node of LL and returns element stored there
        if(isEmpty()){ // Theta(1) Runtime
            System.out.println("Stack Underflow");}
        else{
            E e = head.element;
            head = head.next;
            return e;
        }      
        return null;
    }
    
    
    public E top() throws EmptyStackException{ //Same functionality as above, but does not remov elemtn from list
        if(isEmpty()){ //Theta(1) Runtime
            System.out.println("Stack underflow");           
        }
        else{
            return(head.element);
        }
        return null;
    }
    
    
}
