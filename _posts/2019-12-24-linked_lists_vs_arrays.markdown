---
layout: post
title:      "Linked Lists "
date:       2019-12-24 21:58:53 -0500
permalink:  linked_lists_vs_arrays
---


**Linked Lists And Common fucntions**


The main difference from an Array is that Linked Lists are not indexed.
The Linked List doesn’t hold a reference to all the items that it stores, it usually only contains references to its head (first element) and/or tail (last item). Each item of the Linked List is responsible for storing a reference to the next and previous element of the list.

**# Adding/removing items is usually faster**
Adding and removing items from a non-indexed list is usually faster since it doesn’t need to rebuild the index every time the items change, it just needs to update the references to the next and/or previous element.

**# Iteration can be slower**

The lack of an index and the simple structure can be a drawback since you can’t skip to a certain position on the list some operations will require iterating over most or all of the list elements. 


**# Creating a Linked List**
```
class Node{
    constructor(val){
        this.val = val 
        this.next = null 
    }
}

class SinglyLinkedList{
    constructor(){
        this.head = null
        this.tail = null
        this.length = 0 
    }
```
		
		
**# Adding item to end of a Linked List**
```
push(val){

		 let newNode = new Node(val)

		if(this.head == null){
				this.head = newNode
				this.tail = newNode
		} else{
				this.tail.next = newNode
				this.tail = newNode
		}
		this.length += 1   
		return this 
}
```
**#    Removing last item in a Linked List**
```
pop(){
		if(this.head == null){
				return undefined
		}

		let temp = this.head
		let pop = temp

		while(temp.next){
				pop = temp
				temp = pop.next
		}
		this.tail = pop;
		this.tail.next = null;
		this.length--;
		return pop
}

```
# `Adding and item to the beginnong of a Linked List`

    unshift(val){
        let newNode = new Node(val)
        let currentHead = this.head
         if(this.head == null){
            this.head = newNode
            this.tail = newNode
            }else{
                this.head = newNode
                this.head.next = currentHead
            }
            this.length += 1
            return this
    }
**# Removing item from the beginning of a Linked List**
```
shift(){

		if(this.head == null){
				return undefined
		}

		let shifted = this.head.val

		this.head = this.head.next

		this.length--

		 if( this.length === 0 ){
				this.tail = null
		}

		return shifted

}

```

**# Finding Items in a Linked List**

```
get(id){
		if(id< 0 || id >= this.length){
				return null
		}
		let i = 0
		let current = this.head 
		while(i > id){
				current = current.next
				i++
		}
		return current

}

```

**# Inserting into A linked List**

```
insert(id, value){
		if(id < 0 || id > this.length){
				return false 
		}

		if(id == this.length){
				push(value)
				return true
		}

		if (id == 0){
				unshift(value)
				return true 
		}

		let old = this.get(id - 1)
		let current = this.get(id)
		let newNode = new Node(value)
		old.next = newNode
		newNode.next = current
		this.length++
		return true
}
```
**# Removing items in a Linked List**
```
remove(id){
		if(id < 0 || id >= this.length){
				return undefined
		}

		if(id == this.length - 1){
				return this.pop()
		}

		if (id == 0){
				return this.shift()
		}

		let old = this.get(id - 1)
		let current = this.get(id)
		let temp = this.get(id + 1)
		old.next = temp
		this.length--
		return current

}

```


   


