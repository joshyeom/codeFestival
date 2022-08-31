---
# 문제 8

작성날짜: 2022년 8월 31일 오후 12:48

```jsx
# 문제8 : 객체의 키 이름 중복

자바스크립트 객체를 다음과 같이 만들었다. 
출력값을 입력하시오. (출력값은 공백을 넣지 않습니다. )

var d = {
    'height':180,
    'weight':78,
    'weight':84,
    'temperature':36,
    'eyesight':1
};

console.log(d['weight']);
```

```jsx
유추)
'weight'객체가 2개 있다. 객체값은 2개 이상 될 수 있으므로 2가지 모두 출력한다.

정답) 78, 84
```

```jsx
정답)
정답은 '84' 입니다.
```

# 추가 정보)

- **객체 내에서 key는 중복될 수 없기 때문에 마지막 뒤에 있는 key의 값이 나온다.**
- **중복되는 키의 경우, 초기의 값을 사용합니다.**

### `[Set` 객체 사용](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Set#set_%EA%B0%9D%EC%B2%B4_%EC%82%AC%EC%9A%A9)

```jsx
var mySet = new Set();

mySet.add(1); // Set { 1 }
mySet.add(5); // Set { 1, 5 }
mySet.add(5); // Set { 1, 5 }
mySet.add('some text'); // Set { 1, 5, 'some text' }
var o = {a: 1, b: 2};
mySet.add(o);

mySet.add({a: 1, b: 2}); // o와 다른 객체를 참조하므로 괜찮음

mySet.has(1); // true
mySet.has(3); // false, 3은 set에 추가되지 않았음
mySet.has(5);              // true
mySet.has(Math.sqrt(25));  // true
mySet.has('Some Text'.toLowerCase()); // true
mySet.has(o); // true

mySet.size; // 5

mySet.delete(5); // set에서 5를 제거함
mySet.has(5);    // false, 5가 제거되었음

mySet.size; // 4, 방금 값을 하나 제거했음
console.log(mySet);// Set {1, "some text", Object {a: 1, b: 2}, Object {a: 1, b: 2}}
```

`set` 객체를 사용함으로써, 중복되는 키가 나오지 않게할 수 있고, 확인, 삭제도 가능.

---

그…그렇군… 객체가 중복될 시, 마지막 값을 출력.
