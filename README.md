# data-structure-study
# 배열이란?

배열(array)은 여러 개의 값을 순차적으로 나열한 **************************자료구조**************************다. 배열은 사용 빈도가 매우 높은 가장 기본적인 자료구조다. 

배열이 가지고 있는 값을 ****************요소****************라고 부른다. 배열의 요소는 자신의 위치를 나타내는 0 이상의 정수인 ************************인덱스************************를 갖는다. 인덱스는 배열의 요소에 접근할 때 사용한다. 대부분의 프로그래밍 언어에서는 인덱스는 0부터 시작한다.

*예제*

```jsx
const arr = ['apple', 'banana', 'orange'];
```

예제의 배열 arr은 3개의 요소로 구성되어 있다. 순차적으로 첫 번째 요소인 `‘apple’`의 인덱스는 0, `‘banana’`는 1, `‘orange’`는 2라는 각각의 인덱스를 갖는다.

요소에 접근할 때는 대괄호 표기법을 사용한다. 대괄호 내에는 접근하고 싶은 요소의 인덱스를 지정한다.

*예제*

```jsx
arr[0] // 'apple'
arr[1] // 'banana'
arr[2] // 'orange'
```

배열은 요소의 개수, 즉 배열의 길이를 나타내는 **length 프로퍼티**를 갖는다.

```jsx
arr.length // 3
```

배열은 인덱스와 length 프로퍼티를 갖기 때문에 for 문을 통해 순차적으로 요소에 접근할 수 있다.

```jsx
// 배열의 순회
for(let i = 0; i < arr.length; i++){
	console.log(arr[i]); // 'apple' 'banana' 'orange'
}
```

<aside>
🚨 주의
자바스크립트에 배열이라는 타입은 존재하지 않는다. 자바스크립트에서 배열은 객체 타입이다.

</aside>

---

자료구조에서 말하는 배열은 동일한 크기의 메모리 공간이 빈틈없이 연속적으로 나열된 자료구조를 말한다.

즉, 배열의 요소는 하나의 데이터 타입으로 통일되어 있으며 서로 연속적으로 인접해 있다. 이러한 배열을 ************************밀집 배열************************이라 한다.

<img width="436" alt="Untitled" src="https://github.com/dbs271/data-structure-study/assets/101887549/517dfc5d-3f89-4fa0-8322-f6b76d4b6d78">


이처럼 배열은 인덱스를 통해 효율적으로 요소에 접근할 수 있다는 장점이 있지만 정렬되지 않은 배열에서 특정한 요소를 검색하는 경우 배열의 모든 요소를 처음부터 특정 요소를 발견할 때까지 차례대로 검색해야 한다.

또한 배열에 요소를 삽입하거나 삭제하는 경우 배열의 요소를 연속적으로 유지하기 위해 요소를 이동시켜야 하는 단점도 있다.

---

## 배열의 특징 정리

