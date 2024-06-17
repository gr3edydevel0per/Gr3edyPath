Points to Remember
- Slow and fast pointer concept 
	- slowPointer = slowPointer.next  || fastPointer = fastPointer.next.next
	- when fast.next == null  at that point slow pointer is at middle of the list 4
	- The distance travelled by faster pointer is twice the distance travelled by slow pointer ::    D(fastPointer)  = 2 * D(slowPointer)
