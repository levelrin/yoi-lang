# Loop

## Loop with index

```yoi
loop, do with index
  from: 0
  to: 3
  do:
    with index (int)
    cli, print
      message: index
```

This will print the following:
```
0
1
2
3
```

## Loop with condition

```yoi
num (int)
  value: 0

loop, do until yes
  question: num, are you greater than value?
    value: 3
  do:
    cli, print
      message: num
    num, increment yourself  
```

The above will print the following:
```
0
1
2
3
```
