# Python tricks

## Sorting a dictionary by value in Python

{key: value for key, value in sorted(x.items(), key=lambda item: item[1])}

dict(sorted(x.items(), key=lambda item: item[1]))

## Heap
Definition: Heaps are binary trees for which every parent node has a value less than or equal to any of its children. 

[Heap Docs](https://docs.python.org/3/library/heapq.html)

    def heapsort(iterable):
        h = []
        for value in iterable:
            heappush(h, value)
        return [heappop(h) for i in range(len(h))]
        
    >>> h = []
    >>> heappush(h, (5, 'write code'))
    >>> heappush(h, (7, 'release product'))
    >>> heappush(h, (1, 'write spec'))
    >>> heappush(h, (3, 'create tests'))
    >>> heappop(h)
    (1, 'write spec')
    
## Queue

    from collections import deque
    d = deque([1,2,3])
    d.pop()
    d.popleft()
    d.append(2)
    d.appendleft()
    
## Counter

    Counter('abracadabra').most_common(3)
    [('a', 5), ('b', 2), ('r', 2)]
    
## sorted()    
The sorted() function sorts the elements of a given iterable in a specific order (ascending or descending) and returns it as a list.

    sorted(iterable, key=None, reverse=False)
    
    # take the second element for sort
    def take_second(elem):
        return elem[1]


    # random list
    random = [(2, 2), (3, 4), (4, 1), (1, 3)]

    # sort list with key
    sorted_list = sorted(random, key=take_second)

    # print list
    print('Sorted list:', sorted_list)
    
    # Output
    Sorted list: [(4, 1), (2, 2), (1, 3), (3, 4)]
    
    # with lambda function
    sorted(intervals, key = lambda x:x[0])
