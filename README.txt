Student: Sandra Soza Zambrano
COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		No, there is no difference using a LinkedList, only performance varies. 

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			It removes the object located at index 5 in the list. 

		list.remove(Integer.valueOf(5)); // what does this one do?

			It removes the object with the value 5 in the list. 

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			The iterator will skip elements in the list because after removal the elements will shift to the left. This is a problem
			because after changing positions, the iterator won't delete the remaining 77s in the list. 

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  45ms 45ms 44ms 77ms 68ms 81ms  ... (fill these in in ms)
        testLinkedListAddRemove: 65ms 73ms 62ms 36ms 37ms 59ms
	    testArrayListAccess:     15ms 19ms 22ms 18ms 26ms 47ms
        testLinkedListAccess:    27ms 26ms 37ms 23ms 33ms 39ms

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  90ms 66ms 118ms 85ms 77ms 77ms  ... (fill these in in ms)
        testLinkedListAddRemove: 39ms 59ms 35ms 63ms 43ms 33ms
	    testArrayListAccess:     17ms 15ms 27ms 24ms 24ms 30ms
        testLinkedListAccess:    50ms 53ms 54ms 49ms 34ms 57ms

	SIZE 1000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  192ms 153ms 169ms 164ms 191ms 167ms  ... (fill these in in ms)
        testLinkedListAddRemove: 63ms 56ms 51ms 83ms 49ms 51ms
	    testArrayListAccess:     24ms 22ms 17ms 24ms 24ms 22ms
        testLinkedListAccess:    383ms 360ms 384ms 388ms 399ms 377ms

	SIZE 10000
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  464ms 214ms 247ms 457ms 561ms 443ms ... (fill these in in ms)
        testLinkedListAddRemove: 39ms 41ms 46ms 49ms 42ms 42ms
	    testArrayListAccess:     19ms 18ms 20ms 24ms 19ms 24ms
        testLinkedListAccess:    4sec,170ms 4sec,91ms 4sec,139ms 4sec,229ms 4sec,207ms 4sec,278ms

	listAccess - which type of List is better to use, and why?

		ArrayList because it provides instant access to elements O(1). LinkedList traverses the list n number of times O(n) --> less efficient.

	listAddRemove - which type of List is better to use, and why?

		LinkedList because nodes can be easily readjusted to point to other elements, making adding and removing nodes cost-efficient O(1) --> efficient. In contrast, after
		removing the element at index 0, ArrayLists require shifting the elements to the left O(n) --> less efficient.
