배열 Array
==========

#### 범위 연산자를 사용한 배열 생성
```swift
// Array를 명시하여 타입을 배열로
let array = Array(1...100)
// 1부터 100까지 1씩 더한 결과를 Array로(마지막 100 포함)
let array = Array(stride(from: 1, through: 100, by: 1))
// 1부터 100까지 1씩 더한 결과를 Array로(마지막 100 미포함)
let array = Array(stride(from: 1,to: 100, by: 1))
```

#### 정해진 수만큼 반복한 배열 생성 
```swift
Array(repeating: num, count: cnt)
// 원소 num을 cnt만큼 반복한 컬렉션 반환.
```

#### 범위 연산자를 사용한 접근
```swift
array[0...10]
// 0부터 10까지 배열 리턴
```

#### 배열에 원소 삽입 
```swift
arr.append(contentsOf: arr2)
// arr배열에 arr2배열을 추가
```

#### 인덱스와 값을 가지고있는 순서쌍 배열
```swift
arr.enumerated()
// arr배열을 (offset, element) tuple 타입의 배열로 반환
```

#### 처음과 마지막 원소 제거(반드시 빈 배열 여부 체크!)
```swift
// 배열의 첫 번째 원소 제거 후 해당 원소 값 리턴
arr.removeFirst()
// 배열의 마지막 원소 제거 후 해당 원소 값 리턴
arr.removeLast()
```

#### 배열의 최소, 최대 
```swift
// arr배열 최솟값
arr.min()
// arr배열 최댓값
arr.max()
```

#### 배열 요소 교환 
```swift
// arr의 first과 second의 인덱스에 있는 원소들을 교환
arr.swapAt(first, second)
```

#### 배열의 값을 조회하고 해당하는 인덱스를 반환
```swift
// 배열의 시작부터 조회해서 값이 2인 인덱스를 리턴
arr.firstIndex(of: 2)
// 배열의 끝부터 조회해서 값이 2인 인덱스를 리턴
arr.lastIndex(of: 2)
```
