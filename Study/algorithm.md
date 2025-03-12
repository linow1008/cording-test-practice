🔖 JavaScript 자료구조 및 알고리즘 학습 목차
📚 PART 1. 자료구조 기초
1️⃣ 자료구조와 알고리즘 개요

📌 1. 자료구조의 정의 및 필요성

자료구조란 무엇인가?

자료구조(Data Structure) 는 컴퓨터에서 데이터를 효율적으로 저장하고 관리하며 활용하기 위한 구조를 의미합니다. 자료구조를 활용하면 데이터를 빠르게 탐색하고 수정할 수 있으며, 애플리케이션의 성능 향상에 크게 기여합니다.

자료구조의 필요성

데이터를 효율적으로 저장하고 관리할 수 있습니다.

메모리 공간의 낭비를 최소화할 수 있습니다.

알고리즘의 성능을 최적화할 수 있습니다.

코드의 가독성 및 유지보수가 쉬워집니다.

JavaScript로 보는 자료구조 예시

// 배열(Array): 데이터를 순차적으로 저장
const array = [1, 2, 3, 4];

// 객체(Object): 키-값 쌍으로 데이터를 저장
const object = { name: "Alice", age: 30 };

// 집합(Set): 중복 없는 데이터의 집합
const set = new Set([1, 2, 3, 2, 1]); // 결과: Set {1, 2, 3}

// 맵(Map): 키-값 쌍을 보다 유연하게 관리
const map = new Map();
map.set('name', 'Alice');
map.set('age', 30);

📌 2. 알고리즘의 정의 및 특성

알고리즘이란 무엇인가?

알고리즘(Algorithm) 은 특정 문제를 해결하거나 작업을 수행하기 위해 정의된 일련의 절차 또는 규칙입니다. 알고리즘은 입력(input)을 받아 명확한 과정을 거쳐 출력(output)을 생성합니다.

알고리즘의 필수 특성

명확성: 모든 단계가 명확하고 모호하지 않아야 합니다.

유한성: 반드시 끝이 나야 하며 무한히 반복되지 않아야 합니다.

입력/출력 명확성: 명확한 입력과 출력이 있어야 합니다.

효율성: 최소 자원을 사용하여 최대 성능을 내야 합니다.

JavaScript로 보는 알고리즘 예시

// 단순 합산 알고리즘
function sum(arr) {
  let total = 0;
  for (let num of arr) {
    total += num;
  }
  return total;
}

console.log(sum([1,2,3,4])); // 출력: 10

📌 3. 성능 분석 방법 (Big-O, Big-Ω, Big-Θ)

알고리즘의 성능은 시간복잡도(Time Complexity)와 공간복잡도(Space Complexity)로 평가됩니다.

시간복잡도 표기법

Big-O 표기법 (상한): 최악의 경우를 평가할 때 사용됩니다.

Big-Ω 표기법 (하한): 최선의 경우를 평가할 때 사용됩니다.

Big-Θ 표기법 (정확한 복잡도): 평균적이고 정확한 성능을 나타낼 때 사용됩니다.

JavaScript 예시로 보는 성능 분석

// 배열의 모든 요소를 합산하는 함수
function sumArray(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}

위 알고리즘의 시간복잡도는 배열 크기 n에 비례하므로 O(n) 입니다.

📌 4. 최선, 평균, 최악의 경우 이해하기

알고리즘은 실행 조건에 따라 성능이 달라집니다. 이를 크게 다음 세 가지로 나눕니다.

최선의 경우(Best Case)

알고리즘이 가장 빠르게 동작할 때

예시: 정렬된 배열에서 원하는 값을 바로 찾는 경우

평균적인 경우(Average Case)

알고리즘이 일반적으로 수행하는 속도

예시: 배열 내에서 랜덤하게 원하는 값을 찾는 경우

최악의 경우(Worst Case)

알고리즘이 가장 느리게 동작할 때

예시: 원하는 값이 배열의 마지막에 있거나 없는 경우

JavaScript로 보는 예시

// 선형 탐색 알고리즘
function linearSearch(arr, target) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === target) return i;
  }
  return -1;
}

최선의 경우: O(1) → 찾는 값이 배열의 맨 앞에 있는 경우

평균의 경우: O(n/2) → 평균적으로 배열의 중간쯤에 값이 있을 때

최악의 경우: O(n) → 찾는 값이 마지막 요소이거나 배열에 없을 때



2️⃣ JavaScript 기본 구조 복습

# 📖 JavaScript 기본 구조 복습

## 📌 1장. ES6+ 핵심 문법

### 1. 변수 선언 방식: `let`과 `const`

#### 🔹 `let`
- ES6에서 도입된 블록 스코프(block-scope)를 가진 변수 선언 방식입니다.
- 재할당 가능, 재선언 불가능

```javascript
let message = "Hello, World!";
message = "Hi!"; // 재할당 가능
// let message = "New Message"; // 재선언 불가능 (에러 발생)
```

#### 🔹 `const`
- 블록 스코프이며 상수(constant) 값을 위한 선언 방식입니다.
- 선언과 동시에 반드시 초기화가 필요하며, 이후 값 변경 불가능

```javascript
const PI = 3.14159;
// PI = 3.14; // 에러 발생 (재할당 불가능)
```

> ⚠️ 주의: 객체나 배열을 `const`로 선언했을 때, 객체의 프로퍼티나 배열의 요소 변경은 가능합니다. 단, 객체 자체를 재할당하는 건 불가능합니다.

```javascript
const user = { name: "Alice" };
user.name = "Bob"; // 가능
// user = { name: "Charlie" }; // 에러 발생 (재할당 불가능)
```

### 2. 화살표 함수 (Arrow Functions)

#### 🔹 기본 형태
- ES6에서 함수 표현을 간단히 나타낼 때 사용됩니다.

```javascript
const add = (a, b) => a + b;
console.log(add(1, 2)); // 출력: 3
```

#### 🔹 특징
- 자신의 `this`를 가지지 않고, 부모 스코프의 `this`를 상속받습니다.
- 간결한 표현으로 가독성을 높여줍니다.

```javascript
const numbers = [1, 2, 3];
const squares = numbers.map(n => n * n);
console.log(squares); // [1, 4, 9]
```

### 3. 클래스 (Class)

#### 🔹 기본 구조
- 객체 지향 프로그래밍(OOP)을 위한 클래스 기반 문법입니다.

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello, ${this.name}!`);
  }
}

const alice = new Person("Alice");
alice.greet(); // 출력: Hello, Alice!
```

#### 🔹 상속
- 클래스의 기능을 확장하거나 재사용할 때 사용됩니다.

```javascript
class Student extends Person {
  constructor(name, studentId) {
    super(name);
    this.studentId = studentId;
  }

  showInfo() {
    console.log(`${this.name}, Student ID: ${this.studentId}`);
  }
}

const student = new Student("Bob", 123);
student.greet(); // Hello, Bob!
student.showInfo(); // Bob, Student ID: 123
```

---

## 📌 2장. 내장 자료구조

### 1. 배열 (Array)

- 데이터를 순서대로 저장하는 자료구조로 인덱스를 통해 접근합니다.

```javascript
const fruits = ["Apple", "Banana", "Cherry"];
fruits.push("Date"); // 배열 뒤에 추가
fruits.pop(); // 마지막 요소 제거

fruits.forEach((fruit, index) => console.log(index, fruit));
```

#### 유용한 메서드들
- `map()`, `filter()`, `reduce()`, `find()`, `includes()`

```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(n => n % 2 === 0); // [2,4]
const sum = numbers.reduce((acc, curr) => acc + curr, 0); // 15
```

### 2. 객체 (Object)

- 키-값(key-value) 쌍으로 데이터를 저장하는 자료구조입니다.

```javascript
const user = {
  name: "Charlie",
  age: 25,
  "favorite food": "Pizza"
};

console.log(user.name); // Charlie
console.log(user["favorite food"]); // Pizza

// 객체 프로퍼티 순회
for (let key in user) {
  console.log(`${key}: ${user[key]}`);
}
```

### 3. Set

- 중복되지 않는 유일한 값들의 집합입니다.

```javascript
const set = new Set([1, 2, 3, 2, 1]);
console.log(set); // Set { 1, 2, 3 }

set.add(4);
set.delete(2);
console.log(set.has(3)); // true
```

### 4. Map

- 키-값 쌍을 저장하며 키로 모든 데이터 유형 사용이 가능한 자료구조입니다.

```javascript
const map = new Map();
map.set("name", "David");
map.set(123, "numeric key");

console.log(map.get("name")); // David
console.log(map.size); // 2

// Map 순회
map.forEach((value, key) => console.log(`${key}: ${value}`));
```

---

## 📝 요약 정리
- **let, const**: 블록 스코프 변수 선언
- **화살표 함수**: 간결한 함수 표현
- **클래스**: 객체지향적 프로그래밍
- **배열**: 순서 있는 데이터 구조
- **객체**: 키-값 쌍 구조
- **Set**: 중복 허용하지 않는 데이터 구조
- **Map**: 다양한 자료형의 키 사용 가능한 데이터 구조

이 기본 문법과 자료구조는 JavaScript 프로그래밍에서 필수적으로 자주 사용되므로 반드시 숙지하시길 권장합니다.



3️⃣ 배열(Array)

# 📖 JavaScript 배열(Array) 완벽 가이드

## 📌 1장. 배열 기본 연산

### 🔹 `push()` & `pop()`
- 배열의 끝에 요소 추가 및 제거

```javascript
let numbers = [1, 2, 3];
numbers.push(4); // [1, 2, 3, 4]
numbers.pop();   // [1, 2, 3]
```

### 🔹 `shift()` & `unshift()`
- 배열의 시작 부분에서 요소 제거 및 추가

```javascript
let colors = ['red', 'blue'];
colors.unshift('green'); // ['green', 'red', 'blue']
colors.shift();          // ['red', 'blue']
```

### 🔹 `splice()`
- 배열의 특정 위치에서 요소 추가, 삭제, 교체 가능

```javascript
let fruits = ['apple', 'banana', 'cherry'];
fruits.splice(1, 1, 'blueberry'); // ['apple', 'blueberry', 'cherry']
```

### 🔹 `slice()`
- 기존 배열을 건드리지 않고 새로운 배열 반환

```javascript
let original = [1, 2, 3, 4, 5];
let sliced = original.slice(1, 3); // [2, 3]
```

## 📌 2장. 배열을 이용한 선형 자료구조

### 🔹 스택(Stack) 구현
- 후입선출(LIFO) 구조

```javascript
class Stack {
  constructor() {
    this.stack = [];
  }

  push(item) {
    this.stack.push(item);
  }

  pop() {
    return this.stack.pop();
  }

  peek() {
    return this.stack[this.stack.length - 1];
  }

  isEmpty() {
    return this.stack.length === 0;
  }
}
```

### 🔹 큐(Queue) 구현
- 선입선출(FIFO) 구조

```javascript
class Queue {
  constructor() {
    this.queue = [];
  }

  enqueue(item) {
    this.queue.push(item);
  }

  dequeue() {
    return this.queue.shift();
  }

  front() {
    return this.queue[0];
  }

  isEmpty() {
    return this.queue.length === 0;
  }
}
```

## 📌 3장. 다차원 배열 관리하기

### 🔹 2차원 배열

```javascript
let matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

// 요소 접근
console.log(matrix[1][2]); // 6

// 요소 추가
matrix[0].push(4); // [1, 2, 3, 4]
```

### 🔹 다차원 배열 순회하기

```javascript
matrix.forEach(row => {
  row.forEach(element => {
    console.log(element);
  });
});
```

## 📌 4장. 배열 메서드 성능 분석 및 개선

### 🔹 성능 분석
- `push()`와 `pop()`은 O(1)의 빠른 성능 제공
- `shift()`와 `unshift()`는 배열의 모든 요소를 재배치하므로 O(n)의 성능 저하
- `splice()`도 요소가 많으면 성능 하락

```javascript
// shift() vs pop()
const bigArray = Array(100000).fill(0);

console.time('shift');
bigArray.shift();
console.timeEnd('shift');

console.time('pop');
bigArray.pop();
console.timeEnd('pop');
```

### 🔹 개선점 및 권장사항
- 큰 배열의 맨 앞 요소를 자주 추가/제거할 경우 `Queue`는 배열 대신 연결리스트(linked list)로 구현하는 것이 좋습니다.
- 배열의 중간 요소를 자주 변경해야 한다면 데이터 구조를 재설계하거나, 변경을 최소화하여 성능 최적화를 진행해야 합니다.

---

## 📝 정리 및 요약
- 기본 연산(`push`, `pop`, `shift`, `unshift`, `splice`, `slice`)을 잘 이해하고 상황에 맞는 연산 선택
- 선형 자료구조(스택, 큐) 구현을 통해 배열의 활용도를 높일 수 있습니다.
- 다차원 배열은 행렬(matrix) 형태의 데이터를 관리할 때 매우 유용
- 배열 연산 성능을 고려하여 효율적인 데이터 구조 설계 필요

이 가이드를 통해 배열의 심층적인 이해와 효율적인 사용 방법을 숙지하시길 바랍니다.






4️⃣ 연결 리스트(Linked List)

# 📖 JavaScript 연결 리스트(Linked List) 완벽 가이드

## 📌 1장. 연결 리스트의 필요성 및 특징

### 🔹 필요성
- 배열은 크기 변경 시 성능이 저하되는 단점이 있습니다.
- 연결 리스트는 메모리를 효율적으로 사용하며, 크기 변경 시 유연하게 대처할 수 있습니다.

### 🔹 특징
- 메모리 상에서 비연속적으로 저장됩니다.
- 포인터(참조)를 통해 노드를 연결하여 관리합니다.
- 삽입 및 삭제 연산의 성능이 우수합니다.

## 📌 2장. 단일 연결 리스트 (Singly Linked List)

### 🔹 구조
- 각 노드는 데이터와 다음 노드를 가리키는 참조를 가집니다.

```javascript
class Node {
  constructor(data) {
    this.data = data;
    this.next = null;
  }
}

class SinglyLinkedList {
  constructor() {
    this.head = null;
  }

  append(data) {
    const newNode = new Node(data);
    if (!this.head) {
      this.head = newNode;
      return;
    }

    let current = this.head;
    while (current.next) {
      current = current.next;
    }
    current.next = newNode;
  }

  delete(data) {
    if (!this.head) return;

    if (this.head.data === data) {
      this.head = this.head.next;
      return;
    }

    let current = this.head;
    while (current.next && current.next.data !== data) {
      current = current.next;
    }

    if (current.next) {
      current.next = current.next.next;
    }
  }
}
```

## 📌 3장. 이중 연결 리스트 (Doubly Linked List)

### 🔹 구조
- 각 노드는 이전과 다음 노드를 가리키는 두 개의 참조를 가집니다.

```javascript
class DoublyNode {
  constructor(data) {
    this.data = data;
    this.prev = null;
    this.next = null;
  }
}

class DoublyLinkedList {
  constructor() {
    this.head = null;
    this.tail = null;
  }

  append(data) {
    const newNode = new DoublyNode(data);

    if (!this.head) {
      this.head = newNode;
      this.tail = newNode;
      return;
    }

    this.tail.next = newNode;
    newNode.prev = this.tail;
    this.tail = newNode;
  }

  delete(data) {
    let current = this.head;

    while (current && current.data !== data) {
      current = current.next;
    }

    if (!current) return;

    if (current.prev) {
      current.prev.next = current.next;
    } else {
      this.head = current.next;
    }

    if (current.next) {
      current.next.prev = current.prev;
    } else {
      this.tail = current.prev;
    }
  }
}
```

## 📌 4장. 환형 연결 리스트 (Circular Linked List)

### 🔹 개념
- 마지막 노드가 첫 번째 노드를 가리켜 원형 구조를 형성합니다.
- 순환구조가 필요할 때 주로 활용됩니다. (예: 라운드로빈 스케줄링)

### 🔹 활용 예시
- 음악 플레이리스트
- 라운드 로빈 방식의 작업 스케줄러

```javascript
class CircularLinkedList {
  constructor() {
    this.head = null;
  }

  append(data) {
    const newNode = new Node(data);

    if (!this.head) {
      this.head = newNode;
      newNode.next = this.head;
      return;
    }

    let current = this.head;
    while (current.next !== this.head) {
      current = current.next;
    }

    current.next = newNode;
    newNode.next = this.head;
  }
}
```

## 📌 5장. 배열과 연결 리스트의 성능 차이 분석

| 연산 | 배열(Array) | 연결 리스트(Linked List) |
|------|-------------|-------------------------|
| 접근(Access) | O(1) 빠름 | O(n) 느림 |
| 삽입/삭제(앞쪽) | O(n) 느림 | O(1) 빠름 |
| 삽입/삭제(뒤쪽) | O(1) 빠름 | O(n) 느림 (단, Tail 포인터가 있으면 O(1)) |
| 메모리 사용 | 연속된 메모리 필요 | 비연속적 메모리 사용 |

### 🔹 사용 권장 상황
- 데이터 삽입 및 삭제가 빈번하게 일어날 경우 연결 리스트가 적합합니다.
- 임의 접근(random access)이 중요하면 배열 사용이 적합합니다.

---

## 📝 정리 및 요약
- 연결 리스트는 배열의 단점을 보완하여 메모리 사용과 성능을 최적화합니다.
- 단일, 이중, 환형 연결 리스트 각각의 구조와 활용 방법을 이해해야 합니다.
- 성능 특성을 정확히 파악하여 상황에 따라 배열과 연결 리스트를 적절히 활용할 수 있어야 합니다.

이 가이드를 통해 연결 리스트의 개념과 구현 방법을 충분히 이해하여 효율적인 프로그래밍을 수행하실 수 있기를 바랍니다.







5️⃣ 스택(Stack)