1. ****요소(Element):**** 배열은 여러 개의 데이터 요소로 구성된다. 이 요소들은 순서대로 나열되며, 각 요소는 고유한 위치 또는 인덱스를 가진다.
2. ********************************인덱스(Index):******************************** 배열의 각 요소는 0부터 시작하는 정수로 된 인덱스를 가지며, 인덱스를 사용하여 요소에 접근할 수 있다. ex. 첫 번째 요소의 인덱스는 0, 두 번째 요소의 인덱스는 1이다.
3. ****************************고정된 크기 또는 가변 크기:**************************** 배열은 고정된 크기일 수도 있고, 가변 크기일 수도 있다. 고정된 크기 배열은 생성 시에 크기가 정해지며 크기를 변경할 수 없다. 가변 크기 배열은 동적으로 조절할 수 있다.
4. ********************************************************연속적인 메모리 공간:******************************************************** 대부분의 배열은 연속적인 메모리 공간에 요소를 저장한다. 이로 인해 인덱스를 사용하여 빠르게 요소에 접근할 수 있다.
5. ****************************************************동일한 데이터 유형:**************************************************** 배열은 동일한 데이터 유형의 요소만 저장할 수 있다. 예를 들어, 정수 배열은 정수 값만 저장할 수 있다.
6. **************************길이(Length):************************** 배열은 길이(Length)라고 불리는 프로퍼티(속성)을 가지며, 이 프로퍼티는 배열에 포함된 요소의 개수를 나타낸다. 배열의 길이는 배열에 있는 요소 수를 기준으로 동적으로 변경될 수 있다.
    1. 이때 헷갈릴 수 있는 부분이 배열의 인덱스와 길이이다. 인덱스는 0부터 시작하는 반면 길이는 배열의 요소 개수를 갖기 때문에 이 두개를 헷갈리지 않게 조심해야 한다.
        1. 예시 arr = [1, 2, 3] 이 있다고 하면 인덱스는 순서대로 0, 1, 2의 순서를 메긴다. 즉, arr 요소의 3은 인덱스로 2다. 하지만 길이는 요소의 개수를 갖기 때문에 arr의 길이는 3이다.
7. ******************************다양한 연산:****************************** 배열은 데이터를 저장하고 검색하는 데 사용할 수 있는 다양한 연산을 지원한다. 예를 들어, 요소 추가, 삭제, 정렬, 반복 순회 등의 작업을 수행할 수 있다.
8. ********************************다차원 배열:******************************** 배열은 다차원 형태로도 사용될 수 있다. 1차원 배열은 단순한 목록이며, 2차원 배열은 행과 열로 구성된 표 형태이다. 다차원 배열은 중첩된 배열의 형태로 표현된다.

---

## 배열 연산

배열은 다양한 기본 연산을 할 수 있다.

******************요소 접근******************

배열 내의 특정 요소에 접근하기 위해 인덱스를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];

arr[0] // 1
```

****요소 추가****

배열 끝에 요소를 추가하는 연산으로 주로 `push()` 함수를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];

arr.push(6); // [1, 2, 3, 4, 5, 6]
```

****************요소 삭제****************

배열 내의 요소를 삭제하기 위해 `pop()` 함수(마지막 요소 제거), `shift()` 함수(첫 번째 요소 제거) 또는 `splice(start, deleteCount, item)` 함수(지정한 위치의 요소 제거)와 같은 함수를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];

arr.pop(); // [1, 2, 3, 4]
arr.shift(); // [2, 3, 4, 5]

// splice 함수는 첫 번째 매개변수로 시작할 인덱스를 지정합니다. 
// 두 번째 매개변수로는 제거할 요소의 개수를 지정합니다.
// 마지막으로는 배열에 추가할 요소입니다. 아무 요소도 지정하지 않으면 splice()는 요소를 제거하기만 합니다.

// 0번 인덱스에서 2개 요소를 제거 
arr.splice(0,2); // [3, 4, 5] 인덱스 0부터 2개의 요소를 제거 0, 1

// 0번 인덱스에서 2개 요소를 제거하고 6, 7, 8을 추가
arr.splice(0, 2, 6,7,8); // [6, 7, 8, 3, 4, 5]
```

******요소 삽입******

배열 내에 요소를 특정 위치에 삽입하기 위해 `splice()` 함수나 `unshift()` 함수를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];

arr.splice(0, 0, 6, 7); // [6, 7, 1, 2, 3, 4, 5]
arr.unshifr(6,7); // [6, 7, 1, 2, 3, 4, 5]
```

**************************반복 순회**************************

배열의 모든 요소를 반복하여 처리하기 위해 반복문(`for`, `forEach`)을 사용한다.

```jsx
// for
let arr = [1, 2, 3, 4, 5];

for(let i = 0; i < arr.length; i++){
	console.log(arr[i]) // 1, 2, 3, 4, 5
}

// forEach
let arr = [1, 2, 3, 4, 5];

arr.forEach(e => console.log(e)) // 1, 2, 3, 4, 5
```

