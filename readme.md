# javascript 특징


1. 동적 타입이 가능하다
``` javascript
// 변수에 어떠한 타입의 값을 넣을수있다
var a = 1
console.log(a)

a = "진용화"  //정수를 담았던 배열에 문자열을 담아도 문제가 없음
console.log(a)

//변수에 함수를 담을수도 있다
a = function () {
    console.log('이것은 변수에 할당된 함수')
}

a()

//함수를 다른 변수에 할당 할 수도 있다
var b = a
b()
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

arr.push(test)    //배열에 함수를 담을수있음
arr.push(person)    //하나의 배열에 다른 타입의 데이터를 담을수있음


console.log(arr)
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


### axios 를 이용하여 외부 api 호출하기
``` sh
npm install axios
```

``` javascript
var axios = require('axios')

console.log("URL 가져오기")
axios("http://ip.jsontest.com")
    .then(response => {
        console.log(response.data)
    })

console.log("완료")

```
### async/await
```
var axios = require('axios')

async function getUrl() {
    console.log("URL 가져오기")
    var response = await axios("http://ip.jsontest.com")
    console.log(response.data)
    console.log("완료")
}
getUrl()
```