# 📖 JavaScript 스택(Stack) 완벽 가이드

## 📌 1장. 스택의 개념과 특징

### 🔹 스택(Stack)이란?
- 스택은 데이터의 입출력이 한쪽에서만 이루어지는 자료구조입니다.
- 후입선출(LIFO: Last In First Out) 구조를 가집니다.

### 🔹 주요 연산
- **push**: 스택의 맨 위에 데이터를 추가합니다.
- **pop**: 스택의 맨 위에서 데이터를 제거하고 반환합니다.
- **peek**: 스택의 맨 위 데이터를 확인만 합니다.
- **isEmpty**: 스택이 비었는지 여부를 확인합니다.

## 📌 2장. 스택 구현하기

### 🔹 배열을 이용한 스택 구현

```javascript
class ArrayStack {
  constructor() {
    this.stack = [];
  }

  push(item) {
    this.stack.push(item);
  }

  pop() {
    if (this.isEmpty()) return null;
    return this.stack.pop();
  }

  peek() {
    return this.isEmpty() ? null : this.stack[this.stack.length - 1];
  }

  isEmpty() {
    return this.stack.length === 0;
  }
}

// 예제
const stack = new ArrayStack();
stack.push(1);
stack.push(2);
console.log(stack.pop()); // 2
```

### 🔹 연결 리스트를 이용한 스택 구현

```javascript
class Node {
  constructor(data) {
    this.data = data;
    this.next = null;
  }
}

class LinkedListStack {
  constructor() {
    this.head = null;
  }

  push(data) {
    const newNode = new Node(data);
    newNode.next = this.head;
    this.head = newNode;
  }

  pop() {
    if (this.isEmpty()) return null;
    const removedNode = this.head;
    this.head = this.head.next;
    return removedNode.data;
  }

  peek() {
    return this.isEmpty() ? null : this.head.data;
  }

  isEmpty() {
    return this.head === null;
  }
}

// 예제
const stack = new LinkedListStack();
stack.push(1);
stack.push(2);
console.log(stack.pop()); // 2
```

## 📌 3장. 스택의 주요 활용 사례

### 🔹 브라우저의 뒤로 가기 기능
- 방문한 페이지를 스택에 쌓아두고, 뒤로 가기를 눌렀을 때 마지막 페이지를 불러옵니다.

### 🔹 함수 호출 관리(Call Stack)
- 프로그램에서 함수 호출 시 호출된 순서대로 스택에 쌓이고, 종료될 때는 역순으로 실행됩니다.

### 🔹 수식 계산(중위 표기식 → 후위 표기식)
- 수식의 우선순위 처리를 스택을 통해 효율적으로 관리할 수 있습니다.

```javascript
// 후위 표기식 평가 예시
function evaluatePostfix(expression) {
  const stack = new ArrayStack();

  for (const char of expression) {
    if (!isNaN(char)) {
      stack.push(Number(char));
    } else {
      const b = stack.pop();
      const a = stack.pop();

      switch (char) {
        case '+': stack.push(a + b); break;
        case '-': stack.push(a - b); break;
        case '*': stack.push(a * b); break;
        case '/': stack.push(a / b); break;
      }
    }
  }

  return stack.pop();
}

console.log(evaluatePostfix("23*5+")); // 11
```

## 📌 4장. 성능 분석

| 연산 | 배열 기반 스택 | 연결 리스트 기반 스택 |
|------|-----------------|------------------------|
| push | O(1)            | O(1)                   |
| pop  | O(1)            | O(1)                   |
| 메모리 사용 | 배열 크기 조정 시 추가 메모리 사용 가능성 있음 | 노드별 포인터 메모리 사용 |

### 🔹 구현 방식 선택 가이드
- 대부분 상황에서는 배열 기반이 간단하고 성능도 뛰어나 추천됩니다.
- 메모리 관리가 중요하거나 크기 변동성이 크면 연결 리스트가 유리합니다.

---

## 📝 정리 및 요약
- 스택은 LIFO 원칙을 따르는 자료구조로, 특정 연산(push, pop)에 최적화되어 있습니다.
- 배열과 연결 리스트 모두 O(1)의 성능을 제공하지만, 메모리 관리 특성이 다릅니다.
- 스택은 프로그램 내부의 다양한 관리 작업(함수 호출, 브라우저 히스토리 등)에 필수적으로 사용됩니다.

이 가이드를 통해 스택 자료구조의 이론과 실무적인 활용 방법을 명확히 이해하고 응용하시기 바랍니다.







6️⃣ 큐(Queue)

# 📖 JavaScript 큐(Queue) 완벽 가이드

## 📌 1장. 큐의 개념과 특징

### 🔹 큐(Queue)란?
- 데이터가 입력된 순서대로 처리되는 선입선출(FIFO: First In First Out) 자료구조입니다.
- 먼저 들어온 데이터가 먼저 나가는 구조입니다.

### 🔹 주요 연산
- **enqueue**: 큐의 뒤쪽에 데이터를 추가합니다.
- **dequeue**: 큐의 앞쪽에서 데이터를 제거하고 반환합니다.
- **front**: 큐의 맨 앞 데이터를 확인합니다.
- **isEmpty**: 큐가 비었는지 여부를 확인합니다.

## 📌 2장. 큐 구현하기

### 🔹 배열을 이용한 큐 구현

```javascript
class ArrayQueue {
  constructor() {
    this.queue = [];
  }

  enqueue(item) {
    this.queue.push(item);
  }

  dequeue() {
    return this.isEmpty() ? null : this.queue.shift();
  }

  front() {
    return this.isEmpty() ? null : this.queue[0];
  }

  isEmpty() {
    return this.queue.length === 0;
  }
}

// 사용 예제
const queue = new ArrayQueue();
queue.enqueue(1);
queue.enqueue(2);
console.log(queue.dequeue()); // 1
```

### 🔹 연결 리스트를 이용한 큐 구현

```javascript
class Node {
  constructor(data) {
    this.data = data;
    this.next = null;
  }
}

class LinkedListQueue {
  constructor() {
    this.head = null;
    this.tail = null;
  }

  enqueue(data) {
    const newNode = new Node(data);
    if (this.isEmpty()) {
      this.head = newNode;
      this.tail = newNode;
    } else {
      this.tail.next = newNode;
      this.tail = newNode;
    }
  }

  dequeue() {
    if (this.isEmpty()) return null;
    const removed = this.head;
    this.head = this.head.next;
    if (!this.head) this.tail = null;
    return removed.data;
  }

  front() {
    return this.isEmpty() ? null : this.head.data;
  }

  isEmpty() {
    return this.head === null;
  }
}

// 사용 예제
const queue = new LinkedListQueue();
queue.enqueue(1);
queue.enqueue(2);
console.log(queue.dequeue()); // 1
```

## 📌 3장. 환형 큐(Circular Queue)

### 🔹 개념
- 공간을 효율적으로 사용하기 위해 배열의 끝과 시작을 연결한 원형 형태의 큐입니다.

### 🔹 구현 예시

```javascript
class CircularQueue {
  constructor(size) {
    this.queue = Array(size);
    this.front = 0;
    this.rear = 0;
    this.size = size;
    this.length = 0;
  }

  enqueue(item) {
    if (this.length === this.size) return false;
    this.queue[this.rear] = item;
    this.rear = (this.rear + 1) % this.size;
    this.length++;
    return true;
  }

  dequeue() {
    if (this.length === 0) return null;
    const item = this.queue[this.front];
    this.front = (this.front + 1) % this.size;
    this.length--;
    return item;
  }

  frontItem() {
    return this.length === 0 ? null : this.queue[this.front];
  }
}

// 예시
const cq = new CircularQueue(3);
cq.enqueue(1);
cq.enqueue(2);
cq.enqueue(3);
console.log(cq.dequeue()); // 1
```

## 📌 4장. 우선순위 큐(Priority Queue)

### 🔹 개념
- 데이터를 우선순위에 따라 처리하는 큐입니다.
- 높은 우선순위를 가진 데이터가 먼저 나갑니다.
- 힙(Heap) 자료구조와 연계해 성능을 최적화합니다.

### 🔹 최소 힙 기반 우선순위 큐 구현

```javascript
class PriorityQueue {
  constructor() {
    this.heap = [];
  }

  enqueue(item, priority) {
    this.heap.push({ item, priority });
    this.bubbleUp();
  }

  dequeue() {
    const min = this.heap[0];
    const end = this.heap.pop();
    if (this.heap.length > 0) {
      this.heap[0] = end;
      this.sinkDown();
    }
    return min.item;
  }

  bubbleUp() {
    let idx = this.heap.length - 1;
    const element = this.heap[idx];

    while (idx > 0) {
      let parentIdx = Math.floor((idx - 1) / 2);
      let parent = this.heap[parentIdx];

      if (element.priority >= parent.priority) break;

      this.heap[idx] = parent;
      idx = parentIdx;
    }
    this.heap[idx] = element;
  }

  sinkDown() {
    let idx = 0;
    const length = this.heap.length;
    const element = this.heap[0];

    while (true) {
      let leftChildIdx = 2 * idx + 1;
      let rightChildIdx = 2 * idx + 2;
      let swap = null;

      if (leftChildIdx < length) {
        if (this.heap[leftChildIdx].priority < element.priority) swap = leftChildIdx;
      }

      if (rightChildIdx < length && this.heap[rightChildIdx].priority < (swap === null ? element.priority : this.heap[leftChildIdx].priority)) swap = rightChildIdx;

      if (swap === null) break;

      this.heap[idx] = this.heap[swap];
      idx = swap;
    }
    this.heap[idx] = element;
  }
}
```

---

## 📝 정리 및 요약
- 큐는 FIFO 특성을 가진 필수적인 자료구조입니다.
- 배열과 연결 리스트로 큐를 쉽게 구현할 수 있습니다.
- 환형 큐와 우선순위 큐는 특수한 상황에서 성능과 효율성을 높여줍니다.

이 가이드를 통해 큐를 효과적으로 이해하고, 응용할 수 있기를 바랍니다.





📗 PART 2. 자료구조 심화
7️⃣ 해시 테이블(Hash Table)

# 📖 JavaScript 해시 테이블(Hash Table) 완벽 가이드

## 📌 1장. 해싱의 개념과 원리

### 🔹 해시 테이블이란?
- **해시 함수(Hash Function)**를 통해 키(key)를 해시(hash)라는 고정 길이의 값으로 변환하고, 이를 배열의 인덱스로 사용해 데이터를 저장하는 자료구조입니다.
- 키-값 쌍을 효율적으로 조회, 삽입, 삭제할 수 있어 평균적으로 O(1)에 가까운 시간 복잡도를 가집니다.

### 🔹 해시 함수의 목표
1. **충돌(Collision)을 최소화**해야 합니다.
2. **균등 분포**: 다양한 입력 키가 해시 테이블의 다양한 인덱스에 고르게 분포되어야 합니다.
3. **빠른 계산**: 해시 함수를 계산하는 데에 과도한 시간이 걸리면 오히려 성능이 저하될 수 있습니다.

---

## 📌 2장. 충돌 처리 기법 (Collision Handling)

해시 함수는 매우 좋더라도 충돌이 0%로 일어나지 않는다는 보장은 없습니다. 그래서 충돌 처리 기법이 필요합니다.

### 1. 체이닝(Chaining)
- 동일 인덱스에 충돌이 발생하면 연결 리스트(또는 배열 등)로 해당 슬롯을 확장하여 저장
- 해시 테이블의 각 인덱스가 여러 개의 데이터를 가질 수 있도록 합니다.

**장점**:
- 간단한 구현, 해시 충돌이 발생해도 적절한 구조로 확장 가능

**단점**:
- 테이블이 커질수록, 그리고 충돌이 많을수록 연결 리스트 접근 시간이 증가할 수 있음

### 2. 개방 주소 방식(Open Addressing)

#### 🔹 선형 탐사법(Linear Probing)
- 충돌이 발생하면 **다음 인덱스**부터 순차적으로 비어 있는 슬롯을 탐색해 저장

```plaintext
index = (hash(key) + i) mod table_size
```

- i는 충돌 발생 시 0부터 시작하여 1씩 증가

**장점**:
- 연결 리스트가 필요 없어 메모리를 절약

**단점**:
- 클러스터링(Clustering) 현상으로 인해 충돌이 연쇄적으로 발생 가능

#### 🔹 이중 해싱(Double Hashing)
- 선형 탐사법의 문제점인 클러스터링을 완화하기 위한 방식
- 첫 번째 해시 함수 충돌 시, **두 번째 해시 함수**를 사용해 이동 거리를 결정

```plaintext
index = (hash1(key) + i * hash2(key)) mod table_size
```

**장점**:
- 충돌이 더 분산되어 선형 탐사법보다 충돌이 덜 발생

**단점**:
- 해시 함수를 2개 설계해야 해서 구현 복잡도 증가

---

## 📌 3장. JavaScript에서의 해시 테이블 구현

### 1. 객체(Object)와 맵(Map)
- 자바스크립트에서 객체와 Map은 해시 맵과 유사한 기능을 제공합니다.
- 내부적으로 해시 구조를 사용하여 빠른 키-값 접근이 가능합니다.

```javascript
// 객체(Object) 사용 예
const obj = {};
obj["name"] = "Alice";
obj["age"] = 25;

console.log(obj["name"]); // Alice

// Map 사용 예
const map = new Map();
map.set("name", "Alice");
map.set("age", 25);

console.log(map.get("name")); // Alice
```

**Map과 Object 비교**:
- **Map**은 키 타입에 제한이 없으며, 키-값 쌍의 개수를 쉽게 확인할 수 있는 `size` 프로퍼티 제공
- **Object**는 문자열/심볼 이외의 키 사용 시 내부적으로 문자열로 변환

### 2. 체이닝 기법을 사용한 직접 해시 테이블 구현 예시

```javascript
class HashTable {
  constructor(size = 17) {
    this.buckets = new Array(size);
    for (let i = 0; i < this.buckets.length; i++) {
      this.buckets[i] = [];
    }
  }

  _hash(key) {
    let total = 0;
    for (let char of key) {
      total = (total + char.charCodeAt(0) - 96) % this.buckets.length;
    }
    return total;
  }

  set(key, value) {
    const index = this._hash(key);
    // 중복 키 확인 후 업데이트 또는 새로 삽입
    for (let pair of this.buckets[index]) {
      if (pair[0] === key) {
        pair[1] = value;
        return;
      }
    }
    this.buckets[index].push([key, value]);
  }

  get(key) {
    const index = this._hash(key);
    for (let pair of this.buckets[index]) {
      if (pair[0] === key) {
        return pair[1];
      }
    }
    return undefined;
  }
}

// 사용 예시
const ht = new HashTable();
ht.set("pink", "#ffc0cb");
ht.set("blue", "#0000ff");
console.log(ht.get("pink")); // #ffc0cb
```

---

## 📌 4장. 해시 함수 성능 평가

### 🔹 해시 충돌(Collision) 지표
- **충돌 횟수**: 서로 다른 키가 같은 해시 값을 반환하는 경우
- **체이닝 시 길이**: 단일 버킷에 연결된 노드(또는 배열)의 평균 길이

### 🔹 부하율(Load Factor)
- 저장된 항목 수를 버킷(슬롯) 수로 나눈 값
```plaintext
Load Factor = number_of_elements / number_of_buckets
```
- 부하율이 높아질수록 충돌 확률이 높아지므로, 적절한 시점에 **리사이징(Resizing)** 이 필요합니다.

### 🔹 시간 복잡도
- **평균 시간**: O(1)
- **최악 시간**: O(n)
  - 모든 키가 같은 버킷으로 들어가 연결 리스트가 매우 길어질 경우

---

## 📝 정리 및 요약
- 해시 테이블은 평균적으로 매우 빠른 키-값 접근을 제공하는 자료구조입니다.
- 충돌 처리 방식(체이닝, 개방 주소법, 이중 해싱 등)을 적절히 사용하여 성능을 최적화할 수 있습니다.
- JavaScript에서는 기본적으로 `Object`와 `Map`이 해시 구조를 제공해 편리하게 사용할 수 있습니다.
- 해시 함수를 설계할 때 균등 분포와 빠른 계산 속도를 우선 고려해야 하며, 부하율 관리도 중요합니다.

이 가이드를 통해 해시 테이블의 이론적 토대와 JavaScript를 활용한 구현 방안을 충분히 이해하고 실제 개발 상황에서 활용할 수 있길 바랍니다.







8️⃣ 트리(Tree)

# 📖 JavaScript 트리(Tree) 완벽 가이드

## 📌 1장. 트리 개념 및 용어 정리

### 🔹 트리(Tree)란?
- **계층적**(Hierarchical) 구조를 표현하는 비선형 자료구조
- 노드(Node)들이 연결되어 있으며, 각 노드가 여러 자식 노드를 가질 수 있습니다.

### 🔹 기본 용어
- **루트(Root)**: 트리의 시작 노드로, 부모(parent)가 없는 노드
- **노드(Node)**: 데이터를 저장하는 기본 단위. 자식(child)을 가질 수 있습니다.
- **간선(Edge)**: 노드와 노드를 연결하는 링크
- **단말 노드(Leaf Node)**: 자식이 없는 노드
- **레벨(Level)**: 루트로부터의 거리 (루트의 레벨을 0 또는 1로 정의)
- **높이(Height)**: 트리의 최대 레벨 (또는 최대 깊이)
- **깊이(Depth)**: 특정 노드가 루트로부터 떨어진 거리

> 예를 들어, 루트로부터 2번 이동해야 도달하는 노드의 깊이는 2입니다.

---

## 📌 2장. 이진 트리(Binary Tree) 개념과 순회(Traversal)

