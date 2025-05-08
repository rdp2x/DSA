- The case where we don't know if the array is in ascending order or descending order.
- To figure this out, first we compare the first and last element of the array.
- If the **start** is greater then **end** element, the array is in descending order.

The change in code we make is:
	Target > Middle Element, search in left part
	Target < Middle Element, search in right part.