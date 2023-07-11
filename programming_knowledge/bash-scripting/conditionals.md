# Conditionals

When bash scripting, you can use conditionals to control which set of commands within the script run. Use `if` to start the conditional, followed by the condition in square brackets (`[ ]`). Make sure you leave a space between a bracket and the conditional statement! `then` begins the code that will run if the condition is met. `else` begins the code that will run if the condition is not met. Lastly, the conditional is closed with a backwards `if`, `fi`.

A complete conditional in a bash script uses the following syntax:

```bash
if [ $index -lt 5 ]
then
  echo $index
else
  echo 5
fi
```

Bash scripts use a specific list of operators for comparison. Here we used `-lt` which is “less than”. The result of this conditional is that if `$index` is less than 5, it will print to the screen. If it is 5 or greater, “5” will be printed to the screen.

Here is the list of comparison operators for numbers you can use within bash scripts:

Equal: `-eq`
Not equal: `-ne`
Less than or equal: `-le`
Less than: `-lt`
Greater than or equal: `-ge`
Greater than: `-gt`
Is null: `-z`
When comparing strings, it is best practice to put the variable into quotes (`"`). This prevents errors if the variable is null or contains spaces. The common operators for comparing strings are:

Equal: `==`
Not equal: `!=`
For example, to compare if the variables `foo` and `bar` contain the same string:

```bash
if [ "$foo" == "$bar" ]
```

`script.sh`

```bash
#!/bin/bash

first_greeting="Nice to meet you!"
later_greeting="How are you?"
greeter_occasion=0

if [ $greeting_occasion -lt 1 ]
then
    echo $first_greeting
else
    echo $later_greeting
fi
```