### 🔹 이진 트리(Binary Tree)
- 각 노드가 최대 2개의 자식(왼쪽, 오른쪽)을 가질 수 있는 트리
- 이진 트리는 논리적 구조만 의미하며, 특별한 정렬 조건은 없습니다.

### 🔹 트리 순회(Traversal)
1. **전위 순회(Preorder Traversal)**: (루트) - (왼쪽 서브트리) - (오른쪽 서브트리)
2. **중위 순회(Inorder Traversal)**: (왼쪽 서브트리) - (루트) - (오른쪽 서브트리)
3. **후위 순회(Postorder Traversal)**: (왼쪽 서브트리) - (오른쪽 서브트리) - (루트)
4. **레벨 순회(Level Order Traversal)**: 너비 우선 탐색(BFS) 방식으로 같은 레벨의 노드를 순서대로 방문

### 🔹 순회 예제

```javascript
class TreeNode {
  constructor(value) {
    this.value = value;
    this.left = null;
    this.right = null;
  }
}

// 전위 순회
function preorder(root) {
  if (!root) return;
  console.log(root.value);
  preorder(root.left);
  preorder(root.right);
}

// 중위 순회
function inorder(root) {
  if (!root) return;
  inorder(root.left);
  console.log(root.value);
  inorder(root.right);
}

// 후위 순회
function postorder(root) {
  if (!root) return;
  postorder(root.left);
  postorder(root.right);
  console.log(root.value);
}

// 레벨 순회(BFS)
function levelOrder(root) {
  if (!root) return;
  const queue = [root];

  while (queue.length) {
    const node = queue.shift();
    console.log(node.value);

    if (node.left) queue.push(node.left);
    if (node.right) queue.push(node.right);
  }
}
```

---

## 📌 3장. 이진 탐색 트리(Binary Search Tree, BST)

### 🔹 BST의 특징
- **왼쪽 서브트리**: 루트보다 작은 값의 노드들
- **오른쪽 서브트리**: 루트보다 큰 값의 노드들
- 모든 서브트리 역시 이진 탐색 트리 구조를 만족

### 🔹 BST 구현 및 연산

```javascript
class BSTNode {
  constructor(value) {
    this.value = value;
    this.left = null;
    this.right = null;
  }
}

class BinarySearchTree {
  constructor() {
    this.root = null;
  }

  insert(value) {
    const newNode = new BSTNode(value);

    if (!this.root) {
      this.root = newNode;
      return;
    }

    let current = this.root;
    while (true) {
      if (value < current.value) {
        if (!current.left) {
          current.left = newNode;
          return;
        }
        current = current.left;
      } else {
        if (!current.right) {
          current.right = newNode;
          return;
        }
        current = current.right;
      }
    }
  }

  search(value) {
    let current = this.root;
    while (current) {
      if (value < current.value) {
        current = current.left;
      } else if (value > current.value) {
        current = current.right;
      } else {
        return true; // 값 찾음
      }
    }
    return false; // 값 없음
  }

  remove(value, root = this.root, parent = null) {
    if (!root) return false;

    // 1) 노드 탐색
    if (value < root.value) {
      return this.remove(value, root.left, root);
    } else if (value > root.value) {
      return this.remove(value, root.right, root);
    } else {
      // 2) 노드 삭제
      if (!root.left && !root.right) {
        // 단말 노드
        if (root === this.root) {
          this.root = null;
        } else if (parent.left === root) {
          parent.left = null;
        } else {
          parent.right = null;
        }
      } else if (root.left && root.right) {
        // 두 자식 노드
        const minNode = this._findMinNode(root.right);
        const tempValue = minNode.value;
        this.remove(minNode.value, this.root);
        root.value = tempValue;
      } else {
        // 한 자식 노드
        const child = root.left || root.right;
        if (root === this.root) {
          this.root = child;
        } else if (parent.left === root) {
          parent.left = child;
        } else {
          parent.right = child;
        }
      }
      return true;
    }
  }

  _findMinNode(node) {
    while (node.left) {
      node = node.left;
    }
    return node;
  }
}

// 사용 예시
const bst = new BinarySearchTree();
bst.insert(10);
bst.insert(5);
bst.insert(15);
bst.insert(2);
console.log(bst.search(5));   // true
console.log(bst.search(20));  // false
bst.remove(5);
```

---

## 📌 4장. AVL 트리와 균형 잡힌 트리의 필요성

### 🔹 균형 이진 트리
- 트리가 한쪽으로 치우치지 않도록, 높이를 최소화하는 이진 트리 구조
- **높이 균형**으로 인해 탐색, 삽입, 삭제 연산에서 O(log n) 시간 복잡도 보장

### 🔹 AVL 트리
- 가장 오래된 균형 이진 탐색 트리 구조 중 하나
- **각 노드**에 대해, 왼쪽 서브트리와 오른쪽 서브트리의 **높이 차이가 1을 넘지 않도록 유지**
- 삽입/삭제 시 균형이 깨지면 **회전(Rotation)** 과정을 통해 균형을 맞춤

### 🔹 균형 트리가 필요한 이유
- 일반적인 BST에서, 삽입 순서에 따라 한쪽으로 치우쳐 (예: 오름차순 데이터) 실제 높이가 O(n)까지 증가 가능
- 균형 트리를 유지하면 **항상 O(log n)**의 성능을 기대할 수 있어 대규모 데이터 처리가 효율적

---

## 📝 정리 및 요약
- 트리는 계층적 구조를 나타내는 비선형 자료구조이며, 각각의 노드가 여러 자식을 가질 수 있습니다.
- 이진 트리는 각 노드가 최대 2개의 자식을 가지는 특별한 형태로, 순회를 통해 데이터를 체계적으로 방문할 수 있습니다.
- 이진 탐색 트리(BST)는 정렬된 구조를 제공하여 탐색, 삽입, 삭제가 평균 O(log n) 시간 복잡도를 갖습니다.
- AVL 트리와 같은 균형 잡힌 트리를 사용하면 트리 높이를 최소화하여 일관된 O(log n) 성능을 유지할 수 있습니다.

이 문서로 트리 전반의 핵심 개념과 JavaScript 예시 코드를 충분히 익히시어, 실제 프로젝트에서 트리를 효과적으로 활용하시길 바랍니다.






9️⃣ 힙(Heap)

# 📖 JavaScript 힙(Heap) 완벽 가이드

## 📌 1장. 힙(Heap) 자료구조의 개념과 특징

### 🔹 힙(Heap)이란?
- **완전 이진 트리(Complete Binary Tree)** 형태를 가지는 자료구조
- 부모 노드와 자식 노드 간의 특정 우선순위를 유지

### 🔹 최소 힙(Min Heap)과 최대 힙(Max Heap)
1. **최소 힙(Min Heap)**
   - 부모 노드의 값이 자식 노드의 값보다 항상 작거나 같다.
   - 루트 노드에는 전체 원소 중 최솟값이 위치합니다.

2. **최대 힙(Max Heap)**
   - 부모 노드의 값이 자식 노드의 값보다 항상 크거나 같다.
   - 루트 노드에는 전체 원소 중 최댓값이 위치합니다.

### 🔹 특징
- **추가(Insertion)** 및 **삭제(Removal)** 연산에서 O(log n)의 시간 복잡도
- 루트 노드는 힙에서 가장 작은(최소 힙) 또는 가장 큰(최대 힙) 원소
- **우선순위 큐** 구현에 많이 사용됩니다.

---

## 📌 2장. 힙을 이용한 우선순위 큐(Priority Queue) 구현

### 🔹 우선순위 큐란?
- 우선순위가 높은 요소를 먼저 꺼내는 자료구조
- 힙(특히 최소 힙)을 사용하면 효율적으로 구현 가능

### 🔹 최소 힙 기반 우선순위 큐 예제

```javascript
class MinHeap {
  constructor() {
    this.heap = [];
  }

  // 요소 삽입
  insert(value) {
    this.heap.push(value);
    this.bubbleUp();
  }

  // 힙 정렬 유지
  bubbleUp() {
    let index = this.heap.length - 1;
    const inserted = this.heap[index];

    while (index > 0) {
      let parentIndex = Math.floor((index - 1) / 2);
      if (this.heap[parentIndex] <= inserted) break;
      this.heap[index] = this.heap[parentIndex];
      index = parentIndex;
    }
    this.heap[index] = inserted;
  }

  // 최소값 제거
  extractMin() {
    if (this.heap.length === 0) return null;
    const min = this.heap[0];
    const end = this.heap.pop();
    if (this.heap.length > 0) {
      this.heap[0] = end;
      this.sinkDown(0);
    }
    return min;
  }

  // 힙 구조 유지
  sinkDown(index) {
    const length = this.heap.length;
    const element = this.heap[index];

    while (true) {
      let leftIndex = 2 * index + 1;
      let rightIndex = 2 * index + 2;
      let leftChild, rightChild;
      let swap = null;

      if (leftIndex < length) {
        leftChild = this.heap[leftIndex];
        if (leftChild < element) {
          swap = leftIndex;
        }
      }

      if (rightIndex < length) {
        rightChild = this.heap[rightIndex];
        if (
          (swap === null && rightChild < element) ||
          (swap !== null && rightChild < leftChild)
        ) {
          swap = rightIndex;
        }
      }

      if (swap === null) break;
      this.heap[index] = this.heap[swap];
      this.heap[swap] = element;
      index = swap;
    }
  }
}

// 사용 예시: 우선순위 큐
class PriorityQueue {
  constructor() {
    this.minHeap = new MinHeap();
  }

  enqueue(value) {
    this.minHeap.insert(value);
  }

  dequeue() {
    return this.minHeap.extractMin();
  }
}
```

> 루트 노드가 항상 최소값을 유지하므로, `extractMin()`을 호출하면 최솟값이 먼저 빠져나갑니다.

---

## 📌 3장. 힙 정렬(Heap Sort)

### 🔹 힙 정렬이란?
- 최대 힙을 이용해 배열을 정렬하는 알고리즘
- **루트(최대값)**를 추출 후, 마지막 노드와 교환 → 힙의 크기를 1 줄여가며 반복

### 🔹 최대 힙으로 힙 정렬 구현 예시

```javascript
function heapSort(arr) {
  buildMaxHeap(arr);
  for (let i = arr.length - 1; i > 0; i--) {
    swap(arr, 0, i);
    heapify(arr, 0, i);
  }
  return arr;
}

function buildMaxHeap(arr) {
  const n = arr.length;
  for (let i = Math.floor(n / 2) - 1; i >= 0; i--) {
    heapify(arr, i, n);
  }
}

function heapify(arr, index, heapSize) {
  let largest = index;
  let left = 2 * index + 1;
  let right = 2 * index + 2;

  if (left < heapSize && arr[left] > arr[largest]) {
    largest = left;
  }
  if (right < heapSize && arr[right] > arr[largest]) {
    largest = right;
  }

  if (largest !== index) {
    swap(arr, index, largest);
    heapify(arr, largest, heapSize);
  }
}

function swap(arr, i, j) {
  [arr[i], arr[j]] = [arr[j], arr[i]];
}

// 사용 예시
const array = [3, 1, 5, 2, 4];
console.log(heapSort(array)); // 정렬된 배열 출력
```

### 🔹 알고리즘 복잡도
- **힙 정렬**은 O(n log n)의 시간 복잡도를 가집니다.
- **추가 메모리**를 거의 사용하지 않는 **제자리 정렬(in-place sorting)** 방식

---

## 📝 정리 및 요약
- 힙(Heap)은 완전 이진 트리 기반의 자료구조로, 부모 노드가 자식 노드보다 크거나 작다는 우선순위를 유지합니다.
- 최소 힙에서는 루트가 최소값, 최대 힙에서는 루트가 최대값이 되도록 유지합니다.
- 힙은 우선순위 큐 구현에 탁월한 성능(O(log n))을 발휘합니다.
- 힙 정렬은 최대 힙을 이용하여 배열을 정렬하는 알고리즘으로, 시간 복잡도 O(n log n)을 가집니다.

이 가이드로 힙의 구조와 응용(우선순위 큐, 힙 정렬)을 이해하고, JavaScript로 손쉽게 구현할 수 있길 바랍니다.




🔟 그래프(Graph)

# 📖 JavaScript 힙(Heap) 완벽 가이드

## 📌 1장. 힙(Heap)의 개념과 특징

### 🔹 힙(Heap)이란?
- **완전 이진 트리(Complete Binary Tree)** 기반의 자료구조
- 부모 노드와 자식 노드 간의 특정 우선순위 관계를 유지
- 트리의 높이가 h일 때, 모든 레벨이 꽉 차 있거나 마지막 레벨만 비어 있는 형태

### 🔹 최대 힙(Max Heap)
- 부모 노드의 값이 자식 노드의 값보다 항상 크거나 같은 구조
- 루트 노드가 가장 큰 값을 가짐

### 🔹 최소 힙(Min Heap)
- 부모 노드의 값이 자식 노드의 값보다 항상 작거나 같은 구조
- 루트 노드가 가장 작은 값을 가짐

---

## 📌 2장. 힙의 구현과 연산

### 🔹 힙 구현 시 주의사항
- **배열(리스트)**를 통해 구현
- 인덱스 계산을 통해 부모-자식 노드를 추적:
  - **왼쪽 자식** = `2 * index + 1`
  - **오른쪽 자식** = `2 * index + 2`
  - **부모** = `Math.floor((index - 1) / 2)`

### 🔹 최대 힙 구현 예시
```javascript
class MaxHeap {
  constructor() {
    this.heap = [];
  }

  // 삽입
  insert(value) {
    this.heap.push(value);
    this.bubbleUp();
  }

  bubbleUp() {
    let index = this.heap.length - 1;
    const insertedValue = this.heap[index];

    while (index > 0) {
      let parentIndex = Math.floor((index - 1) / 2);
      if (this.heap[parentIndex] >= insertedValue) break;

      this.heap[index] = this.heap[parentIndex];
      index = parentIndex;
    }
    this.heap[index] = insertedValue;
  }

  // 제거(루트 제거 후 마지막 원소를 루트로 옮기고 재정렬)
  extractMax() {
    if (this.heap.length === 0) {
      return null;
    }
    if (this.heap.length === 1) {
      return this.heap.pop();
    }

    const max = this.heap[0];
    this.heap[0] = this.heap.pop();
    this.sinkDown(0);
    return max;
  }

  sinkDown(index) {
    const length = this.heap.length;
    const element = this.heap[index];

    while (true) {
      let leftIndex = 2 * index + 1;
      let rightIndex = 2 * index + 2;
      let swap = null;

      if (leftIndex < length) {
        if (this.heap[leftIndex] > element) {
          swap = leftIndex;
        }
      }

      if (rightIndex < length) {
        if (
          (swap === null && this.heap[rightIndex] > element) ||
          (swap !== null && this.heap[rightIndex] > this.heap[leftIndex])
        ) {
          swap = rightIndex;
        }
      }

      if (swap === null) break;

      this.heap[index] = this.heap[swap];
      index = swap;
    }
    this.heap[index] = element;
  }
}

// 사용 예시
const maxHeap = new MaxHeap();
maxHeap.insert(10);
maxHeap.insert(15);
maxHeap.insert(20);
maxHeap.insert(17);
console.log(maxHeap.extractMax()); // 20
```

### 🔹 최소 힙 구현 시 차이점
- 비교 연산을 반대로 수행
- 부모 노드가 자식 노드보다 작아야 하므로, `insert`와 `sinkDown` 로직에서 반대 조건 체크

---

## 📌 3장. 우선순위 큐(Priority Queue)와 힙

### 🔹 우선순위 큐
- 큐와 달리, 우선순위가 높은 요소를 먼저 꺼내는 자료구조
- 내부적으로 **힙**을 이용해 높은 성능 제공 (평균 O(log n) 삽입/삭제)

### 🔹 간단한 예시
```javascript
class PriorityQueue {
  constructor() {
    this.heap = [];
  }

  enqueue(value, priority) {
    this.heap.push({ value, priority });
    this.bubbleUp();
  }

  bubbleUp() {
    let index = this.heap.length - 1;
    const element = this.heap[index];

    while (index > 0) {
      let parentIndex = Math.floor((index - 1) / 2);
      let parent = this.heap[parentIndex];
      if (parent.priority <= element.priority) break;
      this.heap[index] = parent;
      index = parentIndex;
    }
    this.heap[index] = element;
  }

  dequeue() {
    if (this.heap.length === 0) return null;
    const min = this.heap[0];
    const end = this.heap.pop();
    if (this.heap.length > 0) {
      this.heap[0] = end;
      this.sinkDown(0);
    }
    return min.value;
  }

  sinkDown(index) {
    const length = this.heap.length;
    const element = this.heap[index];

    while (true) {
      let leftIndex = 2 * index + 1;
      let rightIndex = 2 * index + 2;
      let swap = null;

      if (leftIndex < length) {
        if (this.heap[leftIndex].priority < element.priority) {
          swap = leftIndex;
        }
      }

      if (rightIndex < length) {
        if (
          (swap === null && this.heap[rightIndex].priority < element.priority) ||
          (swap !== null && this.heap[rightIndex].priority < this.heap[leftIndex].priority)
        ) {
          swap = rightIndex;
        }
      }

      if (swap === null) break;
      this.heap[index] = this.heap[swap];
      index = swap;
    }

    this.heap[index] = element;
  }
}
```

---

## 📌 4장. 힙 정렬(Heap Sort)

### 🔹 알고리즘 개념
- **힙 정렬**은 최대 힙을 이용해 배열을 정렬하는 대표적인 정렬 알고리즘 중 하나
- **평균 시간 복잡도**: O(n log n)

### 🔹 동작 원리
1. 배열을 힙 구조로 변환 (build-heap)
2. **루트(최댓값)**와 **말단 원소**를 교환 후, 배열의 정렬된 끝부분에 배치
3. 줄어든 힙 영역에 대해 **heapify** 과정을 반복해 나머지 요소를 재정렬
4. 모든 원소가 자리를 잡으면 정렬 완료