************************************배열 길이 확인************************************

배열 내의 요소 수를 확인하기 위해 `length` 프로퍼티를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];
console.log(arr.length); // 5
```

****배열 복사****

배열을 복사하여 새로운 배열을 만들기 위해 `slcie()` 함수나 `concat()` 함수를 사용한다.

```jsx
// slice() 메서드는 어떤 배열의 begin 부터 end 까지(end 미포함)에 
// 대한 얕은 복사본을 새로운 배열 객체로 반환합니다. 원본 배열은 바뀌지 않습니다.
let arr = [1, 2, 3, 4, 5];

arr.slice(0, 2); // [1, 2]

// concat() 메서드는 두 개 이상의 배열을 병합하는 데 사용됩니다. 
// 이 메서드는 기존 배열을 변경하지 않고, 새 배열을 반환합니다.
let arr = [1, 2, 3, 4, 5];
let arr2 = ['a', 'b', 'c', 'd', 'e'];

console.log(arr.concat(arr2)); // [1, 2, 3, 4, 5, 'a', 'b', 'c', 'd', 'e']
```

**********요소 검색**********

배열에서 특정 값 또는 조건을 만족하는 요소를 검색하기 위해 `indexOf()` 함수(값의 인덱스 검색), `find()` 함수(조건을 만족하는 첫 번째 요소 검색), `filter()` 함수(조건을 만족하는 모든 요소 검색)와 같은 함수를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];

// indexOf()
arr.indexOf(1); // 0
// 배열에 존재하지 않는 값을 입력하면 -1을 반환합니다.
arr.indexOf(6); // -1

// find()
// find() 메서드는 주어진 판별 함수를 만족하는 첫 번째 요소의 값을 반환합니다.
arr.find(e => e > 3); // 4

// filter()
// filter() 메서드는 주어진 배열의 일부에 대한 얕은 복사본을 생성하고, 
// 주어진 배열에서 제공된 함수에 의해 구현된 테스트를 통과한 요소로만 필터링 합니다.
const newArr = arr.filter((e) => e > 2); // [3, 4, 5]
```

********정렬********

배열을 정렬하기 위해 `sort()` 함수나 사용자 정의 비교 함수를 사용한다.

```jsx
let arr = ['a', 'c', 'd', 'f', 'b', 'e']

arr.sort(); // ['a', 'b', 'c', 'd', 'e', 'f']

// 기본 정렬 순서가 문자열의 유니코드 포인트를 따르기 때문에 숫자를 정렬할 때는 아래와 같은 방식을 따릅니다.
let arr = [2, 5, 3, 4, 2];

// 오름차순
arr.sort((a,b) => a - b); // [1, 2, 3, 4, 5]
// 내림차순
arr.sort((a,b) => b - a); // [5, 4, 3, 2, 1]
```

********************배열 연결********************

배열을 합치거나 연결하기 위해 `concat()` 함수를 사용한다.

```jsx
let arr = [1, 2, 3, 4, 5];
let arr1 = ['a', 'b', 'c', 'd', 'e', 'f'];

arr.concat(arr1); // [1, 2, 3, 4, 5, 'a', 'b', 'c', 'd', 'e', 'f'];

```

************************배열 반환************************

배열의 요소를 다른 형태로 변환하기 위해 `map()` 함수나 `reduce()` 함수를 사용한다.

