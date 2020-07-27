# Syntax

[slide]
# Video

[vimeo-video startTimeInSeconds="1495" endTimeInSeconds="5508"]
[stream language="EN" videoId="435033424" default /]
[stream language="RO" videoId="435046150"  /]
[/video-vimeo]

[/slide]

[slide]
# Syntax

Here we'll look at basic RegEx syntax.

- Special sequences

| **Notation** | **Meaning (Returns a match where…)** |
| --- | --- |
|`\d`|the string contains digits, numbers from `0-9`|
|`\D`|the string **DOES NOT** contain **digits**|
|`\b`|the specified characters are at the **beginning** or at the **end** of a word|
|`\s`|the string contains a **white space character**|
|`\S`|the string **DOES NOT** contain a **white space character**|
|`\w`|the string contains any word characters from `a` to `Z`, digits from `0-9`, and the underscore `_` character|
|`\W`|the string **DOES NOT** contain any **word characters**|

- Metacharacters

| **Notation** | **Meaning** |
| --- | --- |
|`\`|Signals a special **sequence** can also be used to **escape** special characters|
|`.`|**Any character** except newline character|
|`+`|**One or more** occurrences|
|`*`|Zero or more occurrences|
|`|`|Either or|
|`()`|Capture and group|
|`{}`|**Exactly** the specified number of occurrences|
|`^`|Starts with|
|`$`|Ends with|

- Sets

| **Examples** | **Meaning (Returns a match …)** |
| --- | --- |
|`[arn]`|where one of the specified characters (`a`, `r`, or `n`) are present|
|`[a-n]`|for any lowercase character, alphabetically between `a` and `n`|
|`[^arn]`|for any character **EXCEPT** `a`, `r`, and `n`|
|`[0123]`|where any of the specified digits `0`, `1`, `2`, or `3` are present|
|`[0-9]`|for any digit between `0` and `9`|
|`[0-5][0-9]`|for any two-digit numbers from `00` and `59`|
|`[a-zA-Z]`|for any character alphabetically between `a` and `z`, **lower case OR upper case**|

We encourage you to play around with [Pythex](https://pythex.org), so you can get a good feeling for basic matching patterns.

[/slide]