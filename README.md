An example using Python code


```
def sum(n):
    ret = 0
    for i in range(1, n+1):
    	ret+=i
    return ret
sum(100)
```    


The codes above can be rewritten in this language as


```
def (@1):
    /0/ _0+1
    /0/ _0+_1
    if _2<(@1+1): goto _2
    return _2
_5(100)
```

Here is another example, which calculates fibonacci sequence iteratively

```
def fibIter(n):
    if n < 2:
        return n
    fibPrev = 1
    fib = 1
    for num in xrange(2, n):
        fibPrev, fib = fib, fib + fibPrev
    return fib
```    

This example can be rewritten like this:

```
def (@1):
    if @1 < 2:
        return @1
    /1/ _0+1
    /1/ |1 # temp
	/1/ _1 + _0 # fib
	_2 # fibPrev
	if _4<(@1) goto _4
    return _3
```    

The syntax looks very weird and awkward, but it's quite simple actually. Most line is an expression. `_1` means to replace itself with the value of the expression in ONE line above. `_2` means to replace with that in TWO lines above. `|1` means to replace with that in ONE line below. The codes are evaulated line by line from top to down. If a line is not evaluated but used, it returns its default value, which locates within the `//`. 
