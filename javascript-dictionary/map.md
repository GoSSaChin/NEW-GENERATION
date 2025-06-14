# `map`

### 개념

- 배열의 각 요소를 순회하며 콜백 함수를 실행하고, 그 결과를 모아 새로운 배열을 반환하는 배열 메서드
- 불변성을 유지하며, 원본 배열은 변경되지 않음

```js
const newArr = array.map((element, index, array) =>
  // 콜백함수
)
// element : 현재 요소, index : 현재 요소의 인덱스, array : 호출한 원본 배열
```

### 예시

1. 숫자 배열 제곱

```js
const numbers = [1, 2, 3, 4];
const squares = numbers.map((num) => num * num);
console.log(squares); // [1, 4, 9, 16]
```

2. 객체 배열에서 특정 속성 추출

```js
const users = [
  { id: 1, name: "Alice" },
  { id: 2, name: "Chris" },
];
const names = users.map((user) => user.name);
console.log(names); // ["Alice", "Chris"]
```

3. index 활용

```js
const arr = ["a", "b", "c"];
const indexed = arr.map((val, idx) => `${idx}: ${val}`);
console.log(indexed); // ["0: a", "1: b", "2: c"]
```

### 특징

- `map()`은 항상 원본 배열과 길이가 동일한 배열 반환
- `undefined`를 반환하면 `undefined`가 결과 배열의 요소
- 조건부 반환을 원한다면 `filter()`와 같이 사용 혹은 `map()`안에서 삼항 연산자 사용
- 중첩 구소에서는 `.map()`을 중첩하여 사용 가능
- 단순 순회를 위해서는 `forEach`를 사용하고, 반환값이 필요할 때 `map()`을 사용!
