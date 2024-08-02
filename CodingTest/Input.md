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
