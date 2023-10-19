# python
# 列表解析

列表解析 双重for循环+条件判断

```
一个数如果恰好等于它的因子之和，这个数就称为“完数”。例如，6的因子为1、2、3，而6=1+2+3，因
此6是完数。编程，找出10000之内的所有完数，将其存入一个列表里
```

```
list1=[]

# n=6 求因子
# for i in range(1, n):
#     if n % i == 0:
#         print(i)
```

```python
for i in range(2,10001):
    sum = 0
    for j in range(1,i):
        if i%j==0:
            # print(i)
            sum+=j
    if (sum==i):
        list1.append(i)
print(list1)
```

尝试以列表解析的方式生成结果列表 

判断写成一个函数在列表调用

```python
def wdyinzi(i):
    sum=0
    for j in range(1, i):
        if i % j == 0:
            # print(i)
            sum += j
    if(sum==i):
        return  i
list2=[i for i in range(2,10001) if wdyinzi(i)]
print(list2)
```