```jsx
// reduce는 배열의 각 요소에 대해 주어진 리듀서(reducer) 함수를 실행하고, 하나의 결과값을 반환합니다.
// reduce()에는 누산기가 포함되어 있기 때문에, 배열의 각 요소에 대해 함수를 실행하고 
// 누적된 값을 출력할 때 용이하다. 가장 기본적인 예제로는 모든 배열의 합을 구하는 경우가 있다.
let arr = [1, 2, 3, 4, 5]
arr.reduce((acc, curr) => acc + curr) // 15

// map 메서드는 배열 내의 모든 요소 각각에 대하여 주어진 함수를 호출한 결과를 모아 새로운 배열을 반환합니다.
let arr = [1, 2, 3, 4, 5]
arr.map(e => e * 2) // [2, 4, 6, 8, 10]
```

****배열 초기화****

배열의 요소를 초기값으로 설정하기 위해 `fill()` 함수나 `Array()` 생성자를 사용합니다.
```jsx
// fill() 메서드는 배열의 인덱스 범위 내에 있는 모든 요소를 정적 값으로 변경합니다. 
// 그리고 수정된 배열을 반환합니다.
// fill(value, start, end)
let arr = [1, 2, 3, 4, 5]
arr.fill(10, 0, 2) // [10, 10, 3, 4, 5]

arr.fill(10, 2) // [1, 2, 10, 10, 10]

arr.fill(10) // [10, 10, 10, 10, 10]


let arr = new Array(1, 2)
arr[1] // 2

let arr = new Array(3)
arr[0] // undefined
arr.length // 3
```
---
## 동적 배열(Dynamic Array)

- 동적 배열은 크기가 가변적인 배열입니다. 배열을 생성할 때 크기를 지정하지 않고 요소를 추가할 때마다 배열의 크기가 자동으로 조정됩니다.
- 동적 배열은 대게 동적 메모리 할당을 통해 크기를 조절합니다. 요소를 추가하거나 삭제할 때마다 필요한 만큼의 메모리를 동적으로 할당하거나 해제합니다.
- 동적 배열의  장점은 요소의 추가와 삭제가 쉽고 효율적이며, 배열 크기에 대한 걱정 없이 사용할 수 있다는 점입니다.

********************************************************************************자바스크립트에서 동적 배열 예시********************************************************************************

```jsx
let arr = [];

// 요소 추가
arr.push(1);
arr.push(2);
arr.push(3);

console.log(arr); // [1, 2, 3]

// 요소 제거
arr.pop(); // 마지막 요소 제거
console.log(arr); // [1, 2]
```

배열의 크기가 동적으로 조절되므로 요소를 추가하거나 제거할 때 배열의 크기가 자동으로 조절됩니다.

---

## 고정 배열(static Array)

- 고정 배열은 생성할 때 크기가 고정되어 있으며, 크기를 동적으로 변경할 수 없습니다. 배열을 생성할 때 지정된 크기만큼의 요소만 저장할 수 있습니다.
- 고정 배열은 메모리를 미리 할당하므로 크기 조절을 위한 추가적인 메모리 할당이 필요하지 않습니다. 이로 인해 메모리 관리가 더 효율적입니다.
- 고정 배열의 단점은 크기를 변경할 수 없기 때문에 크기를 초과하는 요소를 추가하려면 새로운 배열을 만들고 데이터를 복사해야 합니다. 이러한 연산은 비용이 더 들 수 있습니다.

********************************************************************자바스크립트에서 고정 배열 예시********************************************************************

자바스크립트에서는 배열을 동적으로 다루는 것이 일반적이지만, 배열 크기를 고정하려면 새로운 배열을 생성하거나 배열 요소를 직접 조작하여 구현할 수 있습니다.

```jsx
let arr = new Array(3);

// 요소 할당
arr[0] = 1;
arr[1] = 2;
arr[2] = 3;

console.log(arr); // [1, 2, 3]

// 요소 제거
arr[1] = undefined; // 요소 제거
console.log(arr); // [1, undefined, 3]
```

위 예시에서 배열 크기는 3으로 고정되어 있으며, 크기를 변경할 수 없습니다. 요소를 제거하기 위해 해당 요소를 `undefined`로 설정할 수 있지만 배열 크기는 그대로 유지됩니다.
