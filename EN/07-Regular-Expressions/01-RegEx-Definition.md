# RegEx Definition

[slide]
# Video

[vimeo-video startTimeInSeconds="999" endTimeInSeconds="1495"]
[stream language="EN" videoId="435033424" default /]
[stream language="RO" videoId="435046150"  /]
[/video-vimeo]

[/slide]

[slide]
# What Is RegEx?

A regular expression or regex is a sequence of characters that define a search pattern.

A RegEx pattern is a special language used to represent text, numbers, or symbols so it can be used to extract texts that conform to that pattern.

A regular expression or `RegEx`:

- can be used to check if a string contains the specified search pattern

- is used by string searching algorithms for `find` or `find and replace` operations on strings

- is used in search engines, search and replace dialogs of word processors and text editors

# Example

Let's say you want to **validate** if an **e-mail** is valid, it should follow these rules:

- have only alphanumeric characters
- include `@`
- end with `.com`, `.ro`, `.net`

Here is an example for very basic e-mail validator: 

- `^\S+@\S+$`: this is how a simple RegEx looks like.

Without RegEx will be very **difficult** to validate an e-mail address.

At first look this may not mean much to you, but after this lecture you'll understand what each symbol means.


# Pythex

When you create RegEx, there is a fast way to find out is your RegEx correct. You can use [Pythex](https://pythex.org). This is a platform where you can upload your string and write a RegEx and see do you match the correct result.


[/slide]