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