# vector_vs_list
Speed tests comparing a vector of pointers and intrusive list

This tests the time to iterate and add/remove elements in a vector/intrusive list. There are two vector tests: one normal vector of pointers to polymorphics objects, and another where the objects have an embedded index for quicker searching. All tests are also run sorted and unsorted.

Usage: vector_vs_list [-iters COUNT=1000] [-elems NUM=100000] [-add_rem NUM=100]

Results on Windows 7/Intel i3-2370M compiled with Visual Studio 2015:
```
Number times each test is run: 1000
Number elements in vectors/lists: 100000
Number elements to add/remove in a frame: 100

Iteration times(min, max, average) in ms:
Unsorted Vector of Pointers test: (11.61, 18.38, 13.61)
Sorted Vector of Pointers test: (11.15, 14.67, 11.59)
Unsorted Intrusive Vector of Pointers test: (11.29, 21.27, 13.21)
Sorted Intrusive Vector of Pointers test: (11.07, 14.06, 11.20)
Unsorted Intrusive List test: (11.16, 14.63, 12.55)
Sorted Intrusive List test: (11.07, 11.72, 11.17)

Add element times(min, max, average) in ms:
Unsorted Vector of Pointers test: (0.00, 0.00, 0.00)
Sorted Vector of Pointers test: (0.97, 2.84, 1.22)
Unsorted Intrusive Vector of Pointers test: (0.00, 0.00, 0.00)
Sorted Intrusive Vector of Pointers test: (6.09, 9.94, 7.72)
Unsorted Intrusive List test: (0.00, 0.00, 0.00)
Sorted Intrusive List test: (8.60, 13.00, 10.62)

Remove element times(min, max, average) in ms:
Unsorted Vector of Pointers test: (3.42, 6.85, 4.42)
Sorted Vector of Pointers test: (2.15, 4.60, 2.75)
Unsorted Intrusive Vector of Pointers test: (0.00, 0.06, 0.00)
Sorted Intrusive Vector of Pointers test: (12.01, 18.96, 15.28)
Unsorted Intrusive List test: (0.00, 0.02, 0.00)
Sorted Intrusive List test: (0.00, 0.01, 0.00)
```
Results on Windows 7/Intel i7-4770K compiled with Visual Studio 2015:
```
Number times each test is run: 1000
Number elements in vectors/lists: 100000
Number elements to add/remove in a frame: 100

Iteration times(min, max, average) in ms:
Unsorted Vector of Pointers test: (5.52, 7.08, 6.26)
Sorted Vector of Pointers test: (5.37, 9.70, 5.70)
Unsorted Intrusive Vector of Pointers test: (5.43, 12.89, 6.50)
Sorted Intrusive Vector of Pointers test: (5.40, 9.18, 5.67)
Unsorted Intrusive List test: (5.51, 9.86, 6.43)
Sorted Intrusive List test: (5.45, 7.47, 5.68)

Add element times(min, max, average) in ms:
Unsorted Vector of Pointers test: (0.00, 0.01, 0.00)
Sorted Vector of Pointers test: (0.53, 0.95, 0.69)
Unsorted Intrusive Vector of Pointers test: (0.00, 0.00, 0.00)
Sorted Intrusive Vector of Pointers test: (3.62, 5.52, 4.36)
Unsorted Intrusive List test: (0.00, 0.00, 0.00)
Sorted Intrusive List test: (5.12, 11.48, 6.51)

Remove element times(min, max, average) in ms:
Unsorted Vector of Pointers test: (1.10, 1.75, 1.36)
Sorted Vector of Pointers test: (0.52, 0.95, 0.66)
Unsorted Intrusive Vector of Pointers test: (0.00, 0.01, 0.00)
Sorted Intrusive Vector of Pointers test: (7.98, 13.92, 9.66)
Unsorted Intrusive List test: (0.00, 0.01, 0.00)
Sorted Intrusive List test: (0.00, 0.01, 0.00)
```
