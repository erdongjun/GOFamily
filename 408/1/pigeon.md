# 鸽巢理论

核心思想就是让 arr[i] = i 也就是让每一个元素的arr[i]的值都等于自己，寻找的过程类似并查集。判断 for arr[i] != i,然后
i = arr[i],直到找到为止，然后最外层遍历每一个元素都让找到该有的位置，这样就OK了。

```go
for i := 0;i < len(arr);i++ {
  for arr[i] != i{
    i = arr[i]
  }
  if arr[i] ==i 
}
```
说白了其实就是寻找每一个并查集的大boss，然后寻找到以后也不用合并了，各自到各自的位置就可以了。