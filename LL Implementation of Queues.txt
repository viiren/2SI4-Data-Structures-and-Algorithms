/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package queues;

/**
 *
 * @author virenwaghela
 */
public class Queue<E> {
    private Node<E> front;
    private Node<E> end;
    
    public Queue(){ //Constructor
        front = end = new Node<E>(null,null);
    }
    
    public int getSize(){//Theta(n)
        int size = 0;
        Node<E> p= head;
        while(p.next!=null){
            p=p.next;
            size++;
        }
        return size;
    }
    
    public boolean isEmpty(){
        return(front == end);
    }
    public void enqueue(E e){
        end.next = new Node<E>(e,null);
        end = end.next;
    }
    public E dequeue() throws EmptyQueueException{
        if(isEmpty()){
            System.out.println("Queue Underflow");
        }
        else{
            if(end==front.next)
                end = front;
            E val = front.next.element;
            front.next = front.next.next;
            return val;
        }
        
    }
    
    
}