```javascript
function heapSort(arr) {
  // 1. Build Max Heap
  for (let i = Math.floor(arr.length / 2) - 1; i >= 0; i--) {
    heapify(arr, arr.length, i);
  }

  // 2. Extract elements from heap one by one
  for (let end = arr.length - 1; end > 0; end--) {
    // Swap root and end
    [arr[0], arr[end]] = [arr[end], arr[0]];

    // Call max heapify on the reduced heap
    heapify(arr, end, 0);
  }

  return arr;
}

function heapify(arr, size, rootIndex) {
  let largest = rootIndex;
  let left = 2 * rootIndex + 1;
  let right = 2 * rootIndex + 2;

  if (left < size && arr[left] > arr[largest]) {
    largest = left;
  }
  if (right < size && arr[right] > arr[largest]) {
    largest = right;
  }
  if (largest !== rootIndex) {
    [arr[rootIndex], arr[largest]] = [arr[largest], arr[rootIndex]];
    heapify(arr, size, largest);
  }
}

// 사용 예시
const arr = [4, 10, 3, 5, 1];
console.log(heapSort(arr)); // [1, 3, 4, 5, 10]
```

---

## 📝 정리 및 요약
- 힙은 완전 이진 트리를 기반으로 최대(최소) 값을 빠르게 추출할 수 있는 자료구조입니다.
- 우선순위 큐는 힙을 통해 구현 시 O(log n)의 효율적인 연산을 기대할 수 있습니다.
- 힙 정렬은 최대 힙을 활용하여 O(n log n) 시간에 정렬을 수행하는 알고리즘입니다.

이 가이드를 통해 힙 자료구조의 개념과 구현, 그리고 힙 정렬까지 충분히 이해하시어 효율적인 데이터 처리와 정렬 로직을 작성하시길 바랍니다.

# 📖 JavaScript 그래프(Graph) 완벽 가이드

## 📌 1장. 그래프 기본 개념

### 🔹 그래프(Graph)란?
- **정점(Vertex, 노드)**과 **간선(Edge)**으로 구성된 자료구조
- 간선은 두 정점을 연결하는 연결선으로, 방향성과 가중치를 가질 수 있음
- **경로(Path)**: 한 정점에서 다른 정점으로 이동하기 위해 거치는 정점들의 순서

### 🔹 용어 정리
- **인접(Adjacent)**: 간선으로 직접 연결된 두 정점
- **차수(Degree)**: 정점과 연결된 간선의 수
  - 무방향 그래프(Undirected)에서는 연결된 간선의 수
  - 방향 그래프(Directed)에서는 진입 차수(In-degree)와 진출 차수(Out-degree)로 구분

---

## 📌 2장. 그래프 표현 방식

### 🔹 인접 행렬(Adjacency Matrix)
- **2차원 배열**을 이용하여 그래프의 연결 관계를 나타내는 방식
- 정점의 개수가 V라고 할 때, V x V 크기의 행렬 생성
- 행렬 `[i][j]`가 1(또는 가중치)이면 정점 i에서 j로 간선이 존재

**장점**:
- 두 정점이 연결되었는지 확인이 O(1)

**단점**:
- 메모리 사용이 많음 (V^2 공간 필요)
- 희소 그래프(Sparse Graph)에서는 비효율적

### 🔹 인접 리스트(Adjacency List)
- 각 정점이 연결된 **인접 정점 목록**을 리스트로 관리
- 정점 i에 연결된 간선 정보만 별도의 리스트에 저장

**장점**:
- 공간을 절약 가능 (특히 희소 그래프에서 효율적)

**단점**:
- 두 정점의 연결 여부를 확인하려면 리스트를 탐색해야 하므로 O(V) 또는 O(E)

---

## 📌 3장. 그래프 탐색 기법

### 🔹 DFS (Depth-First Search)
- **깊이 우선 탐색**: 한 정점에서 시작해 가능한 경로를 따라 **깊이**를 우선으로 탐색

```javascript
function dfs(graph, start) {
  const visited = new Set();

  function traverse(vertex) {
    visited.add(vertex);
    console.log(vertex);

    for (let neighbor of graph[vertex]) {
      if (!visited.has(neighbor)) {
        traverse(neighbor);
      }
    }
  }

  traverse(start);
}

// 인접 리스트 예시
const graph = {
  A: ['B', 'C'],
  B: ['D'],
  C: ['E'],
  D: ['F'],
  E: [],
  F: []
};

dfs(graph, 'A'); // 방문 순서: A -> B -> D -> F -> C -> E
```

### 🔹 BFS (Breadth-First Search)
- **너비 우선 탐색**: 시작 정점에서 가까운 정점부터 차례로 탐색
- **큐(Queue)** 자료구조를 활용

```javascript
function bfs(graph, start) {
  const visited = new Set();
  const queue = [start];
  visited.add(start);

  while (queue.length) {
    const vertex = queue.shift();
    console.log(vertex);

    for (let neighbor of graph[vertex]) {
      if (!visited.has(neighbor)) {
        visited.add(neighbor);
        queue.push(neighbor);
      }
    }
  }
}

bfs(graph, 'A'); // 방문 순서: A -> B -> C -> D -> E -> F
```

### 🔹 DFS vs BFS 활용
- **DFS**는 경로 탐색(예: 백트래킹, 미로 문제)에 강점
- **BFS**는 최단 경로(가중치가 동일한 그래프의 경우) 문제 해결에 유용

---

## 📌 4장. 방향 그래프와 가중치 그래프

### 🔹 방향 그래프(Directed Graph)
- 간선에 **방향성**이 존재, A -> B와 B -> A가 다른 간선

### 🔹 무방향 그래프(Undirected Graph)
- 간선에 방향이 없으며, 연결되면 양방향 이동 가능

### 🔹 가중치 그래프(Weighted Graph)
- 간선마다 비용(가중치)이 부여
- 최단 경로 알고리즘(다익스트라, 벨만-포드 등)에서 가중치 정보를 사용해 비용 최소화 경로 계산

---

## 📝 정리 및 요약
- 그래프는 정점과 간선으로 구성된 강력하고 일반적인 자료구조
- 인접 행렬과 인접 리스트 중 그래프 특성과 V의 크기에 맞는 방식을 선택
- DFS와 BFS는 그래프 탐색의 기본이며, 각기 다른 최적의 활용 사례가 존재
- 방향성과 가중치 개념을 통해 네트워크, 지도 등 다양한 실제 문제에 적용 가능

이 가이드를 통해 그래프의 기본 이론과 구현 방법을 이해하고, DFS와 BFS를 활용한 다양한 문제 해결 접근 방식을 익히시길 바랍니다.



📘 PART 3. 알고리즘 기초
1️⃣1️⃣ 정렬 알고리즘(Sorting Algorithms)

# 📖 JavaScript 정렬 알고리즘(Sorting) 완벽 가이드

## 📌 1장. 정렬 알고리즘의 필요성
정렬은 많은 알고리즘과 문제에서 필수적으로 요구되는 연산입니다. **정렬 알고리즘**은 주어진 배열이나 리스트의 요소를 일정 기준(예: 오름차순, 내림차순)에 맞추어 재배열합니다. 알고리즘의 선택은 데이터의 크기, 특성, 메모리 사용량, 정렬 안정성(Stable/Unstable) 등에 따라 달라집니다.

---

## 📌 2장. 단순 정렬법

### 🔹 2.1 버블 정렬(Bubble Sort)

#### 알고리즘 개념
- 인접한 두 요소를 비교하여 잘못된 순서이면 교환하면서, 가장 큰 값을 뒤로 보내는 과정을 반복합니다.
- 매 단계마다 가장 큰(또는 작은) 값이 버블(거품)처럼 맨 끝(또는 맨 앞)으로 올라옵니다.

#### 시간 복잡도
- **최선**, **평균**, **최악** 모두 O(n^2)
- 데이터가 거의 정렬되어 있으면 일정 부분 최적화가 가능하지만, 일반적으로 낮은 효율

#### 구현 예시 (오름차순)
```javascript
function bubbleSort(arr) {
  const n = arr.length;
  for (let i = 0; i < n - 1; i++) {
    for (let j = 0; j < n - 1 - i; j++) {
      if (arr[j] > arr[j + 1]) {
        [arr[j], arr[j + 1]] = [arr[j + 1], arr[j]];
      }
    }
  }
  return arr;
}

// 사용 예시
const array1 = [64, 34, 25, 12, 22, 11, 90];
console.log(bubbleSort(array1)); // [11, 12, 22, 25, 34, 64, 90]
```

### 🔹 2.2 선택 정렬(Selection Sort)

#### 알고리즘 개념
- 매 단계마다 **가장 작은(또는 큰) 값을 선택**해서 맨 앞으로 보냅니다.
- 첫 번째 위치부터 n-1번째 위치까지 반복하며, 해당 위치에 올 값을 찾습니다.

#### 시간 복잡도
- **평균**과 **최악** 모두 O(n^2)
- 교환 횟수는 최대 n-1번으로 버블 정렬에 비해 교환 횟수는 적지만, 비교 횟수는 여전히 많습니다.

#### 구현 예시 (오름차순)
```javascript
function selectionSort(arr) {
  const n = arr.length;
  for (let i = 0; i < n - 1; i++) {
    let minIndex = i;
    for (let j = i + 1; j < n; j++) {
      if (arr[j] < arr[minIndex]) {
        minIndex = j;
      }
    }
    [arr[i], arr[minIndex]] = [arr[minIndex], arr[i]];
  }
  return arr;
}

// 사용 예시
const array2 = [29, 10, 14, 37, 13];
console.log(selectionSort(array2)); // [10, 13, 14, 29, 37]
```

### 🔹 2.3 삽입 정렬(Insertion Sort)

#### 알고리즘 개념
- 이미 정렬된 부분 배열에 새로운 요소를 삽입하여 정렬을 확장합니다.
- 초기 상태에서 첫 번째 요소는 이미 정렬되었다고 간주, 두 번째 요소부터 시작합니다.

#### 시간 복잡도
- **최선**: O(n) (이미 정렬된 경우)
- **평균**, **최악**: O(n^2)

#### 구현 예시 (오름차순)
```javascript
function insertionSort(arr) {
  const n = arr.length;
  for (let i = 1; i < n; i++) {
    let key = arr[i];
    let j = i - 1;

    // key보다 큰 값을 오른쪽으로 이동
    while (j >= 0 && arr[j] > key) {
      arr[j + 1] = arr[j];
      j--;
    }
    arr[j + 1] = key;
  }
  return arr;
}

// 사용 예시
const array3 = [12, 11, 13, 5, 6];
console.log(insertionSort(array3)); // [5, 6, 11, 12, 13]
```

---

## 📌 3장. 고급 정렬법

### 🔹 3.1 병합 정렬(Merge Sort)

#### 알고리즘 개념
- **분할 정복(Divide and Conquer)** 방식으로 배열을 반으로 나누어 재귀적으로 정렬 후, 병합하는 과정
- 안정 정렬(Stable Sort)로, 같은 값의 원소가 입력 순서대로 유지

#### 시간 복잡도
- **평균**, **최악** 모두 O(n log n)
- 메모리 사용량이 O(n) 추가로 필요 (임시 배열)

#### 구현 예시
```javascript
function mergeSort(arr) {
  if (arr.length <= 1) return arr;

  const mid = Math.floor(arr.length / 2);
  const left = mergeSort(arr.slice(0, mid));
  const right = mergeSort(arr.slice(mid));

  return merge(left, right);
}

function merge(left, right) {
  const result = [];
  let i = 0;
  let j = 0;

  while (i < left.length && j < right.length) {
    if (left[i] <= right[j]) {
      result.push(left[i]);
      i++;
    } else {
      result.push(right[j]);
      j++;
    }
  }

  return result.concat(left.slice(i)).concat(right.slice(j));
}

// 사용 예시
const array4 = [38, 27, 43, 3, 9, 82, 10];
console.log(mergeSort(array4)); // [3, 9, 10, 27, 38, 43, 82]
```

### 🔹 3.2 퀵 정렬(Quick Sort)

#### 알고리즘 개념
- 분할 정복 방식으로, **피벗(Pivot)**을 기준으로 작은 요소들과 큰 요소들을 각각 분할하여 정렬
- 구현이 간단하고 평균적으로 매우 빠른 정렬 중 하나

#### 시간 복잡도
- **평균**: O(n log n)
- **최악**: O(n^2) (피벗이 최솟값 또는 최댓값이 되는 등 균형이 깨진 경우)

#### 구현 예시
```javascript
function quickSort(arr) {
  if (arr.length < 2) return arr;

  const pivot = arr[Math.floor(arr.length / 2)];
  const left = [];
  const right = [];
  const equal = [];

  for (let num of arr) {
    if (num < pivot) {
      left.push(num);
    } else if (num > pivot) {
      right.push(num);
    } else {
      equal.push(num);
    }
  }

  return quickSort(left).concat(equal, quickSort(right));
}

// 사용 예시
const array5 = [10, 7, 8, 9, 1, 5];
console.log(quickSort(array5)); // [1, 5, 7, 8, 9, 10]
```

### 🔹 3.3 힙 정렬(Heap Sort)

#### 알고리즘 개념
- **힙(Heap)** 자료구조(최대 힙)를 이용하여 오름차순 정렬
- 부모-자식 간의 우선순위 조건을 만족하는 최대 힙을 구성 후, **루트(최댓값) 제거 → 배열 끝에 삽입** 연산을 반복

#### 시간 복잡도
- **평균**, **최악** 모두 O(n log n)
- 추가 메모리 사용이 최소화(O(1))된다는 장점

#### 구현 예시
```javascript
function heapSort(arr) {
  // 1. Build Max Heap
  for (let i = Math.floor(arr.length / 2) - 1; i >= 0; i--) {
    heapify(arr, arr.length, i);
  }

  // 2. 하나씩 extract
  for (let end = arr.length - 1; end > 0; end--) {
    [arr[0], arr[end]] = [arr[end], arr[0]]; // 루트와 말단 교환
    heapify(arr, end, 0);
  }
  return arr;
}

function heapify(arr, size, rootIndex) {
  let largest = rootIndex;
  let left = 2 * rootIndex + 1;
  let right = 2 * rootIndex + 2;

  if (left < size && arr[left] > arr[largest]) {
    largest = left;
  }
  if (right < size && arr[right] > arr[largest]) {
    largest = right;
  }
  if (largest !== rootIndex) {
    [arr[rootIndex], arr[largest]] = [arr[largest], arr[rootIndex]];
    heapify(arr, size, largest);
  }
}

// 사용 예시
const array6 = [4, 10, 3, 5, 1];
console.log(heapSort(array6)); // [1, 3, 4, 5, 10]
```

---

## 📌 4장. 각 정렬 알고리즘 성능 및 특징 비교

| 알고리즘          | 평균 시간 복잡도 | 최악 시간 복잡도 | 메모리 사용    | 안정성(Stable)         | 특징 및 사용 사례 |
|-------------------|-------------------|-------------------|-----------------|-------------------------|--------------------|
| **버블 정렬**     | O(n^2)           | O(n^2)           | O(1)            | 안정 정렬(기본 구현 시) | 단순, 실무 사용 드묾 |
| **선택 정렬**     | O(n^2)           | O(n^2)           | O(1)            | 불안정(단순 구현 시)    | 교환 횟수 적음      |
| **삽입 정렬**     | O(n^2)           | O(n^2)           | O(1)            | 안정 정렬              | 거의 정렬된 데이터에 효과적 |
| **병합 정렬**     | O(n log n)       | O(n log n)       | O(n)            | 안정 정렬              | 대용량 데이터 정렬, 안정성 필요 시 |
| **퀵 정렬**       | O(n log n)       | O(n^2)           | O(log n) 평균   | 불안정                 | 평균 성능 매우 우수  |
| **힙 정렬**       | O(n log n)       | O(n log n)       | O(1)            | 불안정                 | 추가 메모리 최소화    |

- **안정 정렬(Stable Sort)**: 동등한 키 값을 가진 요소들의 순서가 정렬 이후에도 유지되는지 여부
- **불안정 정렬(Unstable Sort)**: 동등한 키 값을 가진 요소들의 상대 순서가 바뀔 수 있음

---

## 📌 5장. 적합한 상황별 정렬 알고리즘
- **데이터가 거의 정렬**되어 있다면 삽입 정렬이 효율적 (O(n)) 가능
- **추가 메모리가 제한**된 환경에서는 힙 정렬 선호
- **안정성이 중요**하면 병합 정렬, 또는 다른 안정 정렬 방법 고려
- **평균적으로 빠른 정렬**을 원한다면 퀵 정렬
- **학습 용도**나 간단한 테스트에는 버블/선택 정렬

---

## 📝 정리 및 요약
- 정렬 알고리즘은 문제의 규모, 데이터 특성, 메모리 제약, 안정성 여부에 따라 적절히 선택해야 합니다.
- 단순 정렬(버블, 선택, 삽입)은 구현이 쉽지만 O(n^2) 시간 복잡도로 대규모 데이터 처리에는 부적합
- 고급 정렬(병합, 퀵, 힙)은 평균 O(n log n) 시간 복잡도로 대규모 데이터에 적합
- 각각의 정렬 알고리즘을 상황에 따라 올바르게 활용할 수 있도록, 시간 복잡도와 구현 방식을 정확히 이해하는 것이 중요합니다.

이 문서가 정렬 알고리즘의 전체적인 이해와 선택에 도움이 되길 바랍니다!





1️⃣2️⃣ 탐색 알고리즘(Searching Algorithms)

# 📖 JavaScript 탐색 알고리즘(Searching Algorithms) 완벽 가이드

## 📌 1장. 탐색 알고리즘 개요

