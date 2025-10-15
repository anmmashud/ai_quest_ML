# 🧵 **Python String Methods — Full Cheat Sheet**

---

## 🔠 Case Conversion Methods

| Method             | Description                                                                         | Example                           | Output                    |
| ------------------ | ----------------------------------------------------------------------------------- | --------------------------------- | ------------------------- |
| **`upper()`**      | Converts all letters to uppercase.                                                  | `'python'.upper()`                | `'PYTHON'`                |
| **`lower()`**      | Converts all letters to lowercase.                                                  | `'PyTHon'.lower()`                | `'python'`                |
| **`capitalize()`** | Makes the first character uppercase and the rest lowercase.                         | `'hello world'.capitalize()`      | `'Hello world'`           |
| **`title()`**      | Capitalizes the first letter of every word.                                         | `'python string methods'.title()` | `'Python String Methods'` |
| **`swapcase()`**   | Swaps uppercase to lowercase and vice versa.                                        | `'PyTHon'.swapcase()`             | `'pYthON'`                |
| **`casefold()`**   | Converts to lowercase, more aggressive than `lower()` (handles foreign characters). | `'ß'.casefold()`                  | `'ss'`                    |

---

## 🧮 String Testing Methods (Return `True` / `False`)

| Method               | Checks if string...                                               | Example                   | Output  |
| -------------------- | ----------------------------------------------------------------- | ------------------------- | ------- |
| **`isalnum()`**      | Contains only letters and numbers (no spaces or symbols).         | `'abc123'.isalnum()`      | `True`  |
| **`isalpha()`**      | Contains only letters (A–Z, a–z).                                 | `'Python'.isalpha()`      | `True`  |
| **`isascii()`**      | Contains only ASCII characters.                                   | `'abc'.isascii()`         | `True`  |
| **`isdecimal()`**    | Contains only decimal numbers (0–9).                              | `'123'.isdecimal()`       | `True`  |
| **`isdigit()`**      | Contains digits (includes superscripts, subscripts).              | `'²'.isdigit()`           | `True`  |
| **`isnumeric()`**    | Contains numeric characters (includes fractions, roman numerals). | `'⅕'.isnumeric()`         | `True`  |
| **`islower()`**      | All characters are lowercase.                                     | `'python'.islower()`      | `True`  |
| **`isupper()`**      | All characters are uppercase.                                     | `'PYTHON'.isupper()`      | `True`  |
| **`istitle()`**      | Follows title case (first letter of each word uppercase).         | `'Hello World'.istitle()` | `True`  |
| **`isspace()`**      | Contains only whitespace.                                         | `'   '.isspace()`         | `True`  |
| **`isidentifier()`** | Valid Python identifier (variable name).                          | `'var_1'.isidentifier()`  | `True`  |
| **`isprintable()`**  | All characters are printable (no control characters).             | `'Hello\n'.isprintable()` | `False` |

---

## ✂️ Trimming & Splitting Strings

| Method                        | Description                                             | Example                  | Output          |
| ----------------------------- | ------------------------------------------------------- | ------------------------ | --------------- |
| **`strip([chars])`**          | Removes whitespace (or specified chars) from both ends. | `' hello '.strip()`      | `'hello'`       |
| **`lstrip([chars])`**         | Removes whitespace (or specified chars) from the left.  | `'  hello'.lstrip()`     | `'hello'`       |
| **`rstrip([chars])`**         | Removes whitespace (or specified chars) from the right. | `'hello  '.rstrip()`     | `'hello'`       |
| **`split([sep, maxsplit])`**  | Splits string by separator into a list.                 | `'a,b,c'.split(',')`     | `['a','b','c']` |
| **`rsplit([sep, maxsplit])`** | Like `split()` but starts from right.                   | `'a,b,c'.rsplit(',',1)`  | `['a,b','c']`   |
| **`splitlines([keepends])`**  | Splits at line breaks (`\n`, `\r`).                     | `'a\nb\nc'.splitlines()` | `['a','b','c']` |

---

## 🔗 Joining & Aligning

