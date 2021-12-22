---
layout:     post
title:     Learn bash Scripting
subtitle:   BY Guanqiao Huang
date:       2020-12-15
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - CLI
---
# LEARN BASH SCRIPTING
- Any command that can be run in the terminal can be run in a bash script.
- Variables are assigned using an equals sign with no space (`greeting="hello"`).
- Variables are accessed using a dollar sign (`echo $greeting`).
- Conditionals use `if`, `then`, `else`, `fi` syntax.
- Three types of loops can be used: `for`, `while`, and `until`.
- Bash scripts use a unique set of comparison operators:
1. Equal: `-eq`
2. Not equal: `-ne`
3. Less than or equal: `-le`
4. Less than: `-lt`
5. Greater than or equal: `-ge`
6. Greater than: `-gt`
7. Is null: `-z`
- Input arguments can be passed to a bash script after the script name, separated by spaces (myScript.sh “hello” “how are you”).
- Input can be requested from the script user with the read keyword.
- Aliases can be created in the .bashrc or .bash_profile using the alias keyword.

# Examples
## Example 1
```Bash
#!/bin/bash
first_greeting="Nice to meet you!"
later_greeting="How are you?"
greeting_occasion=0
greeting_limit=$1
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