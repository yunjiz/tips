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

//2 ways of sort string
sBytes := []byte(s)
sort.Slice(sBytes, func(i int, j int) bool { return sBytes[i] < sBytes[j] })
s = string(sBytes)

tStrings := strings.Split(t, "")
sort.Strings(tStrings)
t = strings.Join(tStrings, "")

// reverse sort
nums := []int{2,1,5,4,6,4}
sort.Sort(sort.Reverse(sort.IntSlice(nums)))

// sort.Slice
sort.Slice(intervals, func(i,j int)bool{
        if intervals[i][0] < intervals[j][0]{
            return true
        }
        if intervals[i][0] == intervals[j][0]{
            return intervals[i][1] < intervals[j][1]
        }
        return false
    })
```
## Math
```go
math.MaxInt32
math.MinInt32
math.MaxInt64
math.MinInt64

int(math.Pow(float64(26), float64(exp)))
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

## Random
```
//rand.Intn returns a random int n, 0 <= n < 100.
//rand.Float64 returns a float64 f, 0.0 <= f < 1.0.
rand.Intn(100)
rand.Float64()
```
# Array
```
direct := [][]int{{0,1},{1,0},{0,-1},{-1,0}}
```
Passed by the value of reference
```go
func main() {
	nums := []int{1,2,3,4}
	changeSlice(nums)
	fmt.Println(nums)
	nums = []int{1,2,3,4}
	changeSlice2(&nums)
	fmt.Println(nums)
}

func changeSlice(nums []int){
	nums[0] = 5
	nums[1] = 6
	nums[2] = 7
	nums[3] = 8
	nums = append(nums, 9)
	nums[0] = 0
	nums[1] = 0
	nums[2] = 0
	nums[3] = 0
}

func changeSlice2(nums *[]int){
	*nums = append(*nums, 9)
	(*nums)[0] = 0
	(*nums)[1] = 0
	(*nums)[2] = 0
	(*nums)[3] = 0
}

//output is
[5 6 7 8]
[0 0 0 0 9]
```