| Method                      | Description                                       | Example                   | Output     |
| --------------------------- | ------------------------------------------------- | ------------------------- | ---------- |
| **`join(iterable)`**        | Joins iterable elements with string between them. | `'-'.join(['a','b','c'])` | `'a-b-c'`  |
| **`center(width[, fill])`** | Centers string within width.                      | `'hi'.center(6,'*')`      | `'**hi**'` |
| **`ljust(width[, fill])`**  | Left-aligns string.                               | `'hi'.ljust(6,'-')`       | `'hi----'` |
| **`rjust(width[, fill])`**  | Right-aligns string.                              | `'hi'.rjust(6,'-')`       | `'----hi'` |
| **`zfill(width)`**          | Pads with zeros on the left.                      | `'42'.zfill(5)`           | `'00042'`  |

---

## 🔍 Searching & Checking Substrings

| Method                                 | Description                                             | Example                    | Output |
| -------------------------------------- | ------------------------------------------------------- | -------------------------- | ------ |
| **`find(sub[, start, end])`**          | Returns lowest index of substring or `-1` if not found. | `'banana'.find('na')`      | `2`    |
| **`rfind(sub[, start, end])`**         | Returns highest index of substring or `-1`.             | `'banana'.rfind('na')`     | `4`    |
| **`index(sub[, start, end])`**         | Like `find()` but raises `ValueError` if not found.     | `'banana'.index('na')`     | `2`    |
| **`rindex(sub[, start, end])`**        | Like `rfind()` but raises `ValueError`.                 | `'banana'.rindex('na')`    | `4`    |
| **`count(sub[, start, end])`**         | Counts number of occurrences of substring.              | `'banana'.count('a')`      | `3`    |
| **`startswith(prefix[, start, end])`** | Returns `True` if string starts with prefix.            | `'hello'.startswith('he')` | `True` |
| **`endswith(suffix[, start, end])`**   | Returns `True` if string ends with suffix.              | `'hello'.endswith('lo')`   | `True` |

---

## 🔄 Replacing & Formatting

| Method                           | Description                                 | Example                                             | Output                |
| -------------------------------- | ------------------------------------------- | --------------------------------------------------- | --------------------- |
| **`replace(old, new[, count])`** | Replaces occurrences of substring.          | `'hi hi'.replace('hi','bye')`                       | `'bye bye'`           |
| **`format(*args, **kwargs)`**    | Inserts variables into placeholders `{}`.   | `'Hello {}'.format('Mashud')`                       | `'Hello Mashud'`      |
| **`format_map(mapping)`**        | Like `format()` but uses dict directly.     | `'Hi {name}'.format_map({'name':'Mashud'})`         | `'Hi Mashud'`         |
| **`translate(mapping)`**         | Replace characters using translation table. | `'abc'.translate(str.maketrans({'a':'1','b':'2'}))` | `'12c'`               |
| **`maketrans()`**                | Creates mapping for `translate()`.          | `str.maketrans('abc','123')`                        | `{97:49,98:50,99:51}` |

---

## ⚙️ Partitioning Strings

| Method                | Description                                     | Example                        | Output                  |
| --------------------- | ----------------------------------------------- | ------------------------------ | ----------------------- |
| **`partition(sep)`**  | Splits string into tuple: (before, sep, after). | `'hello world'.partition(' ')` | `('hello',' ','world')` |
| **`rpartition(sep)`** | Splits from right side.                         | `'a-b-c'.rpartition('-')`      | `('a-b','-','c')`       |

---

## 🧰 Miscellaneous Methods

| Method                         | Description               | Example                | Output     |
| ------------------------------ | ------------------------- | ---------------------- | ---------- |
| **`expandtabs(tabsize=8)`**    | Converts `\t` to spaces.  | `'a\tb'.expandtabs(4)` | `'a   b'`  |
| **`encode(encoding='utf-8')`** | Converts string to bytes. | `'hello'.encode()`     | `b'hello'` |

---

## 🧩 Bonus: String Formatting with f-Strings

| Syntax             | Description                                 | Example                          | Output           |
| ------------------ | ------------------------------------------- | -------------------------------- | ---------------- |
| **`f"..."`**       | Modern way to format strings (Python 3.6+). | `name='Mashud'; f"Hello {name}"` | `'Hello Mashud'` |
| **`f"{x:.2f}"`**   | Format numbers (2 decimal places).          | `x=3.1416; f"{x:.2f}"`           | `'3.14'`         |
| **`f"{var:>10}"`** | Align right in 10 spaces.                   | `var='hi'`                       | `'        hi'`   |

---




