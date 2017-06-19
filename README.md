# Swift 예제코드 바로잡기
[Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines/) 및 [The Swift Programming Language - Language Guide](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/TheBasics.html)에 의거하여 교재 2장~6장의 예제코드를 수정해봅니다.

아래는 예제이므로, 더 좋은 정리방법이 있다면 다른 방법으로 표현하는 것도 좋습니다.

## 2장
> 32 페이지

### 수정 전
```swift
var str = " Hello, playground"
```

### 수정 후
```swift
var greeting = " Hello, playground"
```

### 근거
* Swift API Design Guidelines
	* Naming
		* Promote Clear Usage

> 44 페이지

### 수정 전
```swift
enum PieType {
    case Apple
    case Cherry
    case Pecan
}
```

### 수정 후
```swift
enum PieType {
    case apple
    case cherry
    case pecan
}
```

### 근거
* Enum의 case 명명법 변경
	* UpperCamelCase -> lowerCamelCase
	* The Swift Programming Language(Language Guide)
		* [Enumerations](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html)
			* Enumeration Syntax

## 3장

## 4장
> 88 페이지

### 수정 전
```swift
let numberFormatter: NSNumberFormatter = {
    let nf = NSNumberFormatter()
    nf.numberStyle = .DecimalStyle
    nf.minimumFractionDigits = 0
    nf.maximumFractionDigits = 1
    return nf
}()

```
### 수정 후
```swift
let numberFormatter: NumberFormatter = {
    let numberFormatter = NumberFormatter()
    numberFormatter.numberStyle = .decimal
    numberFormatter.minimumFractionDigits = 0
    numberFormatter.maximumFractionDigits = 1
    return numberFormatter
}()
```

### 근거
* Swift API Design Guidelines
	* Naming
		* Promote Clear Usage
* Foundation의 NSNumberFormatter의 Swift 클래스 이름 변경
	* NSNumberFormatter -> [NumberFormatter](https://developer.apple.com/documentation/foundation/numberformatter)
* Enum의 case 명명법 변경
	* UpperCamelCase -> lowerCamelCase
	* The Swift Programming Language(Language Guide)
		* [Enumerations](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Enumerations.html)
			* Enumeration Syntax



## 5장

## 6장
