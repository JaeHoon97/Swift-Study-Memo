문자열 String
===========

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
// 문자열에 있는 "first"을 "second"로 모두 교체
// 반환타입은 String
str.replacingOccurrences(of: "first", with: "second")
```

#### 정해진 범위의 문자열 바꾸기
```swift
// 시작 인덱스 설정 
var startIndex = str.index(str.startIndex, offsetBy: 0)
// 마지막 인덱스 설정
var endIndex = str.index(str.startIndex, offsetBy: 7)
// 문자열 str의 startIndex..<endIndex 범위에 있는 문자열을 str2로 교체
str.replaceSubrange(startIndex..<endIndex, with: str2)
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

#### 문자열 정렬하기
```swift
// 주의! 반환 타입이 String이 아니라 String.Element
// String.Element은 Character이랑 같음

// 문자열 str을 오름차순 정렬. 원본 변경 X
str.sorted()
// 문자열 str을 오름차순 정렬. 원본 변경 O
str.sort()
```

#### 문자를 아스키코드로 변환하기
```swift
// Char 타입의 문자를 ascii 정수로 변환 
let ascii = Int(UnicodeScalar(String(ch))!.value)
```