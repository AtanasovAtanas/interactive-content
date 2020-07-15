# RegEx in Python

[slide]
# Video

[vimeo-video startTimeInSeconds="5508" endTimeInSeconds="5724"]
[stream language="EN" videoId="435033424" default /]
[stream language="RO" videoId="435046150"  /]
[/video-vimeo]

[/slide]

[slide]
# RegEx Module

Python has a built-in package called `re` module, which provides regular expression support.

It can be used to work with Regular Expressions.

Import the re module as follows:

```Python
import re
```

## Examples

```Python live
import re

txt = "The sun is shining in Bucharest"
x = re.search("^The.*Bucharest$", txt)

if x:
  print("It's a match!")
else:
  print("No match!")
```

- With this pattern `^The.*Bucharest$`, we check if the string starts with `The` and ends with `Bucharest`.

Here we use our simple e-mail validator from the `RegEx Definition` slide to match a correct e-mail:

```Python live
import re

email = input()
isMatch = re.search("^\S+@\S+$", email)

if isMatch:
  print("Correct email!")
else:
  print("Incorrect email!")
```
[/slide]