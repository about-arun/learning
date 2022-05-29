---
## JAVASCRIPT
---

### Basics

---

**Primitive Types**

| Primitive Types |
| --------------- |
| Number          |
| String          |
| Boolean         |
| Null            |
| Undefined       |
| Symbol          |
| BigInt          |
|                 |

---

**Notable Operators**

9 % 2 = 1

> modulo operator

2 \*\* 6 = 16

> 2 to the power of 6

**shorthand notation for** **_`score = score + 10;`_**

> score += 10;

> score -= 50;

> score \*= 2;

> score /= 2;

> score \*= bonusMult;

```js
score = score * bonusMult;
```

**Unary operator**

score++;

score--:

---

**NaN**

> NaN is a numberic value that represents something that is...not a number.

> 0/0 is not a number

> 1+ NaN

---

**Variable**

> _variables in javaScript are camelCased and not snake_cased_

> _Variables in javascript can change type unlike many other languages. Typescript enforces stricter rules over this_

```js
let someName = value;
```

---

**Constant**

> cannot change the value after setting it up.

```js
const pi = 3.14159;
```

> even if one identifier is declared as a constand and the other as a variable. they cant have the same name.

---

**string**

> Use single or double quotes
>
> if you need to have quotes inside a string, use the other quote. These are valid strings:

```js
"he said 'lol' ";
'he said "lol" ';
```

> `firstName + lastName` will concatinate the two strings.
>
> Each character in a string has a corresponding index (a positional number)

| C   | H   | I   | C   | K   | E   | N   |
| --- | --- | --- | --- | --- | --- | --- |
| 0   | 1   | 2   | 3   | 4   | 5   | 6   |

**.length** - every string has this property

> -       `"hello ".length` returns 7
>
> - whitespaces inside string are also counted as its length.

> - Accessing the characters of a string using index:
>
>   -     `mySong[5]`

> - length of a string is always one greater than the last index.

> - Strings are immutable in Javascript meaning individual characters cannot be altered using index as in some other languages.

---
