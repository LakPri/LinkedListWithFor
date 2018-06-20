import Foundation 


print("Hello World")

//Linked List

class Node{
    let value: Int
    var next: Node?
    var prev: Node?
    
    init(value:Int, next:Node?, prev:Node?){
        self.value = value
        self.next = next
        self.prev = prev
    }
}

let numberArray =  [5,3,2,4,1]
var curentnode:Node?
var previousNode:Node? = nil

for valuenumber in numberArray {
  
  curentnode =  Node(value: valuenumber, next: nil, prev: previousNode)
  if previousNode != nil{
     previousNode?.next = curentnode
  }
  previousNode = curentnode

 // print(nodes?.value)
}

/*
//Adding first object
let oneNode = Node(value: 1, next: nil, prev:nil)

//Adding second object
let secondNode = Node(value: 2, next: nil, prev: oneNode)
oneNode.next = secondNode

//Adding third object
let thirdNode = Node(value: 3, next: nil, prev: secondNode)
secondNode.next = thirdNode
*/

/*func printNodes(head:Node?){
    var currentNode = head
    while currentNode != nil {
        print(currentNode?.value)
        currentNode = currentNode?.next
    }
}
printNodes(head: oneNode)*/


func printNodesFromLast(head:Node?){
    var currentNode = head
    while currentNode != nil {
        print(currentNode?.value)
        currentNode = currentNode?.prev
    }
}
printNodesFromLast(head: curentnode)
