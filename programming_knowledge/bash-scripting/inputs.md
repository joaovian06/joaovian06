# Inputs

To make bash scripts more useful, we need to be able to access data external to the bash script file itself. The first way to do this is by prompting the user for input. For this, we use the `read` syntax. To ask the user for input and save it to the `number` variable, we would use the following code:

```bash
echo "Guess a number"
read number
echo "You guessed $number"
```

Another way to access external data is to have the user add input arguments when they run your script. These arguments are entered after the script name and are separated by spaces. For example:

`saycolors red green blue`

Within the script, these are accessed using `$1`, `$2`, etc, where `$1` is the first argument (here, “red”) and so on. Note that these are 1 indexed.

If your script needs to accept an indefinite number of input arguments, you can iterate over them using the `"$@"` syntax. For our saycolors example, we could print each color using:

```bash
for color in "$@"
do
echo $color
done
```

Lastly, we can access external files to our script. You can assign a set of files to a variable name using standard bash pattern matching using regular expressions. For example, to get all files in a directory, you can use the `*` character:

`files=/some/directory/*`

You can then iterate through each file and do something. Here, lets just print the full path and filename:

```bash
for file in $files
do
    echo $file
done
```

---

`script.sh`

```bash
#!/bin/bash
first_greeting="Nice to meet you!"
later_greeting="How are you?"
greeting_occasion=0
echo "How many times should I greet?"
read greeting_limit
while [ $greeting_occasion -lt $greeting_limit ]
do
  if [ $greeting_occasion -lt 1 ]
  then
    echo $first_greeting
  else
    echo $later_greeting
  fi
  greeting_occasion=$((greeting_occasion + 1))
done
```
