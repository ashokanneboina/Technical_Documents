



## 1. What is Encoding?

Computers **do not understand characters or text** directly.

Humans see:

```
Hello 
```

But computers only store:

```
binary (0s and 1s)
```

**Encoding** is the process of converting human-readable text into numbers and bytes so computers can store and transmit it.

```
Text → Numbers → Bytes → Binary
```

---

## 2. ASCII (American Standard Code for Information Interchange)

ASCII was one of the first character encoding systems.

### Key Features

* Uses numbers from **0 to 127**
* Each character uses **1 byte**
* Supports only:

  * English letters
  * digits
  * punctuation
  * control characters

### Examples

| Character | ASCII Number |
| --------- | ------------ |
| A         | 65           |
| B         | 66           |
| a         | 97           |
| space     | 32           |

### Python Example

```python
print(ord("A"))   # character → number
print(chr(65))    # number → character
```

ASCII worked well for English but failed for other languages and emojis.

---

## 3. Unicode — Universal Character System

To support all languages, Unicode was created.

Unicode assigns a **unique number (code point)** to every character.

### Unicode Format

```
U+XXXX
```

* `U` = Unicode
* `+` = separator
* `XXXX` = hexadecimal number

### Examples

| Character | Unicode |
| --------- | ------- |
| A         | U+0041  |
| ₹         | U+20B9  |
| 😀        | U+1F600 |
| अ         | U+0905  |

Unicode is **not storage** — it only defines character IDs.

### Example

```python
print(f"U+{ord('A'):04X}")
```

---

## 4. Why Unicode Needs UTF Encodings

Unicode gives numbers, but computers store **bytes**.

So we need rules to convert Unicode numbers into bytes.

These rules are called **UTF (Unicode Transformation Format)**.

---

## 5. UTF-8 Encoding

UTF-8 is the most widely used encoding today (used by websites, APIs, databases).

### Properties

* Variable length encoding
* Uses 1 to 4 bytes per character

| Character Type   | Bytes Used |
| ---------------- | ---------- |
| English letters  | 1 byte     |
| European symbols | 2 bytes    |
| Asian scripts    | 3 bytes    |
| Emoji            | 4 bytes    |

### Example

```python
text = "A 😀"
print(text.encode("utf-8"))
```

Output (example):

```
b'A \xf0\x9f\x98\x80'
```

UTF-8 became popular because:

* Compatible with ASCII
* Saves memory
* Efficient for English-heavy text

---

## 6. UTF-16 Encoding

UTF-16 stores characters using **16-bit units (2 bytes)**.

### Properties

* Most characters → 2 bytes
* Large characters (like emojis) → 4 bytes
* Uses something called **surrogate pairs** for large Unicode values.

### Example

```python
print("A ".encode("utf-16"))
```

UTF-16 is used internally by some systems and programming environments.

---

## 7. UTF-32 Encoding

UTF-32 uses a fixed size:

```
4 bytes per character
```

### Advantages

* Simple indexing
* Every character same size

### Disadvantages

* Uses much more memory

### Example

```python
print("A ".encode("utf-32"))
```

---

## 8. Hex Representation

Bytes are often displayed in **hexadecimal** because binary is long.

Example:

```python
data = "A".encode("utf-8")
print(data.hex())
```

Output:

```
41
```

Hex is just a readable form of binary.

---

## 9. Binary Representation

Binary shows the actual stored bits.

```python
data = "A".encode("utf-8")

for byte in data:
    print(format(byte, "08b"))
```

Output:

```
01000001
```

This is how data physically exists in memory.

---

## 10. Base64 Encoding

Base64 is **NOT a character encoding** like UTF-8.

It converts binary data into safe text characters.

Some systems allow only text transmission:

* Email systems
* JSON
* HTTP headers
* APIs

Binary data may break these systems, so Base64 converts bytes into ASCII-safe text.

### Example

```python
import base64

data = bytes([0b00000011])

encoded = base64.b64encode(data)
print(encoded)

decoded = base64.b64decode(encoded)
print(decoded)
```
---

##  Summary

- **ASCII** – Early character encoding for English text. Uses numbers (0–127) to represent characters, typically stored in 1 byte.

- **Unicode** – A universal system that assigns a unique code point (`U+XXXX`) to every character across all languages and symbols.

- **UTF-8** – A Unicode encoding that stores characters using 1–4 bytes. Efficient and widely used on the internet.

- **UTF-16** – A Unicode encoding that usually uses 2 bytes per character, but may use 4 bytes for larger characters like emojis.

- **UTF-32** – A Unicode encoding where every character uses exactly 4 bytes, making processing simple but memory usage higher.

- **Base64** – A binary-to-text encoding that converts data into safe ASCII text for transmission through text-based systems.
