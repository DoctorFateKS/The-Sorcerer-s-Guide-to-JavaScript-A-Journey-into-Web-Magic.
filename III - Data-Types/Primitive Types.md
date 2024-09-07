# **📚 JavaScript Data Types and Structures**

JavaScript is a versatile, dynamically typed language with a variety of built-in data types and structures. Below is a detailed overview of these types and how they interact within the language.

### **🔄 Dynamic and Weak Typing**
JavaScript is both **dynamic** and **weakly typed**. Here's what that means:

- **🌀 Dynamic Typing**: Variables can be reassigned to different types of values throughout their lifecycle. For example:
  ```javascript
  let foo = 42;  // Initially a number
  foo = "bar";   // Now a string
  foo = true;    // Now a boolean
  ```

- **⚠️ Weak Typing**: JavaScript allows implicit type conversion during operations involving mismatched types, known as **[type coercion](https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion)**. For instance:
  ```javascript
  const result = 42 + "1";  // JavaScript coerces the number to a string, resulting in "421"
  ```

### **🧩 Primitive Values**
JavaScript includes several **primitive types** that represent simple data:

- **[`Null`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/null)**: Represents the intentional absence of any object value.
- **[`Undefined`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined)**: Indicates that a variable has been declared but has not yet been assigned a value.
- **[`Boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)**: Represents logical values `true` and `false`.
- **[`Number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)**: Represents both integer and floating-point numbers.
- **[`BigInt`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)**: Allows representation of integers larger than those safely representable by `Number`.
- **[`String`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)**: Represents sequences of characters in UTF-16 encoding.
- **[`Symbol`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)**: A unique and immutable value, often used as object property keys.

**Note**: Each of these primitive types, except `Null` and `Undefined`, has a corresponding **[object wrapper](https://javascriptrefined.io/the-wrapper-object-400311b29151)** (e.g., `Boolean`, `Number`, `BigInt`, `String`, `Symbol`) that provides additional methods and properties.

### **📦 Objects**
**Objects** are complex data structures used to store collections of key-value pairs. Objects can be created using the object literal syntax:

```javascript
let obj = {
  key1: "value1",
  key2: "value2"
};
```

Objects consist of properties, which can be either **[data properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)** (holding values) or **accessor properties** (with getter and setter functions). 

**Example**: Accessor properties allow for dynamic computation of property values:

```javascript
let person = {
  firstName: "John",
  lastName: "Doe",
  get fullName() {
    return `${this.firstName} ${this.lastName}`;
  }
};
```

### **🔢 Numeric Types**
JavaScript has two primary **numeric types**:

- **[`Number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)**: A double-precision 64-bit floating-point value.
- **[`BigInt`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/BigInt)**: Handles integers larger than `Number.MAX_SAFE_INTEGER`.

**Example**:
```javascript
const bigInt = BigInt(9007199254740991);
console.log(bigInt + 1n);  // 9007199254740992n
```

### **✒️ Strings**
**[Strings](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** in JavaScript represent text and are encoded as sequences of 16-bit unsigned integers in UTF-16. 

- *Strings are immutable*, meaning they cannot be altered once created. Methods like `concat()`, `substring()`, and the `+` operator create new strings rather than modifying the original string.

**Note**: Using strings to represent non-textual data is generally discouraged as it can lead to maintainability issues.

### **🔑 Symbols**
**[Symbols](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol)** are a unique primitive type used primarily as object property keys. They are *guaranteed to be unique*, helping avoid naming conflicts.

**Example**:
```javascript
const sym = Symbol('description');
let obj = {
  [sym]: "value"
};
console.log(obj[sym]);  // "value"
```

### **📚 Collections**
JavaScript provides several types of **collections** for managing sets of data:

- **[Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)**: Ordered lists of elements.
- **[Typed Arrays](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Typed_arrays)**: Arrays providing a view over binary data.
- **[Maps](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)**: Collections of key-value pairs, where keys can be of any type.
- **[Sets](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)**: Collections of unique values.

### **🔄 Type Coercion**
JavaScript's weak typing system allows for various forms of **[type coercion](https://developer.mozilla.org/en-US/docs/Glossary/Type_coercion)**, where values are implicitly converted between types. Coercion can occur in different contexts:

- **Primitive Coercion**: Converts objects to primitives based on context.
- **Numeric Coercion**: Handles conversion to `Number` or `BigInt`.
- **String Coercion**: Converts values to strings, often used in concatenation.

### **🗂️ Structured Data**
For structured data, **[JSON](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/JSON)** (JavaScript Object Notation) is the preferred format in JavaScript.

### **🔧 Other Standard Objects**
JavaScript includes a comprehensive standard library with various **built-in objects** like `Date`, `RegExp`, and `Error`.
