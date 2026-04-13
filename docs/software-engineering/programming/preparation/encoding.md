# Encoding

## Character Set

### General

- ASCII
- Unicode/UTF

------

### Regional-Language

| Character Set | Language |
|-------------|--------------|
|Big5 | 繁体中文 (Double Byte) |
|GBK/GB2312 | 简体中文 (Double Byte)|
|Shift-JIS / EUC-J | 日语 (Double Byte)|
|EUC-KR | 韩语 (Double Byte)|
|ISO 8859 系列 | 欧洲/阿拉伯|
|KOI8-R/KOI8-U | 俄语/乌克兰语 （Single Byte）|
|Latin-1 | 西欧语言|

------

## Text Escape

- HTML-Entities
- URL-Encoding
- Quoted-Printable (MIME)
- Base64/Base32/Base16

------

## Text Serialization

- JSON
- XML
- YAML
- TOML
- CSV

------

## Regular Expressions

- [正则表达式必知必会]({{ files_server }}/software-engineering/programming/preparation/正则表达式必知必会(修订版).pdf)
- [精通正则表达式 3rd]({{ files_server }}/software-engineering/programming/preparation/精通正则表达式(第3版).epub)
- [RegExr](https://regexr.com/)
- [Regex Vis](https://regex-vis.com/)
- grep
- Hyperscan
- PCRE
- RE2
- Python/Perl/JavaScript Built-in Mdules

## Number System

### Decimal | Base-10

这是人类文明最通用的进制，起源于人类有十根手指。

- **符号：** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
- **规则：** 逢十进一。
- **应用：** 日常生活中的几乎所有场景（货币、长度、统计等）。

### Binary | Base-2

计算机底层运算的基石。物理层面上对应电路的“开”与“关”（高低电平）。

- **符号：** 0, 1
- **规则：** 逢二进一。
- **应用：** 逻辑电路、机器语言、数据存储。在编程中常以 `0b` 开头表示（如 `0b1010`）。

### Hexadecimal | Base-16

二进制的“高级缩写”。由于 $2^4 = 16$，一位十六进制数可以精确代表四位二进制位（4 bits），极大提高了可读性。

- **符号：** 0-9 加上 A-F（A=10, B=11, C=12, D=13, E=14, F=15）。
- **规则：** 逢十六进一。
- **应用：** 内存地址、颜色代码（如 `#FFFFFF`）、MAC地址、十六进制编辑器。常以 `0x` 开头（如 `0x4A`）。

### Octal | Base-8

在早期的计算机系统中较为流行（如 12 位或 36 位系统），现在使用频率已大幅降低。

- **符号：** 0, 1, 2, 3, 4, 5, 6, 7
- **规则：** 逢八进一。
- **应用：** Unix/Linux 文件权限（如 `chmod 755` 代表 `rwxr-xr-x`）。常以 `0o` 或 `0` 开头。

------

### Contrast

| **进制**     | **基数** | **常用符号** | **示例 (十进制的 255)** |
| ------------ | -------- | ------------ | ----------------------- |
| **二进制**   | 2        | 0-1          | `11111111`              |
| **八进制**   | 8        | 0-7          | `377`                   |
| **十进制**   | 10       | 0-9          | `255`                   |
| **十六进制** | 16       | 0-9, A-F     | `FF`                    |

