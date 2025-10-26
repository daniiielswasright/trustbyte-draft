Unicode assigns a unique code point to every character, symbol, and control mark—enabling consistent representation across systems, languages, and encodings. This guide focuses on the operational subset most relevant to this repo.

### FAQ
**Q**:

## ASCII

ASCII (American Standard Code for Information Interchange) is a character set that defines 128 symbols, each assigned a unique number from 0 to 127. These include:

| Group         | Range  | Notes                                    |
| ------------- | ------ | ---------------------------------------- |
| Control chars | 0–31   | Non-printable (e.g. NULL, BEL, ESC)      |
| Printable     | 32–126 | Includes space, symbols, digits, letters |
| Digits        | 48–57  | '0' to '9'                               |
| Uppercase A–Z | 65–90  | Sequential, but offset from digits       |
| Lowercase a–z | 97–122 | Sequential, offset from uppercase        |
|               |        |                                          |

### Uppercase Letters 
This section catalogs all printable ASCII letters—uppercase A–Z and lowercase a–z—with their Unicode code points, decimal values, and hex representations. These characters form the baseline for identifier integrity, spoof detection, and homoglyph mapping.

| Upper | Codepoint | Dec | Hex  | Lower | Codepoint | Dec | Hex  |
| ----- | --------- | --- | ---- | ----- | --------- | --- | ---- |
| A     | U+0041    | 65  | 0x41 | a     | U+0061    | 97  | 0x61 |
| B     | U+0042    | 66  | 0x42 | b     | U+0062    | 98  | 0x62 |
| C     | U+0043    | 67  | 0x43 | c     | U+0063    | 99  | 0x63 |
| D     | U+0044    | 68  | 0x44 | d     | U+0064    | 100 | 0x64 |
| E     | U+0045    | 69  | 0x45 | e     | U+0065    | 101 | 0x65 |
| F     | U+0046    | 70  | 0x46 | f     | U+0066    | 102 | 0x66 |
| G     | U+0047    | 71  | 0x47 | g     | U+0067    | 103 | 0x67 |
| H     | U+0048    | 72  | 0x48 | h     | U+0068    | 104 | 0x68 |
| I     | U+0049    | 73  | 0x49 | i     | U+0069    | 105 | 0x69 |
| J     | U+004A    | 74  | 0x4A | j     | U+006A    | 106 | 0x6A |
| K     | U+004B    | 75  | 0x4B | k     | U+006B    | 107 | 0x6B |
| L     | U+004C    | 76  | 0x4C | l     | U+006C    | 108 | 0x6C |
| M     | U+004D    | 77  | 0x4D | m     | U+006D    | 109 | 0x6D |
| N     | U+004E    | 78  | 0x4E | n     | U+006E    | 110 | 0x6E |
| O     | U+004F    | 79  | 0x4F | o     | U+006F    | 111 | 0x6F |
| P     | U+0050    | 80  | 0x50 | p     | U+0070    | 112 | 0x70 |
| Q     | U+0051    | 81  | 0x51 | q     | U+0071    | 113 | 0x71 |
| R     | U+0052    | 82  | 0x52 | r     | U+0072    | 114 | 0x72 |
| S     | U+0053    | 83  | 0x53 | s     | U+0073    | 115 | 0x73 |
| T     | U+0054    | 84  | 0x54 | t     | U+0074    | 116 | 0x74 |
| U     | U+0055    | 85  | 0x55 | u     | U+0075    | 117 | 0x75 |
| V     | U+0056    | 86  | 0x56 | v     | U+0076    | 118 | 0x76 |
| W     | U+0057    | 87  | 0x57 | w     | U+0077    | 119 | 0x77 |
| X     | U+0058    | 88  | 0x58 | x     | U+0078    | 120 | 0x78 |
| Y     | U+0059    | 89  | 0x59 | y     | U+0079    | 121 | 0x79 |
| Z     | U+005A    | 90  | 0x5A | z     | U+007A    | 122 | 0x7A |

---

---

### printable non letters 

| Char | Codepoint | Dec | Hex  | Description        |
|------|-----------|-----|------|--------------------|
| ␣    | U+0020    |  32 | 0x20 | Space              |
| !    | U+0021    |  33 | 0x21 | Exclamation mark   |
| "    | U+0022    |  34 | 0x22 | Quotation mark     |
| #    | U+0023    |  35 | 0x23 | Number sign        |
| $    | U+0024    |  36 | 0x24 | Dollar sign        |
| %    | U+0025    |  37 | 0x25 | Percent sign       |
| &    | U+0026    |  38 | 0x26 | Ampersand          |
| '    | U+0027    |  39 | 0x27 | Apostrophe         |
| (    | U+0028    |  40 | 0x28 | Left parenthesis   |
| )    | U+0029    |  41 | 0x29 | Right parenthesis  |
| *    | U+002A    |  42 | 0x2A | Asterisk           |
| +    | U+002B    |  43 | 0x2B | Plus sign          |
| ,    | U+002C    |  44 | 0x2C | Comma              |
| -    | U+002D    |  45 | 0x2D | Hyphen-minus       |
| .    | U+002E    |  46 | 0x2E | Period             |
| /    | U+002F    |  47 | 0x2F | Slash              |
| :    | U+003A    |  58 | 0x3A | Colon              |
| ;    | U+003B    |  59 | 0x3B | Semicolon          |
| <    | U+003C    |  60 | 0x3C | Less-than sign     |
| =    | U+003D    |  61 | 0x3D | Equals sign        |
| >    | U+003E    |  62 | 0x3E | Greater-than sign  |
| ?    | U+003F    |  63 | 0x3F | Question mark      |
| @    | U+0040    |  64 | 0x40 | At sign            |
| [    | U+005B    |  91 | 0x5B | Left bracket       |
| \    | U+005C    |  92 | 0x5C | Backslash          |
| ]    | U+005D    |  93 | 0x5D | Right bracket      |
| ^    | U+005E    |  94 | 0x5E | Caret              |
| _    | U+005F    |  95 | 0x5F | Underscore         |
| `    | U+0060    |  96 | 0x60 | Grave accent       |
| {    | U+007B    | 123 | 0x7B | Left brace         |
|     | U+007C    | 124 | 0x7C | Vertical bar       |
| }    | U+007D    | 125 | 0x7D | Right brace        |
| ~    | U+007E    | 126 | 0x7E | Tilde              |

---

#### Digits

| Char | Codepoint | Dec | Hex  | Description   |
|------|-----------|-----|------|---------------|
| 0    | U+0030    |  48 | 0x30 | Digit zero    |
| 1    | U+0031    |  49 | 0x31 | Digit one     |
| 2    | U+0032    |  50 | 0x32 | Digit two     |
| 3    | U+0033    |  51 | 0x33 | Digit three   |
| 4    | U+0034    |  52 | 0x34 | Digit four    |
| 5    | U+0035    |  53 | 0x35 | Digit five    |
| 6    | U+0036    |  54 | 0x36 | Digit six     |
| 7    | U+0037    |  55 | 0x37 | Digit seven   |
| 8    | U+0038    |  56 | 0x38 | Digit eight   |
| 9    | U+0039    |  57 | 0x39 | Digit nine    |
