https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics/

## Overview

Swift is similar to C or Obj-C. It has type safety.

Swift has its own primitives:
- `Int`, `Double`, `Float`
- `Bool`
- `String`

And collections:
- `Array`, `Set`, `Dictionary`
- `Tuples` => multiple returns

Swift has constants by default (yay) and a couple of quirks:
* optionals (explicit non-existent value)

## Syntax

Editing a const is a compile-time error.
```
let PI = 3.14 // constants
var radius = 10 // variables

var x = 0.0, y = 0.0, z = 0.0 // multi-declaration

let name: String // type declaration

var r, g, b: Double // multiple type annotation

var `class` // naming things as built-in (don't use)

print("hello, world!") // print(_:separator:terminator), set terminator to "" for no \n
let name = "Jeff"
print("hello, \(name)") // interpolation

/* multiline comments
 /* nested comments (woah) */
 */
 
let teacher = "Me"; print(teacher) // semicolons

// Types in Swift have capitalized names
// Ints have signed-ness and width
// Int and UInt (no width) has default width equal to platform; keep for interop

// Double: 64-bit (15 decimal digits)
// Float: 32-bit (6 decimal digits)

// numeric special forms:
// 0b for binary
// 0o (o) for hex
// 0x for hex
// decimal forms can be exponential (ex. 1.25e2)
// for hex, use p. (ex. 0xfp2 means 15 * 2^2)

// numeric literals can have underscores (:

// you can get int maxes via Int8.max

// casting to wider widths must be explicit. cast with UInt8(value)

typealias AudioSampleRate = UInt16 // alias
if booleanValue { // must be Boolean, not int
} else {
}

// Tuples (use Structures and Classes for things that are more complex)
let http404Error = (404, "Not Found")
let (code, message) = http404Error // decomposition
let (_, message) = http404Error // partial decomposition
print("\(http404Error.0)") // accessing
let http200 = (code: 200, desc: "Success")
print("we got \(http200.code)")

// Structs (can have constructors)
struct Resolution { 
	var width = 0
	var height = 0
}

// Classes (structs + inheritance, typecasting to change class at runtime, deinitializers to free assigned resources, multiple refs)
class VideoMode {
	var resolution = Resolution()
	var interlaced = false
	var frameRate = 0.0
	var name: String?
	var kelvin: Double?
	init(_ unnamedParam: Double, fromKelvin kelvin: Double, frameRate: Double) {
		// initializer
		// use this iff a field doesn't change
		// use self. to specify own fields
	}
}

// structs are value types - copied when it's assigned
enum CompassPoint {
	case north, south, east, west
	mutating func turnNorth() {
		self = .north
	}
}

// === checks both exactly same instance (classes)
// !===
// classes can define their own == and !=

// Optionals
// you can use _optionals_ where the value is absent, ex.
let converted = Int("42") // inferred Int?
if converted == nil {
}

// nil must be used with optionals, not regular values
// NOT a pointer; works for any type

// check with
if let converted = Int("42") {
}
if let converted { // where "converted" is the name of the optional
}

// initialize multiple, separated with commas, with boolean conditions

// use an ! to assert that an optional exists

func multiply() throws {} // throws, forcing catch
do {

} catch SandwichError.outOfDishes {

}

// assertions and preconditions let your app fail when things go wrong, and make debugging easier
assert(age >= 0, "Age must be positive")

func canThrow() throws -> String

// functional programming and no multiple inheritance, yay (:
```