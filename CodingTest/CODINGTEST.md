입력 Input
==========

#### 기본 입력
```swift
var input = readLine()!
```
#### 정수형 변환
```swift
var input = Int(readLine()!)!
```
#### 공백 있는 숫자 입력 받기 return type: [Int]
```swift
// 단일 요소의 구분자
var arr = readLine()!.components(separatedBy: " ").map{Int($0)!} 
```
#### 공백 있는 숫자 입력 받기 return type: [Int]
```swift
// []을 사용하여 여러 개의 구분자 설정
var arr = readLine()!.components(separatedBy: [" "]).map{Int($0)!} 
```

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

문자열 String
==============

#### 문자열 뒤집기
```swift
var str: String = "hello world"
var reverse: String = String(str.reversed())
// 새롭게 리턴하는 것이 아니라 역순으로 접근하는 방식.
// 따라서 타입 변환 필요.
```
#### 문자(문자열 X)를 정수로 변환
```swift
var ch = "1"
(ch.wholeNumberValue)!
// 옵셔널 해제 필요.
Int(String(ch))!
// 문자를 문자열로 바꾸고 다시 정수로 바꾼다.
// 문자에서 정수로 바로 바꾸는 것을 불가 
```
#### 문자열 바꾸기
```swift
str.replacingOccurrences(of: "first", with: "second")
// 문자열에 있는 "first"을 "second"로 모두 교체 
```
#### 문자열 대소문자 바꾸기
```swift
// 문자열 str을 대문자로 변경
str.uppercased()
// 문자열 str을 소문자로 변경
str.lowercased()
```

#### 접두사, 접미사 체크하기
```swift
// 문자열 input이 str의 접두사인지 체크하고 Bool반환 
str.hasPrefix(input)
// 문자열 input이 str의 접미사인지 체크하고 Bool반환 
str.hasSuffix(input)
```

#### 문자열의 부분 가져오기
```swift
// 문자열 str의 앞에서부터 n개의 문자를 반환 
str.prefix(n)
// 문자열 str의 뒤에서부터 n개의 문자를 반환 
str.suffix(n)
```

#### 문자를 아스키코드로 변환하기
```swift
// Char 타입의 문자를 ascii 정수로 변환 
let ascii = Int(UnicodeScalar(String(ch))!.value)
```


기타 Etc
========

#### 절대값
```swift
abs(-7)
// 7 
```

#### 제곱근
```swift
sqrt(9.0)
// 3
```

#### 소수점 올림
```swift
ceil(5.13)
// 6
```