**탐색 알고리즘**은 주어진 데이터 집합에서 특정 값을 빠르고 효율적으로 찾기 위한 절차를 의미합니다. 탐색 알고리즘을 잘 활용하면 프로그램의 성능이 크게 향상됩니다. 본 문서에서는 가장 기본적이면서도 중요한 선형 탐색(Linear Search)과 이진 탐색(Binary Search)에 대해 알아봅니다.

---

## 📌 2장. 선형 탐색(Linear Search)

### 🔹 알고리즘 개념
- 배열(또는 리스트)의 **처음부터 끝까지** 차례대로 비교하며 원하는 값을 찾는 방법입니다.
- 구현이 간단하고 직관적이지만, 데이터가 많을수록 탐색 시간이 오래 걸릴 수 있습니다.

### 🔹 알고리즘 동작 방식
1. 배열의 첫 번째 요소부터 순차적으로 검사
2. 현재 요소가 찾는 값과 일치하면 탐색 성공
3. 배열 끝까지 검사했지만 찾는 값이 없으면 탐색 실패

### 🔹 시간 복잡도
- **평균**, **최악** 모두 O(n)
- 배열의 크기가 커질수록 시간 비용이 선형적으로 증가

### 🔹 코드 예시
```javascript
function linearSearch(arr, target) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === target) {
      return i; // 해당 인덱스를 반환
    }
  }
  return -1; // 찾지 못했을 경우 -1
}

// 사용 예시
const array1 = [4, 2, 7, 1, 9];
console.log(linearSearch(array1, 7));  // 출력: 2
console.log(linearSearch(array1, 10)); // 출력: -1
```

---

## 📌 3장. 이진 탐색(Binary Search)

### 🔹 알고리즘 개념
- 배열이 **정렬되어 있다는 전제** 하에, 중앙 요소와 비교하면서 탐색 범위를 절반씩 줄여가는 방식
- 선형 탐색보다 훨씬 빠른 검색이 가능하지만, **정렬**이 필수적입니다.

### 🔹 알고리즘 동작 방식
1. 배열의 중앙(mid) 요소를 선택
2. 찾는 값이 mid 값보다 작으면 왼쪽 절반, 크면 오른쪽 절반만 검사
3. 탐색 범위를 줄여가며 값을 찾거나, 범위가 없으면 탐색 실패

### 🔹 시간 복잡도
- **최대** O(log n)
- 데이터 개수가 2배가 되어도 탐색 횟수는 1회 정도만 증가하므로 대규모 데이터 탐색에 매우 효율적

### 🔹 코드 예시 (반복문)
```javascript
function binarySearch(arr, target) {
  let left = 0;
  let right = arr.length - 1;

  while (left <= right) {
    const mid = Math.floor((left + right) / 2);

    if (arr[mid] === target) {
      return mid;
    } else if (arr[mid] < target) {
      left = mid + 1;
    } else {
      right = mid - 1;
    }
  }
  return -1;
}

// 사용 예시 (정렬된 배열 필요)
const array2 = [1, 3, 5, 7, 9, 11];
console.log(binarySearch(array2, 7));  // 출력: 3
console.log(binarySearch(array2, 10)); // 출력: -1
```

### 🔹 재귀 구현 예시
```javascript
function binarySearchRecursive(arr, target, left = 0, right = arr.length - 1) {
  if (left > right) return -1;

  const mid = Math.floor((left + right) / 2);
  if (arr[mid] === target) {
    return mid;
  } else if (arr[mid] < target) {
    return binarySearchRecursive(arr, target, mid + 1, right);
  } else {
    return binarySearchRecursive(arr, target, left, mid - 1);
  }
}
```

---

## 📌 4장. 탐색 알고리즘 성능 비교 및 사용법

### 🔹 성능 비교

| 알고리즘         | 평균 시간 복잡도 | 최악 시간 복잡도 | 정렬 필요 여부 | 메모리 사용 | 특징                 |
|------------------|-------------------|-------------------|----------------|------------|----------------------|
| **선형 탐색**   | O(n)             | O(n)             | ❌             | O(1)       | 구현 간단, 정렬 불필요 |
| **이진 탐색**   | O(log n)         | O(log n)         | ✅             | O(1)       | 빠른 탐색, 정렬 필수  |

- 데이터가 **정렬**되어 있지 않다면, **선형 탐색**을 바로 사용하는 경우가 많습니다.
- 데이터가 **정렬**되어 있고 탐색 연산이 자주 발생한다면, **이진 탐색**을 사용하면 큰 이점을 얻습니다.
- 정렬 비용(최대 O(n log n))을 고려해야 하며, 정렬 후에도 데이터가 변경되지 않고 탐색만 빈번하다면 이진 탐색이 매우 효율적입니다.

---

## 📝 정리 및 요약
- **선형 탐색**: 단순하고 직관적이나 O(n)의 시간 복잡도.
- **이진 탐색**: 정렬된 배열에서 O(log n)에 탐색 가능.
- 데이터 상태(정렬 여부), 데이터 변경 빈도, 탐색 횟수 등을 고려해 적절한 알고리즘 선택 필요.

이 문서를 통해 탐색 알고리즘의 장단점과 상황별 활용 방안을 숙지하시어, 효율적인 데이터 탐색 로직을 구현하시길 바랍니다.





📙 PART 4. 알고리즘 심화
1️⃣3️⃣ 재귀(Recursion)

# 📖 JavaScript 재귀(Recursion) 완벽 가이드

## 📌 1장. 재귀의 개념과 작동 원리

### 🔹 재귀(Recursion)란?
- **함수가 자기 자신을 호출**하는 프로그래밍 기법
- 문제를 작은 부분 문제로 나누어(분할) 해결하는 **분할 정복(Divide and Conquer)** 방식과 밀접한 관련이 있음

### 🔹 기본 구조
1. **기저 사례(Base Case)**: 재귀 호출을 멈출 조건
2. **재귀 단계(Recursive Case)**: 기저 사례가 아닐 때, 자기 자신을 호출하여 해결

예:
```javascript
function recursiveFunction(n) {
  if (n <= 0) { // 기저 사례
    return;
  }
  // 재귀 단계
  recursiveFunction(n - 1);
}
```

### 🔹 호출 스택(Call Stack)
- 재귀 함수 호출 시, **각 함수의 실행 컨텍스트가 스택처럼 쌓였다가**(push) **완료되면 제거**(pop)
- 재귀 깊이가 깊어질수록 스택 메모리 사용량이 증가, 최악의 경우 스택 오버플로(Stack Overflow) 가능

---

## 📌 2장. 꼬리 재귀(Tail Recursion)와 호출 스택 이해

### 🔹 꼬리 재귀(Tail Recursion)
- **함수의 마지막 동작**으로 자기 자신을 호출하는 재귀 기법
- 재귀 호출 이후에 추가 작업이 필요하지 않음
- 일부 언어에서는 꼬리 재귀 최적화(Tail Call Optimization)를 통해 스택 오버플로 방지 가능 (JavaScript는 표준적으로 지원하지 않거나, 엔진마다 제한적으로 지원)

예:
```javascript
function tailRecursiveSum(n, acc = 0) {
  if (n === 0) return acc;
  return tailRecursiveSum(n - 1, acc + n);
}
```

### 🔹 호출 스택(Call Stack) 이해
- 일반 재귀:
  - 함수가 리턴되어야만 이전 스택 프레임으로 돌아가서 후속 작업을 진행할 수 있음
- 꼬리 재귀:
  - 다음 함수가 바로 return을 통해 결과를 넘기므로, 추가 작업이 거의 없음

---

## 📌 3장. 반복(Loop)과 재귀(Recursion)의 장단점

| 비교 항목         | 재귀(Recursion)                                                 | 반복(Loop)                                     |
|-------------------|----------------------------------------------------------------|-------------------------------------------------|
| 코드 가독성       | 문제 구조를 직관적으로 표현할 수 있음 (분할 정복)              | 단순 반복문이 명확할 때 이해가 쉬움            |
| 메모리 사용       | 호출 스택이 증가하여 메모리 사용량 많아질 수 있음               | 스택 증가는 없음                                |
| 성능              | 반복에 비해 오버헤드가 존재 (함수 호출 비용)                     | 일반적으로 재귀보다 빠르고 메모리 사용도 적음  |
| 구현 난이도       | 기저 사례(Base Case)를 고려해야 함                              | 재귀만큼 복잡한 문제라도 반복으로 변환 가능     |

- 데이터 구조가 **트리(tree)**나 **그래프(graph)**, 또는 **분할 정복** 접근에 적합할 때 재귀를 사용하면 코드가 간결해집니다.
- 단순한 반복 구조인 경우에는 for/while 루프가 성능적으로 유리합니다.

---

## 📌 4장. 대표적 재귀 알고리즘 사례

### 🔹 4.1 팩토리얼(Factorial)

```javascript
function factorial(n) {
  if (n <= 1) return 1; // 기저 사례
  return n * factorial(n - 1);
}

console.log(factorial(5)); // 120
```

### 🔹 4.2 피보나치(Fibonacci) 수열

```javascript
function fibonacci(n) {
  if (n <= 1) return n; // 기저 사례
  return fibonacci(n - 1) + fibonacci(n - 2);
}

console.log(fibonacci(5)); // 5

// 성능 개선 (메모이제이션)
function fibonacciMemo() {
  const memo = {};
  return function fib(n) {
    if (n <= 1) return n;
    if (memo[n]) return memo[n];
    memo[n] = fib(n - 1) + fib(n - 2);
    return memo[n];
  };
}

const fib = fibonacciMemo();
console.log(fib(10)); // 55
```

### 🔹 4.3 하노이탑(Tower of Hanoi)

**문제 요약**: 서로 다른 크기의 원판들을 한 기둥에서 다른 기둥으로 모두 옮기는데, 한 번에 하나씩만 옮길 수 있고, 큰 원판을 작은 원판 위에 놓으면 안 됩니다.

```javascript
function hanoi(n, start, aux, end) {
  if (n === 1) {
    console.log(`${start} -> ${end}`);
    return;
  }
  // Step 1: n-1개를 start에서 aux로 이동
  hanoi(n - 1, start, end, aux);
  // Step 2: 가장 큰 원판을 start에서 end로 이동
  console.log(`${start} -> ${end}`);
  // Step 3: n-1개를 aux에서 end로 이동
  hanoi(n - 1, aux, start, end);
}

hanoi(3, 'A', 'B', 'C');
// 출력:
// A -> C
// A -> B
// C -> B
// A -> C
// B -> A
// B -> C
// A -> C
```

---

## 📝 정리 및 요약
- **재귀**는 함수가 자기 자신을 호출하는 방식으로, 기본적으로 기저 사례와 재귀 단계를 포함합니다.
- **꼬리 재귀**를 통해 함수 호출 스택을 최적화할 수 있으나, JavaScript 엔진별 지원이 제한적입니다.
- 재귀 vs 반복은 상황과 문제 구조에 따라 선택하며, 성능과 가독성 트레이드오프가 존재합니다.
- 팩토리얼, 피보나치, 하노이탑 등 전형적인 재귀 문제들을 통해 재귀를 연습할 수 있습니다.

재귀 함수를 작성할 때는 반드시 **기저 사례**를 명확히 설정하고, 깊은 재귀가 발생할 수 있는 문제(예: 무한 루프)에 주의하시길 바랍니다!




1️⃣4️⃣ 분할정복(Divide and Conquer)

# 📖 JavaScript 분할 정복(Divide and Conquer) 완벽 가이드

## 📌 1장. 분할정복(Divide and Conquer) 기본 개념

### 🔹 개념 정의
- **분할 정복(Divide and Conquer)**은 문제를 작은 하위 문제(subproblems)로 분할하여 각각을 해결한 뒤, 그 결과를 합쳐 원래 문제의 해답을 구하는 알고리즘 설계 기법입니다.
- 대규모 문제도 작은 문제들로 나누면 해결하기 용이해지고, 재귀(Recursion) 방식을 많이 사용합니다.

### 🔹 주요 단계
1. **분할(Divide)**: 문제를 동일하거나 비슷한 크기의 작은 문제들로 나눕니다.
2. **정복(Conquer)**: 나눈 문제를 재귀적으로 해결합니다.
3. **결합(Combine)**: 하위 문제의 해답을 합쳐 원래 문제의 해답을 도출합니다.

> 분할 과정에서 하위 문제가 1개 또는 0개가 될 정도로 충분히 작아지면, 더 이상 분할할 필요가 없습니다.

---

## 📌 2장. 분할정복 설계 원칙

1. **작게 나누기**: 문제를 더 이상 나눌 수 없을 정도로 작은 단위로 분할
2. **하위 문제 해결**: 재귀적(또는 반복적) 방법으로 각 하위 문제를 해결
3. **결과 합치기**: 하위 문제들의 결과를 합쳐 최종 결과 도출

이 방식을 취하면 문제 해결 과정을 계층화하여 관리하기 쉬워집니다.

---

## 📌 3장. 분할정복 활용 사례

### 🔹 3.1 병합 정렬(Merge Sort)
- 배열을 반으로 나누고(분할), 각 부분 배열을 재귀적으로 정렬(정복)한 후, 두 부분 배열을 병합(결합)합니다.

```javascript
function mergeSort(arr) {
  if (arr.length <= 1) return arr;

  const mid = Math.floor(arr.length / 2);
  const left = mergeSort(arr.slice(0, mid));
  const right = mergeSort(arr.slice(mid));

  return merge(left, right);
}

function merge(left, right) {
  const result = [];
  let i = 0, j = 0;
  while (i < left.length && j < right.length) {
    if (left[i] < right[j]) {
      result.push(left[i]);
      i++;
    } else {
      result.push(right[j]);
      j++;
    }
  }
  return [...result, ...left.slice(i), ...right.slice(j)];
}
```

### 🔹 3.2 퀵 정렬(Quick Sort)
- 피벗(Pivot)을 기준으로 배열을 두 부분(왼쪽: 피벗보다 작거나 같은 원소, 오른쪽: 피벗보다 큰 원소)으로 분할
- 좌측, 우측 부분 배열을 재귀적으로 정렬(정복)
- 분할된 결과를 합쳐 최종 배열(결합)

```javascript
function quickSort(arr) {
  if (arr.length < 2) return arr;
  const pivot = arr[Math.floor(arr.length / 2)];
  const left = [];
  const right = [];
  const equal = [];

  for (let num of arr) {
    if (num < pivot) {
      left.push(num);
    } else if (num > pivot) {
      right.push(num);
    } else {
      equal.push(num);
    }
  }

  return quickSort(left).concat(equal, quickSort(right));
}
```

### 🔹 3.3 최대/최소값 찾기
- 배열에서 최댓값(또는 최솟값)을 찾는 문제를 분할정복으로 접근 가능
1. 배열을 절반으로 분할
2. 왼쪽 절반과 오른쪽 절반의 최대값(또는 최소값)을 재귀적으로 구함
3. 두 값을 비교해 최종 최대(또는 최소)값 결정

```javascript
function findMax(arr, start = 0, end = arr.length - 1) {
  if (start === end) {
    return arr[start];
  }
  const mid = Math.floor((start + end) / 2);
  const leftMax = findMax(arr, start, mid);
  const rightMax = findMax(arr, mid + 1, end);
  return leftMax > rightMax ? leftMax : rightMax;
}
```

---

## 📌 4장. 분할정복 알고리즘의 장단점

| 장점                                                       | 단점                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------|
| - 문제 구조가 직관적, 코드 가독성 향상                                             | - 재귀 호출로 인한 **오버헤드** 및 스택 메모리 사용                                        |
| - 병렬화(Parallelization)에 유리 (각 하위 문제 독립 수행 가능)                  | - 부적절한 분할 방식(퀵 정렬에서 편향된 피벗 등) 시 **성능 저하** 발생                  |
| - 각 부분 문제를 별도의 자료구조나 기법으로도 해결 가능 (유연성 높음)          | - 분할 과정에서 **추가 메모리**가 필요할 수 있음 (병합 정렬 등)                           |

---

## 📝 정리 및 요약
- 분할정복(Divide and Conquer)은 문제를 작은 하위 문제로 나누어 재귀적으로 해결한 뒤 통합하는 강력한 알고리즘 설계 기법입니다.
- 병합 정렬, 퀵 정렬, 최대/최소값 탐색 등 다양한 문제에서 활용되며, 효율적인 시간 복잡도(O(n log n) 등)를 보장합니다.
- 재귀 호출로 인해 스택 사용이 많아질 수 있으며, 분할 방식이 부적합하면 성능이 저하될 수도 있음을 유의해야 합니다.

이 문서를 통해 분할정복의 이론적 개념과 실무적 활용 사례를 파악하시고, 복잡한 문제를 손쉽게 해결하는 방법으로 적용해 보시기 바랍니다.



1️⃣5️⃣ 동적 계획법(Dynamic Programming)

# 📖 JavaScript 동적 계획법(Dynamic Programming) 완벽 가이드

## 📌 1장. 동적 계획법(Dynamic Programming) 개념

### 🔹 동적 계획법이란?
- **큰 문제**를 여러 개의 **작은 하위 문제(subproblems)**로 나누어 해결한 뒤, 그 답을 이용해 원래 문제를 해결하는 **알고리즘 설계 기법**입니다.
- 중복되는 하위 문제를 **메모이제이션(Memoization)** 또는 **테이블(Tabulation)** 기법으로 한 번만 계산해, 전체 연산량을 줄이는 것이 핵심입니다.

### 🔹 적용 조건
1. **최적 부분 구조(Optimal Substructure)**: 큰 문제의 최적해가 작은 하위 문제의 최적해를 통해 구성될 수 있어야 함
2. **중복 하위 문제(Overlapping Subproblems)**: 하위 문제가 여러 번 반복되어 등장해야 함

