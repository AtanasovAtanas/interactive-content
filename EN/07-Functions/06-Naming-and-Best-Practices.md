# Naming and Best Practices

[slide]
# Best Function Practices

 - Each function should perform a **single**, well-defined task.
 - **Avoid long functions**, **split** them into **several shorter ones**.

 ```python
 def print_receipt():
    print_header()
    print_body()
    print_footer()
 ```

 Following the practices, the function defined in the example above is **self-documenting** and **easy to test**.

[/slide]

[slide]
# Naming Functions

 - Function names should **describe their task** in a **clear** and **unambigious** way
 - Their names should be **meaningful and not very long**
 - Should answer the question: "**What does this function do?**"

Examples for **good** names:
```python
find_student, load_report, sine
```

Examples for **bad** names:
```python
do_something, handle_stuff, dirtyHack
```

If you **cannot** find a **good name** for a function, think about **whether it has a clear intent**.

[/slide]

[slide]
# Naming Function Parameters

 - Preferred form: `[Noun]` or `[Adjective] + [Noun]`
 - Should **not** have **capital** letters
 - Should be **meaningful**
 - Unit of measure should be obvious

Examples for **good** parameter names:
```python
first_name, report, speed, users_list, font_size, font
```

Examples for **bad** parameter names:
```python
p, p1, p2, populate, LastName, lastName
```

[/slide]