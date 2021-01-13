# Stack
```java
Stack<Integer> stack = new Stack<>();
stack.push(1);
int value = stack.pop();
value = stack.peek();
stack.isEmpty();
stack.size();
```
# Queue
```java
Queue<Integer> queue = new LinkedList<>();
queue.offer(2);
value = queue.poll();
value = queue.peek();
queue.isEmpty();
queue.size();
```

# HashMap
```java
HashMap<Integer, String> hashmap = new HashMap<>();
hashmap.put(1, "a");
hashmap.getOrDefault(2, "b");
hashmap.containsKey(3);
hashmap.containsValue("a");
hashmap.size();
hashmap.remove(2);
Iterator iter = hashmap.entrySet().iterator();
while (iter.hasNext()) {
    Map.Entry mapElemnt = (Map.Entry) iter.next();
    mapElemnt.getKey();
    mapElemnt.getValue();
}
for (Integer k : hashmap.keySet()) {
    String value = hashmap.get(k);
}
```

# List
```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
int len = cars.length;
Integer[] arr = {1, 2, 3, 4, 5, 6};
List<String> carsList = Arrays.asList(cars);
len = carsList.size();
List<Integer> list = new ArrayList<>();
list.add(1);
list.contains(1);
list.get(0);
list.indexOf(1);
list.remove(0);
list.isEmpty();

List<List<Integer>> result = new ArrayList<>();
List<Integer> temp = new ArrayList<>();
result.add(new ArrayList<>(temp));
temp.add(1);
temp.remove(temp.size() - 1);
result.get(0).add(1);
```

# Sort
```java
Collections.sort(list);
Arrays.sort(cars);
Collections.sort(carsList, (c1, c2) -> c1.charAt(1) < c2.charAt(1) ? 1 : 0);
Collections.sort(carsList, Comparator.reverseOrder());
```

# Math
```java
int maxValue = Integer.MAX_VALUE;
int minValue = Integer.MIN_VALUE;
Integer a = -1;
Math.abs(a);
Math.pow(a, 2);
```

# String
```java
String s = "12345";
Integer sInt = Integer.valueOf(s);
s = sInt.toString();
s.toCharArray();
s.compareTo("123");
s.charAt(1);
s.indexOf("23");
s.substring(0, 2);
Strings.isNullOrEmpty(s);
s.split(" ");
s.split("\\.");
s.split(",");

StringBuilder sb = new StringBuilder();
sb.append("a");
sb.append("b");
sb.toString();
```

# Array
```java
Integer[][] dp = new Integer[3][5];
int[][] dirs = new int[][]{{-1, 0}, {0, -1}, {1, 0}, {0, 1}};
for (int[] d : dirs) {
    System.out.println(d[0]);
    System.out.println(d[1]);
}

int[] jobs = new int[]{1,2,3};
Integer[] jobsBoxed = Arrays.stream(jobs).boxed().toArray(Integer[]::new);
Arrays.sort(jobsBoxed, Comparator.reverseOrder());
jobs = Arrays.stream(jobsBoxed).mapToInt(Integer::intValue).toArray();
```

# Random
```java
Random r = new Random();
int rand_int = r.nextInt(100);
```


