#### Given
- Start - $S$
- End - $E$
- Middle - $M$
- Target - $T$

#### Steps
1. Sort the array. Store the target element in $T$.
2. Store the first element in $F$ and last element in $E$.
3. Find the middle element and store it in $M$.
4. If 
	   $T$ = $M$, element found,
	   $T$ > $M$, search in right part
	   $T$ < $M$, search in left part.
5. Repeat until element is found.