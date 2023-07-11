# Aliases

You can set up aliases for your bash scripts within your `.bashrc` or `.bash_profile` file to allow calling your scripts without the full filename. For example, if we have our `saycolors.sh` script, we can alias it to the word `saycolors` using the following syntax:

```bash
alias saycolors='./saycolors.sh'
```

You can even add standard input arguments to your alias. For example, if we always want “green” to be included as the first input to `saycolors`, we could modify our alias to:

```bash
alias saycolors='./saycolors.sh "green"'
```
