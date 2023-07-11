# Building a build script

`script.sh`

```bash
#!/bin/bash

echo "Welcome to the build script"

firstline=$(head -n 1 source/changelog.md)

read -a splitfirstline <<< $firstline

version=${splitfirstline[1]}

echo "You are building version" $version

echo 'Are you sure that you want to build this version? (y/yes n/no)'
read versioncontinue

if [ $versioncontinue == "y" ]
then
  for filename in source/*
  do
    if [ "$filename" == "source/secretinfo.md" ]
    then
      echo "Filtering" $filename
      sed -i 's/42/XX/g' $filename
      echo "Filtered" $filename
      cp $filename build/
    else
      echo "Copying" $filename
      cp $filename build/.
    fi
  done
  cd build/
  echo "Build version $version contains:"
  ls
else
  echo "Please come back when you are ready"
fi
```
