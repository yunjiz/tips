# Golang

## Stack
```go
var stack []int
//push
stack = append(stack, 12)
//pop
v := stack[len(stack)-1]
stack = stack[:len(stack)-1]
//check
len(stack) == 0
```

## Queue
```go
var queue []int
//enqueue
queue=append(queue, 12)
//dequeue
v := queue[0]
queue = queue[1:]
//check
len(queue) == 0
```

Note
- the range is [ )
</br></br>

## HashMap
```go
hashMap := make(map[string]int)
m["hello"] = 1
delete(m,"hello")
for k,v := range m{
  //k is key
  //v is value
}
```
Note
- map key should be comparable, cannot be slice, map, function

## Sort
```go
sort.Intes([]int{})
sort.Strings([]string{})
sort.Slice(s, func(i,j int)bool{return s[i]<s[j})
```
## Math
```go
math.MaxInt32
math.MinInt32
math.MaxInt64
math.MinInt64
```
## Copy
```go
//delete a[i]
copy(a[i:], a[i+1:])
a=a[:len(a)-1]

a:=make([]int, n)
a[n] = x
var b []int
b = append(b,x)

numsSorted := make([]int, len(nums))
copy(numsSorted, nums)
sort.Ints(numsSorted)
```
## Convert
```go
s := "12345" //s[0] is byte
num := int(s[0]-'0') // int 1
str := string(s[0]) // string "1"
b := byte(num+'0') // byte '1'

num, _ := strconv.Atoi(str)
str := strconv.Itoa(num)
```

## String
```go
s := "12345"
var strArray []string
strArray = strings.Split(s,"")


var sb strings.Builder
for _, str := range strs {
  sb.WriteString(str)
}
return sb.String()

someString := "one    two   three four "
words := strings.Fields(someString)
fmt.Println(words, len(words)) // [one two three four] 4
```

## Pointer append
```go
func foo(result *[]string){
  *result = append(*result, "hello")
}
```

## DP
```go
dp := make([][]int, m)
for i := 0; i < m; i++ {
  dp[i] = make([]int, n)
}
```

