# javascript 특징


1. 변수의 타입이 정의되지 않음
``` javascript
// 변수에 어떠한 탑의 값을 넣을수있다
var a = 1
console.log(a)

a = "진용화"  //정수를 담았던 배열에 문자열을 담아도 문제가 없음
console.log(a)

//변수에 함수를 담을수도 있다
a = function () {
    console.log('이것은 변수에 할당된 함수')
}

a() 
```
2. 자유로운 Object,Array 형태
``` javascript
var person = {
    firstName: "용화",
    lastName: "진"
}
console.log(person.firstName + " " + person.lastName)
```

``` javascript
var arr = []
var person = {
    firstName: "용화",
    lastName: "진"
}

function test() {
    console.log("이것은 test함수")
}

arr.push(test)
arr.push(person)

arr[0]()
console.log(arr[1])
```


3. Non-block
``` javascript
console.log("나는")
setTimeout(function () {
    console.log("진용화")
}, 1000)
console.log("입니다")

```
