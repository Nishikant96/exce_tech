Question 1
Define an array of numbers (use any random numbers). Write a program to print only the even numbers of the array. Do not use any library functions, need to do via for loops only

```
let arr=[1,2,3,4,5,6,7,8,9,10,11]

for(let i=0;i<arr.length;i=i+2){
    console.log(arr[i]);
}
```

---

Question 2
Find the maximum consecutive 1's in an array of 0's and 1's.
Example:
a) 00110001001110 - Output :3 [Max num of consecutive 1's is 3]
b) 1000010001 - Output :1 [Max num of consecutive 1's is 1]

```
var arr=[1,0,1,1,1,0,1,0,0,1,1,1,1,1,1]
let max=0,curMax=0;
for(let i=0;i<arr.length;i++){
if(arr[i]===0){
  curMax=0;
}
else{
  curMax++;
  if(curMax>max)
  max=curMax;
}
}
console.log(max);
```

---

Question 3
Suppose you have an array of 101 integers. This array is already sorted and all numbers in this array are consecutive. Each number only occurs once in the array except one number which occurs twice. Write a js code to find the repeated number.
e.g $arr = array(0,1,2,3,4,5,6,7,7,8,9,10...................);

```
let arr=[0,1,2,3,4,5,6,7,7,8,9,10]
let ans=0;
for (let i=0;i<arr.length;i++){
  if(arr[i]!=arr[0]+i){
    ans=arr[i];
    break;
  }
}

console.log(ans);
```

---

Question 4
Let’s see we an api url https://my-json-server.typicode.com/typicode/demo/posts
Write a sample code to call this rest api and display the result.

```

async function fetchAPI() {
const answer = await fetch(
"https://my-json-server.typicode.com/typicode/demo/posts"
).then((res) => res.json());
console.log(answer);
}
fetchAPI();
```

---

Question 5
Assume there is a object of this format
var obj = {
“id” : 4, “name” : “abc”,
“id” : 10, “name” : “ab2”,
“id” : 5, “name” : “abc3”,
“id” : 6, “name” : “abc5”
}
It can be a dictionary or java object, as per your language of choice. But its key/value pair dictionary simply.

Write a code to sort the object by id
I.e final output should have objected sort by id’s

```
var obj = {
      4: "abc",
      10 : "ab2",
      5: "abc3",
      6: "abc5"
      }
var arr=[];
for(var key in obj)
arr.push(key);
arr.sort;

var newObj={};
for(let i=0;i<arr.length;i++)
newObj[arr[i]]=obj[arr[i]];

console.log(newObj);
```