예: 피보나치 수열, 배낭 문제(Knapsack Problem) 등

---

## 📌 2장. 하향식(Top-Down)과 상향식(Bottom-Up)

### 🔹 하향식(Top-Down)
- **재귀**를 기반으로, 큰 문제 해결 과정에서 하위 문제의 결과가 필요한 시점에 계산
- 계산한 결과는 **메모이제이션(Memoization)** 배열(또는 객체)에 저장하여 재활용

**장점**:
- 구현이 직관적 (재귀 구조 그대로)
- 필요한 부분만 계산하므로 불필요한 계산이 줄어듦

**단점**:
- 깊은 재귀 호출로 인한 **스택 오버플로** 위험

### 🔹 상향식(Bottom-Up)
- 작은 하위 문제부터 **반복문**을 통해 차례로 계산을 진행하며, 최종적으로 큰 문제를 해결
- 계산 결과는 **테이블(Tabulation)** 형태(배열 등)에 순서대로 채워 넣음

**장점**:
- 재귀 호출이 없어 메모리 사용이 비교적 효율적
- 모든 하위 문제를 순서대로 계산하므로, 전체 문제 공간을 확실히 탐색

**단점**:
- 불필요한 하위 문제까지 계산하는 경우가 있을 수 있음 (사용되지 않는 부분문제 포함)

---

## 📌 3장. 대표적 예제

### 🔹 3.1 피보나치(Fibonacci) 수열

#### (1) 하향식 (Top-Down) 메모이제이션 예시
```javascript
function fibMemo(n, memo = {}) {
  if (n <= 1) return n;
  if (memo[n]) return memo[n];
  memo[n] = fibMemo(n - 1, memo) + fibMemo(n - 2, memo);
  return memo[n];
}

console.log(fibMemo(10)); // 55
```

#### (2) 상향식 (Bottom-Up) 테이블 예시
```javascript
function fibTab(n) {
  if (n <= 1) return n;
  const dp = [0, 1];
  for (let i = 2; i <= n; i++) {
    dp[i] = dp[i - 1] + dp[i - 2];
  }
  return dp[n];
}

console.log(fibTab(10)); // 55
```

### 🔹 3.2 최장 공통 부분 수열(LCS: Longest Common Subsequence)

- 두 시퀀스(문자열, 배열 등)가 주어졌을 때, 두 시퀀스에 **모두 등장하는 가장 긴 부분 수열**을 찾는 문제
- 예: `ABCBDAB`과 `BDCABA`의 LCS는 `BCBA` (길이 4)

#### 상향식 접근
```javascript
function LCS(str1, str2) {
  const m = str1.length;
  const n = str2.length;

  // dp[i][j] = str1의 앞 i글자와 str2의 앞 j글자로 구성된 부분 문자열의 LCS 길이
  const dp = Array.from({ length: m + 1 }, () => Array(n + 1).fill(0));

  for (let i = 1; i <= m; i++) {
    for (let j = 1; j <= n; j++) {
      if (str1[i - 1] === str2[j - 1]) {
        dp[i][j] = dp[i - 1][j - 1] + 1;
      } else {
        dp[i][j] = Math.max(dp[i - 1][j], dp[i][j - 1]);
      }
    }
  }

  return dp[m][n];
}

console.log(LCS("ABCBDAB", "BDCABA")); // 4
```

### 🔹 3.3 배낭 문제(Knapsack Problem)

- **0/1 배낭 문제**: 무게 제한(W)가 있는 배낭에 여러 물건을 넣을 때, **가치(Value)의 합을 최대로** 하는 물건 조합을 찾는 문제
- 각 물건의 무게(w_i)와 가치(v_i)가 주어졌을 때, **dp[i][w]** = i번째 물건까지 고려했을 때 무게 제한 w에서의 최대 가치

```javascript
function knapSack(W, weights, values, n) {
  // W: 배낭의 최대 무게, weights: 각 물건의 무게, values: 각 물건의 가치, n: 물건 개수
  const dp = Array.from({ length: n + 1 }, () => Array(W + 1).fill(0));

  for (let i = 1; i <= n; i++) {
    for (let w = 1; w <= W; w++) {
      // 현재 물건의 무게와 가치
      const wt = weights[i - 1];
      const val = values[i - 1];

      if (wt <= w) {
        // 넣을 수 있으면 (넣는 경우, 안 넣는 경우) 중 최댓값
        dp[i][w] = Math.max(dp[i - 1][w], dp[i - 1][w - wt] + val);
      } else {
        // 무게 초과라면 못 넣음
        dp[i][w] = dp[i - 1][w];
      }
    }
  }

  return dp[n][W];
}

// 예시
const W = 7;
const weights = [1, 3, 4, 5];
const values = [1, 4, 5, 7];
const n = weights.length;
console.log(knapSack(W, weights, values, n)); // 9
```

---

## 📌 4장. 동적 계획법의 장단점

| 장점                                                      | 단점                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------|
| - 중복 하위 문제를 한 번만 계산하여 **시간 복잡도** 대폭 감소      | - 문제 크기에 비례해 **메모리 사용** 증가 (dp 테이블 크기가 커질 수 있음)       |
| - 하위 문제의 솔루션을 저장(메모이제이션/테이블화) → **재활용**    | - 문제 구조에 따라 dp 테이블 설계가 **복잡**할 수 있음                   |
| - 최단 경로, 최적 스케줄링, 배낭 문제 등 **최적화 문제**에 광범위 적용 | - 재귀(Top-Down) 시 호출 스택 과다 사용으로 오버플로 위험                  |

---

## 📝 정리 및 요약
- 동적 계획법(DP)은 **최적 부분구조**와 **중복 하위 문제** 조건을 만족할 때 탁월한 성능을 발휘합니다.
- **하향식(Top-Down)**: 재귀 + 메모이제이션, **상향식(Bottom-Up)**: 반복문 + 테이블로 접근
- 피보나치, 최장 공통 부분 수열(LCS), 배낭 문제 등 다양한 예시로 DP를 학습할 수 있습니다.

이 문서를 통해 동적 계획법의 핵심 원리와 구현 방법을 숙지하시어, 복잡한 최적화 문제를 효율적으로 해결해 보시길 바랍니다.




1️⃣6️⃣ 탐욕 알고리즘(Greedy Algorithm)
# 📖 JavaScript 탐욕 알고리즘(Greedy Algorithm) 완벽 가이드

## 📌 1장. 탐욕 알고리즘의 기본 개념과 특징

### 🔹 탐욕 알고리즘(Greedy Algorithm)이란?
- 매 단계에서 **가장 최적이라고 생각되는 선택**(Greedy Choice)을 하는 알고리즘 설계 기법
- 전역적으로 최적해(Optimal Solution)에 도달하기 위해, 국소적으로 최적해(Local Optimum)를 반복해서 선택

### 🔹 필수 조건
1. **탐욕 선택 속성(Greedy Choice Property)**: 문제의 최적해가 각 단계에서의 국소적 최적 선택으로 구성되어야 함
2. **최적 부분구조(Optimal Substructure)**: 문제의 최적해가 하위 문제의 최적해로부터 구성 가능

### 🔹 장단점
| 장점 | 단점 |
| --- | --- |
| 구현이 간단하고 빠름 | 모든 문제에서 최적해 보장 X |
| 각 단계의 단순 계산 | 반례(예외 상황)에 취약 |

---

## 📌 2장. 대표적 사례

### 🔹 2.1 거스름돈 문제(Change-Making Problem)
- **문제**: 화폐 단위가 1, 5, 10, 50, 100, 500원 등으로 주어질 때, 거슬러 줄 금액을 최소 동전 개수로 지불
- **탐욕 선택**: **가장 큰 화폐 단위**부터 가능한 만큼 먼저 사용

#### 예시 코드 (동전 단위가 그리디 해를 보장하는 경우)
```javascript
function makeChange(amount, coins = [500, 100, 50, 10, 5, 1]) {
  const result = [];
  for (let coin of coins) {
    while (amount >= coin) {
      amount -= coin;
      result.push(coin);
    }
  }
  return result;
}

console.log(makeChange(1270)); // [500, 500, 100, 100, 50, 10, 10]
```

> 단, **화폐 단위가 불규칙**한 경우(예: 1, 3, 4원 동전 등) 탐욕적 접근으로는 최적해가 보장되지 않을 수 있습니다.

### 🔹 2.2 회의실 배정 문제(Activity Selection / Interval Scheduling)
- **문제**: 회의실 하나에 여러 회의가 신청되었을 때, **서로 겹치지 않게** 가장 많은 회의를 배정하기 위해 어떠한 기준으로 선택?
- **탐욕 선택**: 종료 시간이 가장 빠른 회의부터 선택 (종료 시간 기준 오름차순 정렬 후, 가능한 회의를 순차 선택)

#### 예시 코드
```javascript
function activitySelection(intervals) {
  // 종료 시간이 빠른 순으로 정렬
  intervals.sort((a, b) => a.end - b.end);

  let count = 0;
  let currentEnd = 0;

  for (let interval of intervals) {
    if (interval.start >= currentEnd) {
      count++;
      currentEnd = interval.end;
    }
  }

  return count;
}

const intervals = [
  { start: 1, end: 3 },
  { start: 2, end: 5 },
  { start: 4, end: 7 },
  { start: 1, end: 8 },
  { start: 5, end: 9 },
  { start: 8, end: 10 }
];

console.log(activitySelection(intervals)); // 3 (예: {1,3}, {4,7}, {8,10})
```

### 🔹 기타 예시
- **최소 신장 트리(MST)**의 Kruskal 알고리즘
  - 간선의 가중치를 기준으로 오름차순 정렬 후, 사이클이 생기지 않는 선에서 간선을 추가
- **허프만 코딩(Huffman Coding)**
  - 빈도가 가장 낮은 문자들을 묶어 트리를 구성해 압축 효율 극대화

---

## 📌 3장. 탐욕 알고리즘의 한계점

1. **부분적 최적 해 선택**이 전체 문제의 **전역적 최적해**를 보장하지 않는 경우가 많음
2. 탐욕 알고리즘으로 접근 시, **반례(Counter Example)**가 존재할 수 있음
3. 문제 구조가 탐욕 선택 속성을 만족해야만 최적해 보장 가능

예시:
- **화폐 단위가 불규칙**한 거스름돈 문제
- **배낭 문제(Knapsack Problem)** 중 0/1 배낭 문제는 탐욕적 접근으로 최적해를 보장하지 않음 (단, 분할 가능한 배낭 문제(Fractional Knapsack)는 탐욕이 유효)

---

## 📝 정리 및 요약
- 탐욕 알고리즘은 매 단계에서 최적으로 보이는 선택을 반복하며, 구현이 간단하고 빠른 계산이 장점
- **탐욕 선택 속성**과 **최적 부분구조**를 만족하는 문제에서 최적해를 제공
- 대표적 사례로 거스름돈 문제(특정 화폐 단위), 회의실 배정 문제, MST(Kruskal), 허프만 코딩 등을 들 수 있음
- 그러나 모든 최적화 문제에서 통하지 않으며, 반례가 존재할 수 있음을 유의

이 문서를 통해 탐욕 알고리즘의 원리와 적용 예시를 이해하시어, 문제에 따라 탐욕적 해법이 올바른지 판단하고 적용해 보시기 바랍니다.



1️⃣7️⃣ 백트래킹(Backtracking)

# 📖 JavaScript 백트래킹(Backtracking) 완벽 가이드

## 📌 1장. 백트래킹(Backtracking)의 개념과 원리

### 🔹 백트래킹이란?
- **완전 탐색(Brute Force)** 접근을 최적화한 기법으로, 가능한 해답 후보를 **체계적으로 탐색**하면서 정답이 될 수 없는 경우 **되돌아(Backtrack)** 나오는 방법
- 재귀(Recursion)를 기반으로, 유효하지 않은 해 또는 이미 탐색할 필요가 없는 경로는 미리 가지치기(Pruning)를 통해 제거

### 🔹 작동 방식
1. **해 후보(Candidate)**를 단계별로 선택하며 해를 구성
2. 각 단계에서 **유효성 검사(Constraint Check)** 진행
3. 유효하지 않은 경우, 해당 경로를 포기(Backtrack)하고 다른 경로 탐색
4. 가능한 모든 경로를 살펴본 후, 최적해 혹은 모든 해를 도출

---

## 📌 2장. 재귀를 이용한 백트래킹 구현 방법

1. **결정 트리(Decision Tree)**를 구성: 각 단계에서 선택할 수 있는 여러 후보
2. **재귀 함수**로 구현:
   - 파라미터로 현재까지의 경로(상태), 단계 인덱스 등 전달
   - 기저 사례(Base Case) 도달 시, 해답을 확인하거나 기록
3. **가지치기(Pruning)**:
   - 현재 상태가 **유효성**을 위반하면 더 이상 재귀 호출을 진행하지 않고 중단
   - 불필요한 연산을 줄여 탐색 효율을 향상

---

## 📌 3장. 대표적 백트래킹 문제

### 🔹 3.1 N-Queen 문제
- **문제**: N x N 체스판에 퀸(N개의 퀸)을 놓되, 서로 공격할 수 없는 위치에 배치하는 모든 경우의 수를 찾거나, 하나의 해를 찾는 문제
- **백트래킹 방법**: 한 행(혹은 열)씩 퀸을 놓고, **이전 행들의 퀸과 충돌**이 나는지 검사. 충돌이면 배치 불가능

```javascript
function solveNQueens(n) {
  const results = [];
  const board = Array(n).fill(-1); // index = row, value = col

  function isValid(row, col) {
    for (let r = 0; r < row; r++) {
      const c = board[r];
      // 같은 열 or 대각선 검사
      if (c === col || Math.abs(row - r) === Math.abs(col - c)) {
        return false;
      }
    }
    return true;
  }

  function backtrack(row) {
    if (row === n) {
      // 모든 행에 퀸 배치 성공
      results.push([...board]);
      return;
    }
    for (let col = 0; col < n; col++) {
      if (isValid(row, col)) {
        board[row] = col;
        backtrack(row + 1);
        board[row] = -1; // backtrack
      }
    }
  }

  backtrack(0);
  return results;
}

console.log(solveNQueens(4));
// 예시 출력: 모든 해들의 퀸 위치
```

### 🔹 3.2 미로찾기 문제(Maze)
- **문제**: 2차원 미로에서 출발점부터 도착점까지 이동 경로를 찾는 문제
- **백트래킹 방법**:
  - 현재 위치에서 상하좌우(또는 8방향)로 이동
  - 벽이거나 이미 방문한 칸은 배제
  - 목적지 도달 시 경로 완성

```javascript
function findPath(maze, start, end) {
  const rows = maze.length;
  const cols = maze[0].length;
  const visited = Array.from({ length: rows }, () => Array(cols).fill(false));
  const path = [];

  function backtrack(r, c) {
    if (r < 0 || c < 0 || r >= rows || c >= cols) return false;
    if (maze[r][c] === 1 || visited[r][c]) return false; // 1은 벽

    path.push([r, c]);
    visited[r][c] = true;

    if (r === end[0] && c === end[1]) {
      return true; // 목적지 도달
    }

    // 상하좌우 이동 시도
    if (
      backtrack(r - 1, c) ||
      backtrack(r + 1, c) ||
      backtrack(r, c - 1) ||
      backtrack(r, c + 1)
    ) {
      return true;
    }

    // 되돌아가기
    path.pop();
    return false;
  }

  backtrack(start[0], start[1]);
  return path; // 목표점까지의 경로, 없으면 빈 배열
}

// 예시
const maze = [
  [0, 1, 0, 0],
  [0, 0, 0, 1],
  [1, 0, 0, 0],
  [0, 0, 1, 0]
];
const start = [0, 0];
const end = [3, 3];
console.log(findPath(maze, start, end));
```

### 🔹 3.3 스도쿠(Sudoku)
- **문제**: 9x9 스도쿠 퍼즐에서 미완성 칸을 채우되, 가로/세로/3x3 박스에 1~9가 중복되지 않아야 함
- **백트래킹 방법**: 한 칸씩 숫자를 채워 넣으며, **유효성 검사** 후 문제 해결까지 시도

```javascript
function solveSudoku(board) {
  function isValid(board, row, col, num) {
    // 행, 열 검사
    for (let i = 0; i < 9; i++) {
      if (board[row][i] === num || board[i][col] === num) {
        return false;
      }
    }

    // 3x3 박스 검사
    const boxRow = Math.floor(row / 3) * 3;
    const boxCol = Math.floor(col / 3) * 3;
    for (let r = 0; r < 3; r++) {
      for (let c = 0; c < 3; c++) {
        if (board[boxRow + r][boxCol + c] === num) {
          return false;
        }
      }
    }

    return true;
  }

  function backtrack() {
    for (let r = 0; r < 9; r++) {
      for (let c = 0; c < 9; c++) {
        if (board[r][c] === 0) {
          // 1~9 시도
          for (let num = 1; num <= 9; num++) {
            if (isValid(board, r, c, num)) {
              board[r][c] = num;
              if (backtrack()) {
                return true;
              }
              board[r][c] = 0; // backtrack
            }
          }
          return false; // 어떤 숫자도 못 넣었으므로 실패
        }
      }
    }
    return true; // 모든 칸이 채워짐
  }

  backtrack();
  return board;
}

// 예시: 스도쿠 퍼즐에서 0은 미완성 칸
let board = [
  [5, 3, 0, 0, 7, 0, 0, 0, 0],
  [6, 0, 0, 1, 9, 5, 0, 0, 0],
  [0, 9, 8, 0, 0, 0, 0, 6, 0],
  [8, 0, 0, 0, 6, 0, 0, 0, 3],
  [4, 0, 0, 8, 0, 3, 0, 0, 1],
  [7, 0, 0, 0, 2, 0, 0, 0, 6],
  [0, 6, 0, 0, 0, 0, 2, 8, 0],
  [0, 0, 0, 4, 1, 9, 0, 0, 5],
  [0, 0, 0, 0, 8, 0, 0, 7, 9]
];

console.log(solveSudoku(board));
```

