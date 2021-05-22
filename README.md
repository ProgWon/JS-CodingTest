# JS-CodingTest

## 필요성

- 프론트 엔드 개발자를 준비하는 사람이라면 어떤 언어를 사용해서 코딩 테스트를 진행해야 하는지 고민이 많으실겁니다. 대부분의 코딩테스트는 C++ 이나 Java, 그리고 간결하고 쉬운 Python 을 많이 사용합니다. 물론 이런 언어들로도 공채 코딩테스트를 보는데에는 문제가 없지만, 프론트엔드 개발자는 JS 만을 사용하는 코딩테스트 환경에 놓일 수도 있습니다. (ex) 배달의 민족 우아한 테크 코스) 다른 언어와 달리 많은 자료들이 존재하지 않아 문제를 풀면서 얻은 지식들을 게시하고 공유하고자 합니다!

## 문자열

### toLowerCase(), toUpperCase()

- 문자의 대문자, 소문자 여부를 구분 할 수 있는 함수입니다. **대문자라면,** 혹은 **소문자라면** 이라는 조건식에 주로 많이 사용됩니다.

- 주로 for 문과 같이 사용됩니다. 사용 방법은 문자열에 대해서 한 개의 문자를 뽑은 후 str.toLowerCase() 혹은 str.toUpperCase() 로 대문자나 소문자로 치환하고 if 문을 통해 비교하는데 사용합니다.

```javascript
// 만약 소문자라면, 답을 하나 더해줍니다.
if (x == x.toLowerCase()) answer++;
// 대문자라면, 답을 하나 더해줍니다.
if (x == x.toUpperCase()) answer++;
```

- 대문자이거나 소문자라면 True 를 return 하는 함수가 아닙니다. 소문자라면 대문자, 대문자라면 소문자로 만들어 주는 함수이니 isUpper, isLower 로 잘못 아시면 안됩니다.

```javascript
str = "abc";
console.log(str[0].toUpperCase()); // A 출력!
```

### charCodeAt()

- 문자 하나를 아스키 코드로 바꿔주는 함수입니다. 마찬가지로 대문자나 소문자 여부를 판단하기 위해서 사용되는 기법중 하나입니다. 아래의 코드처럼 사용합니다.

```javascript
// num 에 문자 chr 의 아스키 코드를 대입합니다.
let num = chr.charCodeAt();
// 아스키 코드에서 65는 'A', 90은 'Z' 입니다. 그렇다면 아래 코드는 대문자라면, 이 되겠네요.
if (num >= 65 && num <= 90) answer++;
```

- 대소문자 뿐만 아니라 원하는 아스키 코드 범위의 내용을 검색하는데에도 사용 가능합니다. 이 부분은 아스키 코드 표를 보면서 공부해시길 바랍니다.

## 배열

### 배열에 값 추가하기

#### 1. Array.push()

Array.push() 는 배열의 끝에 원하는 값을 추가하고 싶을 때 사용합니다.

```javascript
var arr[1, 2, 3];

arr.push(4)
console.log(arr) // [1, 2, 3, 4]
```

#### 2. Array.unshift()

Array.unshift() 는 push() 와 반대로 맨 앞에 원하는 값을 추가하고 싶을 때 사용합니다.

```javascript
var arr[1, 2, 3];

arr.unshift(4)
console.log(arr) // [4, 1, 2, 3]
```

#### 3. Array.splice()

Array.splice() 는 원하는 위치에 1개 이상의 원소를 추가할 수 있습니다. arr.splice('인덱스 위치', 0, ["값1", "값2"]) 처럼 사용합니다.

```javascript
var arr[1, 2, 3];

arr.splice(0, 0, 4)
console.log(arr) // [4, 1, 2, 3]
arr.splice(0, 0, 1, 2, 3, 4)
console.log(arr) // [1, 2, 3, 4, 4, 1, 2, 3]
```
