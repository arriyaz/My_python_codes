## Take input from user by a prompt
```python
name = input("What is your name: ")
print(name)
```
### Writing Clear Prompts
Sometimes you’ll want to write a prompt that’s longer than one line. For example, you might want to tell the user why you’re asking for certain input. You can assign your prompt to a variable and pass that variable to the `input()` function. This allows you to build your prompt over several lines, then write a clean `input()` statement. For example:

```python
msg = "I will print your name on the screen"
msg += "\nWhat is your name: "

name = input(msg)
print(name)
```