---

## 📝 정리 및 요약
- 백트래킹은 재귀 기반의 완전 탐색 방식에서, **유효하지 않은 해**를 미리 배제하여 탐색 효율을 높이는 기법
- N-Queen, 미로 찾기, 스도쿠 등 **제약 조건**이 있는 문제를 해결할 때 자주 사용
- 문제마다 **가지치기(Pruning) 로직**을 잘 설계하면 실행 시간을 대폭 단축할 수 있음

이 문서를 통해 백트래킹의 개념과 구현 원리를 이해하고, 각종 퍼즐 및 탐색 문제에서 자유롭게 응용해 보시길 바랍니다.





1️⃣8️⃣ 그래프 알고리즘(Graph Algorithms) 심화

# 📖 JavaScript 그래프 알고리즘(Graph Algorithms) 심화 가이드

## 📌 1장. 최소 스패닝 트리(Minimum Spanning Tree)

### 🔹 개념
- **스패닝 트리(Spanning Tree)**: 무방향 연결 그래프(connected graph)에서, 모든 정점을 포함하면서 간선 수가 (정점 수 - 1)인 트리 구조
- **최소 스패닝 트리(MST)**: 스패닝 트리 중 **간선 가중치의 합**이 최소가 되는 트리
- 대표 알고리즘: **Kruskal**, **Prim**

### 🔹 Kruskal 알고리즘
- 간선을 가중치 오름차순으로 정렬 후, 사이클(순환)이 생기지 않는 한에서 간선을 추가
- **Union-Find(Disjoint Set)** 자료구조를 사용하여 사이클 여부 검사

#### 알고리즘 절차
1. 간선을 가중치 기준 오름차순 정렬
2. 가장 가중치가 낮은 간선부터 순차적으로 선택
3. 현재 간선을 추가했을 때 **사이클**이 생성되는지 확인
   - Union-Find 자료구조로 검사
4. 사이클이 없다면 MST 집합에 추가
5. 모든 정점이 연결될 때까지(간선 수 = V-1) 반복

#### 시간 복잡도: O(E log E) (간선 정렬 시간이 지배적)

##### Kruskal 구현 예시
```javascript
class UnionFind {
  constructor(n) {
    this.parent = Array.from({ length: n }, (_, i) => i);
    this.rank = Array(n).fill(0);
  }

  find(x) {
    if (this.parent[x] !== x) {
      this.parent[x] = this.find(this.parent[x]);
    }
    return this.parent[x];
  }

  union(a, b) {
    const rootA = this.find(a);
    const rootB = this.find(b);

    if (rootA !== rootB) {
      if (this.rank[rootA] > this.rank[rootB]) {
        this.parent[rootB] = rootA;
      } else if (this.rank[rootA] < this.rank[rootB]) {
        this.parent[rootA] = rootB;
      } else {
        this.parent[rootB] = rootA;
        this.rank[rootA] += 1;
      }
      return true;
    }
    return false;
  }
}

function kruskalMST(vertices, edges) {
  // vertices: 정점 개수, edges: [ [u, v, weight], ... ]
  // 1) 간선을 가중치 오름차순 정렬
  edges.sort((a, b) => a[2] - b[2]);

  const uf = new UnionFind(vertices);
  const mst = [];
  let cost = 0;

  for (let [u, v, w] of edges) {
    // 2) 사이클이 형성되지 않으면 MST에 포함
    if (uf.union(u, v)) {
      mst.push([u, v, w]);
      cost += w;
      if (mst.length === vertices - 1) break;
    }
  }

  return { mst, cost };
}

// 사용 예시
const vertices = 5; // 0 ~ 4
const edges = [
  [0, 1, 2],
  [0, 3, 6],
  [1, 3, 8],
  [1, 2, 3],
  [1, 4, 5],
  [2, 4, 7]
];

const result = kruskalMST(vertices, edges);
console.log(result.mst); // MST 간선 목록
console.log(result.cost); // MST 전체 가중치
```

### 🔹 Prim 알고리즘
- 임의의 정점에서 시작해, **MST에 속한 정점**과 **속하지 않은 정점** 사이의 간선 중 최소 가중치 간선을 선택해 MST에 추가
- 우선순위 큐(최소 힙)를 사용하면 효율적으로 구현 가능

#### 알고리즘 절차
1. 임의의 시작 정점을 MST 집합에 추가
2. MST 내부 정점과 MST 외부 정점을 연결하는 간선 중 **가장 낮은 가중치**를 가진 간선을 MST에 추가
3. MST에 새 정점이 추가될 때마다, 해당 정점과 연결된 간선을 우선순위 큐에 추가
4. MST에 정점이 V개 포함될 때까지 반복

#### 시간 복잡도: O(E log V)

##### Prim 구현 예시 (인접 리스트 + 우선순위 큐)
```javascript
class MinHeap {
  constructor() {
    this.heap = [];
  }

  push(edge) {
    this.heap.push(edge);
    this.bubbleUp();
  }

  pop() {
    if (this.heap.length === 0) return null;
    const top = this.heap[0];
    const end = this.heap.pop();
    if (this.heap.length > 0) {
      this.heap[0] = end;
      this.sinkDown(0);
    }
    return top;
  }

  bubbleUp() {
    let index = this.heap.length - 1;
    const element = this.heap[index];
    while (index > 0) {
      let parentIndex = Math.floor((index - 1) / 2);
      let parent = this.heap[parentIndex];
      if (element[1] >= parent[1]) break; // weight 비교
      this.heap[index] = parent;
      index = parentIndex;
    }
    this.heap[index] = element;
  }

  sinkDown(index) {
    const length = this.heap.length;
    const element = this.heap[index];

    while (true) {
      let leftIdx = 2 * index + 1;
      let rightIdx = 2 * index + 2;
      let swap = null;

      if (leftIdx < length) {
        if (this.heap[leftIdx][1] < element[1]) {
          swap = leftIdx;
        }
      }
      if (rightIdx < length) {
        if (
          (swap === null && this.heap[rightIdx][1] < element[1]) ||
          (swap !== null && this.heap[rightIdx][1] < this.heap[leftIdx][1])
        ) {
          swap = rightIdx;
        }
      }
      if (swap === null) break;
      this.heap[index] = this.heap[swap];
      index = swap;
    }
    this.heap[index] = element;
  }
}

function primMST(adjList, start = 0) {
  // adjList: { vertex: [ [neighbor, weight], ... ], ... }
  const n = Object.keys(adjList).length;
  const visited = new Array(n).fill(false);
  const heap = new MinHeap();

  visited[start] = true;
  for (let [next, w] of adjList[start]) {
    heap.push([next, w, start]); // [도착점, 가중치, 시작점]
  }

  const mst = [];
  let edgeCount = 0;
  let totalCost = 0;

  while (edgeCount < n - 1) {
    let edge = heap.pop();
    if (!edge) break; // 간선이 더 이상 없음

    const [v, w, u] = edge;
    if (visited[v]) continue; // 이미 방문한 정점

    // MST에 간선 추가
    visited[v] = true;
    mst.push([u, v, w]);
    totalCost += w;
    edgeCount++;

    // 새로운 정점 v에 연결된 간선들 추가
    for (let [next, weight] of adjList[v]) {
      if (!visited[next]) {
        heap.push([next, weight, v]);
      }
    }
  }

  return { mst, totalCost };
}

// 사용 예시
const graph = {
  0: [[1, 2], [3, 6]],
  1: [[0, 2], [2, 3], [3, 8], [4, 5]],
  2: [[1, 3], [4, 7]],
  3: [[0, 6], [1, 8]],
  4: [[1, 5], [2, 7]]
};

const primResult = primMST(graph, 0);
console.log(primResult.mst); // MST 간선 목록
console.log(primResult.totalCost); // MST 전체 가중치
```

---

## 📌 2장. 최단 경로 알고리즘(Shortest Path)

### 🔹 Dijkstra 알고리즘
- **하나의 시작 정점**에서 다른 모든 정점까지의 **최단 경로**를 구하는 알고리즘
- 간선 가중치가 **음수가 아닌** 경우에만 사용 가능
- 우선순위 큐 사용 시 시간 복잡도 O(E log V)

#### 구현 예시
```javascript
function dijkstra(adjList, start) {
  const n = Object.keys(adjList).length;
  const dist = Array(n).fill(Infinity);
  dist[start] = 0;

  const visited = Array(n).fill(false);
  const heap = new MinHeap();
  heap.push([start, 0]); // [정점, 거리]

  while (true) {
    const edge = heap.pop();
    if (!edge) break;

    const [u, currentDist] = edge;
    if (visited[u]) continue;
    visited[u] = true;

    for (let [v, w] of adjList[u]) {
      if (!visited[v] && dist[u] + w < dist[v]) {
        dist[v] = dist[u] + w;
        heap.push([v, dist[v]]);
      }
    }
  }

  return dist;
}

// 사용 예시
const graphDijkstra = {
  0: [[1, 2], [2, 4]],
  1: [[2, 1], [3, 7]],
  2: [[3, 1]],
  3: []
};

console.log(dijkstra(graphDijkstra, 0)); // [0, 2, 3, 4] 등
```

### 🔹 Floyd-Warshall 알고리즘
- **모든 정점 쌍** 사이의 최단 경로를 구하는 알고리즘
- 간선 가중치가 음수여도 사용 가능하지만, **음의 사이클(negative cycle)**은 처리 불가
- 인접 행렬(2차원 배열)로 구현

#### 시간 복잡도: O(V^3)

#### 알고리즘 절차
1. dist[i][j]를 간선 (i→j)의 가중치로 초기화(직접 간선이 없으면 ∞)
2. 모든 정점 k에 대해, dist[i][j] = min(dist[i][j], dist[i][k] + dist[k][j]) 반복

```javascript
function floydWarshall(matrix) {
  const n = matrix.length;
  const dist = matrix.map(row => row.slice()); // 깊은 복사

  for (let k = 0; k < n; k++) {
    for (let i = 0; i < n; i++) {
      for (let j = 0; j < n; j++) {
        if (dist[i][k] + dist[k][j] < dist[i][j]) {
          dist[i][j] = dist[i][k] + dist[k][j];
        }
      }
    }
  }

  return dist;
}

// 예시
const INF = Infinity;
const matrix = [
  [0,   5,   INF, 8],
  [7,   0,   9,   INF],
  [2,   INF, 0,   4],
  [INF, INF, INF, 0]
];

const resultFW = floydWarshall(matrix);
console.log(resultFW);
```

---

## 📌 3장. 위상 정렬(Topological Sort)

### 🔹 개념
- **방향 그래프(Directed Graph)**에서, 정점들의 순서를 위배하지 않도록 나열하는 것
- **선행 관계(Dependency)**가 있는 작업을 차례로 수행할 때 사용
- 그래프에 **사이클이 없어야(DAG: Directed Acyclic Graph)** 위상 정렬이 가능

### 🔹 구현 방법
1. **진입 차수(In-degree)**가 0인 정점을 큐에 넣음
2. 큐에서 정점을 꺼내며, 해당 정점과 연결된 간선을 제거(연결된 노드의 진입 차수 감소)
3. 진입 차수가 0이 된 정점을 큐에 삽입
4. 큐가 빌 때까지 반복, 꺼낸 순서가 위상 정렬의 결과

#### 코드 예시
```javascript
function topologicalSort(V, edges) {
  // V: 정점 개수, edges: [ [u, v], ... ] (u -> v)
  const adjList = Array.from({ length: V }, () => []);
  const inDegree = Array(V).fill(0);

  // 인접 리스트 및 진입 차수 계산
  for (let [u, v] of edges) {
    adjList[u].push(v);
    inDegree[v]++;
  }

  // 진입 차수 0인 정점 큐에 삽입
  const queue = [];
  for (let i = 0; i < V; i++) {
    if (inDegree[i] === 0) {
      queue.push(i);
    }
  }

  const result = [];

  while (queue.length) {
    const node = queue.shift();
    result.push(node);

    // 연결된 정점의 진입 차수 감소
    for (let neighbor of adjList[node]) {
      inDegree[neighbor]--;
      if (inDegree[neighbor] === 0) {
        queue.push(neighbor);
      }
    }
  }

  // 모든 정점을 처리하지 못하면 사이클 존재
  if (result.length < V) {
    throw new Error("Cycle detected in the graph!");
  }

  return result;
}

// 사용 예시
const V = 6;
const edgesTS = [
  [5, 2],
  [5, 0],
  [4, 0],
  [4, 1],
  [2, 3],
  [3, 1]
];

console.log(topologicalSort(V, edgesTS)); // [5, 4, 2, 3, 1, 0] 등
```

---

## 📝 정리 및 요약
- **최소 스패닝 트리(MST)**
  - Kruskal: 간선 정렬 + Union-Find
  - Prim: 임의 정점 시작 + 최소 간선 선택
- **최단 경로**
  - Dijkstra: 음이 아닌 가중치, 단일 출발 최단 경로
  - Floyd-Warshall: 모든 쌍 최단 경로, O(V^3)
- **위상 정렬(Topological Sort)**: DAG(Directed Acyclic Graph)에서 선행 순서를 지키며 정점을 나열

이 가이드를 통해 그래프 알고리즘의 심화 개념을 익히시고, 다양한 문제(네트워크, 지도, 스케줄링, 의존 관계 등)에서 효과적으로 적용해 보시길 바랍니다.





📕 PART 5. 고급 알고리즘 및 기타 이론
1️⃣9️⃣ 문자열 알고리즘

# 📖 JavaScript 문자열 알고리즘 완벽 가이드

## 📌 1장. 문자열 탐색 및 매칭

문자열 매칭 알고리즘은 큰 텍스트(Text) 내에서 특정 패턴(Pattern)을 효율적으로 찾는 방법을 연구합니다. 대표적인 알고리즘으로는 **KMP(Knuth-Morris-Pratt)**와 **Rabin-Karp**가 있습니다.

---

## 1. KMP 알고리즘 (Knuth-Morris-Pratt)

### 🔹 개념
- **KMP 알고리즘**은 문자열 탐색 과정에서, **부분적으로 일치한 상태**를 효율적으로 활용하여 불필요한 비교를 줄입니다.
- 패턴 내에서 반복되는 접두사와 접미사의 정보를 사전에 계산한 **파이(π) 테이블**(또는 LPS: Longest Prefix Suffix array)을 사용
- 시간 복잡도: **O(n + m)** (n: 텍스트 길이, m: 패턴 길이)

### 🔹 LPS(파이) 배열 계산
- 패턴의 각 위치에서 **가장 긴 접두사(prefix) == 접미사(suffix)** 길이를 기록
- 매칭이 실패했을 때, **LPS 배열**을 참조해 옮길 위치를 결정

```javascript
function computeLPS(pattern) {
  const lps = new Array(pattern.length).fill(0);
  let prefixEnd = 0;
  let i = 1;

  while (i < pattern.length) {
    if (pattern[i] === pattern[prefixEnd]) {
      prefixEnd++;
      lps[i] = prefixEnd;
      i++;
    } else {
      if (prefixEnd !== 0) {
        prefixEnd = lps[prefixEnd - 1];
      } else {
        lps[i] = 0;
        i++;
      }
    }
  }

  return lps;
}

function kmpSearch(text, pattern) {
  if (pattern.length === 0) return 0; // 빈 패턴은 0번 인덱스부터 매칭

  const lps = computeLPS(pattern);
  let i = 0; // text index
  let j = 0; // pattern index

  while (i < text.length) {
    if (text[i] === pattern[j]) {
      i++;
      j++;

      if (j === pattern.length) {
        return i - j; // 매칭 시작 인덱스
      }
    } else {
      if (j !== 0) {
        j = lps[j - 1];
      } else {
        i++;
      }
    }
  }

  return -1; // 매칭 실패
}

// 사용 예시
const text = "ABXABABCABABDAABAB";
const pattern = "ABABCABAB";
console.log(kmpSearch(text, pattern)); // 패턴 시작 인덱스(예: 2)
```

---

## 2. 라빈-카프(Rabin-Karp) 알고리즘

### 🔹 개념
- **해시 기법**을 사용하여 패턴의 해시값과 텍스트의 **슬라이딩 윈도우** 해시값을 비교
- 해시 충돌이 발생할 수 있으므로, **충돌 발생 시 직접 문자열 비교**로 확인

### 🔹 시간 복잡도
- 평균 **O(n + m)**, 최악 **O(n*m)** (충돌이 자주 발생하는 경우)

### 🔹 구현 예시
```javascript
function rabinKarpSearch(text, pattern) {
  const base = 256; // 해시를 계산할 때 사용할 진법 (가령 ASCII 256)
  const mod = 101; // 해시를 나눌 소수
  const n = text.length;
  const m = pattern.length;
  if (m === 0) return 0;

  let patternHash = 0;
  let windowHash = 0;
  let h = 1; // (base^(m-1)) % mod

  // h 계산 (슬라이딩 윈도우 이동 시 사용)
  for (let i = 0; i < m - 1; i++) {
    h = (h * base) % mod;
  }

  // 패턴과 첫 윈도우의 해시 값 계산
  for (let i = 0; i < m; i++) {
    patternHash = (patternHash * base + pattern.charCodeAt(i)) % mod;
    windowHash = (windowHash * base + text.charCodeAt(i)) % mod;
  }

  // 슬라이딩 윈도우를 이동하며 비교
  for (let s = 0; s <= n - m; s++) {
    // 해시가 일치하면 실제 문자열도 비교
    if (patternHash === windowHash) {
      let match = true;
      for (let j = 0; j < m; j++) {
        if (text[s + j] !== pattern[j]) {
          match = false;
          break;
        }
      }
      if (match) {
        return s;
      }
    }

    // 다음 윈도우의 해시값 업데이트
    if (s < n - m) {
      windowHash = (
        (windowHash - text.charCodeAt(s) * h) * base +
        text.charCodeAt(s + m)
      ) % mod;
      if (windowHash < 0) {
        windowHash += mod;
      }
    }
  }

  return -1;
}

// 사용 예시
const textRK = "ABXABABCABABDAABAB";
const patternRK = "ABABCABAB";
console.log(rabinKarpSearch(textRK, patternRK)); // 인덱스
```

