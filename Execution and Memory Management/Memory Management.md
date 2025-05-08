#### Stack Memory
- Stack memory is the one where the Reference Variable is created.
- The reference variable is a thing that is named to a piece of data.
- In this stack memory, all the variable names, function names, basically all the identifiers are stored that point towards a specific piece of data that is present in Heap Memory

#### Heap Memory
- Heap Memory is the place where the original data is stored.
- This original data is known as objects.
- So, if a reference variable 'a' is pointing to a value '10', then 10 is the object to that reference variable.

> [!NOTE]
> - Multiple reference variables can point to a single object.
> - If any changes are made in the Object of any reference variable, it'll be reflected to all the other variable pointing to the same object.


#### Garbage Collection
When an object does not have any reference varaible pointing to it, the data is removed by the garbage collector of the language. It is basically erased or removed from existence. :)