---

## 📌 2장. 트라이(Trie) 자료구조

### 🔹 개념
- **문자열 집합**을 효율적으로 저장하고 검색하기 위한 **트리(Tree)** 기반 자료구조
- 각 노드가 **문자**를 나타내며, 루트에서부터 특정 경로를 따라가면 문자열 1개가 완성

### 🔹 특징
1. 문자열 검색 시간: O(m) (m: 문자열 길이)
2. 공통 접두사를 공유하기 때문에, 문자열 집합이 많을 때 효율적
3. 구현이 다소 복잡하며, 대문자/소문자/특수문자 등 **알파벳 크기**에 따라 공간 사용량 달라짐

### 🔹 트라이 구현 예시
```javascript
class TrieNode {
  constructor() {
    this.children = {}; // { char: TrieNode }
    this.isEnd = false; // 단어의 끝 지점 표시
  }
}

class Trie {
  constructor() {
    this.root = new TrieNode();
  }

  insert(word) {
    let current = this.root;
    for (let char of word) {
      if (!current.children[char]) {
        current.children[char] = new TrieNode();
      }
      current = current.children[char];
    }
    current.isEnd = true;
  }

  search(word) {
    let current = this.root;
    for (let char of word) {
      if (!current.children[char]) {
        return false;
      }
      current = current.children[char];
    }
    return current.isEnd;
  }

  startsWith(prefix) {
    let current = this.root;
    for (let char of prefix) {
      if (!current.children[char]) {
        return false;
      }
      current = current.children[char];
    }
    return true;
  }
}

// 사용 예시
const trie = new Trie();
trie.insert("apple");
trie.insert("app");
console.log(trie.search("apple"));  // true
console.log(trie.search("app"));    // true
console.log(trie.search("apex"));   // false
console.log(trie.startsWith("ap")); // true
```

---

## 📝 정리 및 요약
- 문자열 탐색 알고리즘:
  - **KMP**: 접두사/접미사 정보를 미리 계산해 O(n + m) 시간에 탐색
  - **라빈-카프**: 해시를 이용한 평균 O(n + m) 탐색, 하지만 최악 O(n*m)
- **트라이(Trie)**: 문자열 집합 관리에 특화된 트리 구조
  - 접두사 검색, 자동완성 기능 등에서 유용
  - 문자열 개수와 평균 길이에 따라 상당한 메모리 사용 가능

이 문서를 통해 문자열 관련 알고리즘과 자료구조를 숙지하시고, 필요한 문제 상황에 맞춰 효율적으로 적용할 수 있길 바랍니다.





2️⃣0️⃣ 비트 연산(Bitwise Operations)

# 📖 JavaScript 비트 연산(Bitwise Operations) 가이드

## 📌 1장. 비트 연산 기본 개념

### 🔹 비트 연산이란?
- 정수를 **2진수(Binray)** 형태로 해석하여, 각 자릿수별로 논리적 연산(AND, OR, XOR 등)이나 시프트(Shift)를 수행
- 프로그래밍에서 숫자를 효율적으로 다루거나, 특정 비트만을 조작할 때 사용
- 저수준 단위의 조작이 필요할 때 매우 유용 (예: 권한 처리, 상태 표시, 압축된 자료 구조)

### 🔹 자바스크립트에서의 정수 처리
- JavaScript의 숫자는 기본적으로 **배정밀도 부동소수점(64비트)**을 사용
- **비트 연산** 시 내부적으로 **32비트 정수**로 변환하여 계산 후, 다시 64비트 부동소수점으로 변환
- 이로 인해 매우 큰 정수에 대해 비트 연산을 수행하면 정밀도 손실이 발생할 수 있음

---

## 📌 2장. 자바스크립트 주요 비트 연산자

| 연산자 | 설명                         | 예시 (x = 5(0101), y = 3(0011)) |
|--------|-----------------------------|------------------------------------|
| `&`    | **비트 AND**                | (5 & 3) = 1 (0001)                 |
| `|`    | **비트 OR**                 | (5 \| 3) = 7 (0111)                 |
| `^`    | **비트 XOR**                | (5 ^ 3) = 6 (0110)                 |
| `~`    | **비트 NOT(보수)**          | (~5) = -6 (보수는 -1 - n)           |
| `<<`   | **왼쪽 시프트**              | (5 << 1) = 10 (1010)               |
| `>>`   | **오른쪽 시프트** (부호 유지) | (5 >> 1) = 2 (0010)                 |
| `>>>`  | **부호 없는 오른쪽 시프트**   | (5 >>> 1) = 2 (0010)                |

### 🔹 시프트(Shift)
- `<<`: 왼쪽 시프트 → 오른쪽으로 0이 채워짐
- `>>`: 부호 있는 오른쪽 시프트 → 최상위 비트(부호 비트) 복사
- `>>>`: 부호 없는 오른쪽 시프트 → 최상위 비트에 0 채워짐 (모두 양수로 처리)

### 🔹 음수의 비트 표현
- 32비트 정수에서 **2의 보수(2's complement)** 형태로 표현
- 예: -6을 32비트 이진으로 표현하면, `1111...1010` 형태

---

## 📌 3장. 비트마스크(Bitmask) 활용 사례

**비트마스크**: 여러 상태나 정보를 1비트씩 사용하여 압축적으로 표현하는 방식

### 1. 권한/접근 제어 (예: Unix 파일 권한)
- `rwx`(읽기, 쓰기, 실행)를 각각 1비트로 나타냄
- 예: 0b100(4) = 읽기만 가능, 0b110(6) = 읽기/쓰기 가능 등

```javascript
const READ = 1 << 2;  // 0b100
const WRITE = 1 << 1; // 0b010
const EXEC = 1 << 0;  // 0b001

let permission = READ | WRITE; // 0b110

function canRead(p) {
  return (p & READ) !== 0;
}

function canWrite(p) {
  return (p & WRITE) !== 0;
}

console.log(canRead(permission));  // true
console.log(canWrite(permission)); // true
console.log(permission & EXEC);    // 0, 실행 권한 없음
```

### 2. 부분 집합 처리
- n개의 원소가 있을 때, 각 원소의 포함 여부(1=포함, 0=불포함)를 n비트로 표현
- 예: `1010₂` = {1, 3}번 원소 포함

```javascript
function subsets(arr) {
  const result = [];
  const n = arr.length;

  for (let mask = 0; mask < (1 << n); mask++) {
    const subset = [];
    for (let i = 0; i < n; i++) {
      if (mask & (1 << i)) {
        subset.push(arr[i]);
      }
    }
    result.push(subset);
  }

  return result;
}

console.log(subsets(["a", "b", "c"]));
// 예: [ [], [ 'a' ], [ 'b' ], [ 'a', 'b' ], [ 'c' ], ...]
```

### 3. 상태 압축 DP
- 동적 계획법(DP)에서, 여러 요소의 상태를 비트로 압축해 관리 (예: 방문한 도시 집합)
- 예: TSP(Traveling Salesman Problem)에서 방문 상태를 bitmask로 표현

---

## 📌 4장. 주의사항 및 팁
1. **자바스크립트**에서는 **비트 연산 시 32비트 정수**로 변환
   - 매우 큰 정수에 대한 비트 연산은 예기치 않은 결과 가능
2. **음수 처리**에 유의
   - `>>>` 연산자를 사용하면 음수가 양수로 변환 (2의 보수 해석이 사라짐)
3. **비트 우선순위**
   - `~` > `<<`, `>>`, `>>>` > `&` > `^` > `|`
4. **효율적**: 비트마스크 사용 시, O(1)로 특정 조건 체크/추가/삭제 가능

---

## 📝 정리 및 요약
- **비트 연산**은 논리/시프트 연산으로 정수의 각 비트를 직접 조작하는 기능을 제공, JavaScript에서는 내부적으로 32비트 정수로 변환
- **비트마스크(Bitmask)**는 여러 상태를 한 번에 표현하고 관리하는 효율적인 기법
  - 권한 제어, 부분 집합 탐색, 상태 압축 DP 등 다양한 곳에서 활용
- 높은 성능과 간결한 상태 표현이 가능하지만, 대규모 비트마스크나 음수 처리에는 주의해야 합니다.

이 문서를 통해 비트 연산과 비트마스크의 개념을 충분히 이해하셔서, 실제 프로젝트나 알고리즘 문제에서 효율적으로 이용해 보시기 바랍니다.





2️⃣1️⃣ 고급 자료구조

# 📖 고급 자료구조 가이드: 세그먼트 트리(Segment Tree)와 펜윅 트리(Fenwick Tree)

## 📌 1장. 세그먼트 트리(Segment Tree)

### 🔹 개념
- **세그먼트 트리(Segment Tree)**는 배열과 같은 선형 자료구조에 대해, **구간 쿼리(Range Query)**와 **구간 업데이트**를 효율적으로 처리하기 위한 트리 자료구조입니다.
- 예: 합, 최소/최대, GCD, XOR 등 다양한 구간 연산을 빠르게 수행 가능.
- 트리의 각 노드는 배열의 특정 구간을 대표하며, 자식 노드들은 그 구간을 절반으로 나눈 하위 구간을 대표.

### 🔹 동작 원리
1. **트리 구성(Build)**: 배열을 기반으로 세그먼트 트리를 재귀적으로 구성
   - 루트 노드는 전체 구간 [0..n-1]
   - 재귀적으로 왼쪽 자식 노드는 [start..mid], 오른쪽 자식 노드는 [mid+1..end]
   - 각 노드는 해당 구간의 연산(합, 최솟값, 최댓값 등) 결과를 저장.
2. **구간 쿼리(Query)**: 원하는 구간이 노드 구간과 완전히 겹칠 경우 노드 값을 반환, 겹치지 않으면 무시, 부분 겹치면 자식 노드 탐색
3. **구간 업데이트(Update)**: 특정 인덱스(또는 구간)를 업데이트하고, 트리 경로를 따라 부모 노드까지 갱신

### 🔹 시간 복잡도
- 트리 구성(Build): O(n)
- 구간 쿼리 / 업데이트: O(log n)

### 🔹 예시: 구간 합 세그먼트 트리
```javascript
class SegmentTree {
  constructor(arr) {
    this.n = arr.length;
    // 세그먼트 트리는 최대 4*n 크기의 배열이 필요
    this.tree = new Array(this.n * 4).fill(0);
    this.build(arr, 1, 0, this.n - 1);
  }

  // node: 현재 노드 인덱스
  // start, end: arr의 구간 범위
  build(arr, node, start, end) {
    if (start === end) {
      // 리프 노드
      this.tree[node] = arr[start];
    } else {
      const mid = Math.floor((start + end) / 2);
      // 왼쪽 자식
      this.build(arr, node * 2, start, mid);
      // 오른쪽 자식
      this.build(arr, node * 2 + 1, mid + 1, end);
      // 부모 노드는 자식 노드의 합
      this.tree[node] = this.tree[node * 2] + this.tree[node * 2 + 1];
    }
  }

  // 구간 합 쿼리
  // left, right: 구하고자 하는 구간 범위
  query(node, start, end, left, right) {
    if (right < start || end < left) {
      // 범위 밖
      return 0;
    }
    if (left <= start && end <= right) {
      // 완전히 포함되는 구간
      return this.tree[node];
    }
    const mid = Math.floor((start + end) / 2);
    const sumLeft = this.query(node * 2, start, mid, left, right);
    const sumRight = this.query(node * 2 + 1, mid + 1, end, left, right);
    return sumLeft + sumRight;
  }

  // 단일 인덱스 업데이트 (arr[idx] = val)
  update(node, start, end, idx, val) {
    if (idx < start || idx > end) {
      // 범위 밖
      return;
    }
    if (start === end) {
      // 리프 노드
      this.tree[node] = val;
      return;
    }
    const mid = Math.floor((start + end) / 2);
    this.update(node * 2, start, mid, idx, val);
    this.update(node * 2 + 1, mid + 1, end, idx, val);
    this.tree[node] = this.tree[node * 2] + this.tree[node * 2 + 1];
  }

  getRangeSum(left, right) {
    return this.query(1, 0, this.n - 1, left, right);
  }

  updateValue(idx, val) {
    this.update(1, 0, this.n - 1, idx, val);
  }
}

// 사용 예시
const arr = [1, 3, 5, 7, 9, 11];
const segTree = new SegmentTree(arr);
console.log(segTree.getRangeSum(1, 3)); // 3 + 5 + 7 = 15

segTree.updateValue(1, 10); // arr[1] = 10
console.log(segTree.getRangeSum(1, 3)); // 10 + 5 + 7 = 22
```

---

## 📌 2장. 펜윅 트리(Fenwick Tree, Binary Indexed Tree)

### 🔹 개념
- **펜윅 트리(Fenwick Tree)** 또는 **이진 인덱스 트리(BIT)**는 세그먼트 트리와 유사하게 **구간 합 쿼리**, **단일 업데이트** 등을 O(log n)에 처리
- 내부 구조는 배열을 사용, 인덱스의 **최하위 비트(LSB)**를 활용해 구간 정보를 저장
- 세그먼트 트리보다 구현이 간단하고 메모리 사용량이 적은 장점

### 🔹 동작 원리
1. **LSB(Least Significant Bit)**: x & (-x)를 통해 x의 LSB를 쉽게 구할 수 있음
2. 펜윅 트리 배열 `tree[]`에서, 각 인덱스 i는 인덱스 범위 [i - LSB(i) + 1 .. i]의 합을 저장
3. **구간 합**을 구하거나 업데이트 할 때, 적절히 LSB를 조정하며 이동

### 🔹 기본 연산
1. **init / build**: O(n log n) 또는 O(n) 기법 (단순히 n번 update 사용 시 O(n log n))
2. **prefix sum**(1부터 특정 인덱스까지의 합): O(log n)
3. **update**(단일 원소 업데이트): O(log n)
4. **range sum**(구간 합): prefixSum(R) - prefixSum(L-1)

### 🔹 구현 예시
```javascript
class FenwickTree {
  constructor(n) {
    this.n = n;
    this.tree = new Array(n + 1).fill(0); // 인덱스 1부터 사용
  }

  // idx 위치에 val을 더하기
  update(idx, val) {
    while (idx <= this.n) {
      this.tree[idx] += val;
      idx += idx & -idx; // LSB(Least Significant Bit) 이용해 다음 인덱스로 이동
    }
  }

  // 1부터 idx까지의 prefix sum
  prefixSum(idx) {
    let result = 0;
    while (idx > 0) {
      result += this.tree[idx];
      idx -= idx & -idx;
    }
    return result;
  }

  // 구간 합 [left, right]
  rangeSum(left, right) {
    return this.prefixSum(right) - this.prefixSum(left - 1);
  }
}

// 사용 예시
const arr2 = [1, 3, 5, 7, 9, 11];
const n = arr2.length;
const fenw = new FenwickTree(n);

// 초기화: 각 원소를 update로 반영
arr2.forEach((val, i) => {
  fenw.update(i + 1, val); // 인덱스 1부터 사용
});

console.log(fenw.rangeSum(2, 4)); // arr2[1..3] = 3 + 5 + 7 = 15

// update: arr2[1] += 7
fenw.update(2, 7);
console.log(fenw.rangeSum(2, 4)); // (3+7) + 5 + 7 = 22
```

---

## 📌 3장. 세그먼트 트리 vs 펜윅 트리 비교

| 구분                  | 세그먼트 트리                | 펜윅 트리 (Fenwick)          |
|-----------------------|-------------------------------|------------------------------|
| 구현 복잡도           | 상대적으로 복잡 (트리 구조)   | 비교적 간단 (단일 배열)       |
| 메모리 사용량         | O(4n) 정도                    | O(n)                         |
| 기본 기능             | 다양한 구간 연산 가능         | 보통 구간 합, 구간 업데이트 등 |
| 확장성(구간 업데이트) | Lazy Propagation 등 별도 구현 | 차분 배열 기법으로 응용       |
| 시간 복잡도           | 빌드: O(n), 쿼리/업데이트: O(log n) | 빌드: O(n log n) (단순), 쿼리/업데이트: O(log n) |

- 세그먼트 트리는 **합, 최솟값, 최댓값, GCD** 등 다양한 연산을 일관적으로 처리 가능
- 펜윅 트리는 구현이 간단하고 메모리 사용이 작지만, **부분 업데이트**(예: 구간 업데이트)에는 별도 기법 필요

---

## 📝 정리 및 요약
- **세그먼트 트리**: 구간 쿼리와 업데이트를 O(log n)에 처리하며, 다양한 연산에 활용 가능
  - 트리 구조를 직접 구성해야 하고, 구현 복잡도와 메모리 사용이 상대적으로 높음
- **펜윅 트리(Fenwick Tree)**: O(log n)으로 구간 합 쿼리와 단일 업데이트 가능
  - 비교적 구현이 간단하고 메모리 사용 적음
- 대규모 데이터에서 구간 연산을 자주 수행할 때 매우 유용한 자료구조들

이 문서를 통해 고급 자료구조인 **세그먼트 트리**와 **펜윅 트리**의 핵심 개념과 구현 방법을 익히시고, 상황에 맞게 선택하여 효율적인 구간 연산을 처리해보시기 바랍니다.

