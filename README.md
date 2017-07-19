## Examples of
# Text File Manipulation Tools

### Linux Command Line

These are the following tools that will work on this post.

| Tool |
| ------ |
| tr |
| sort | 
| diff Drive |
| uniq | 
| cut | 
| Basic regular expressions | 
| grep | 
| sed | 
| awk |
| find | 


### Working with tr

```sh
$ cat example  | tr a-z A-Z
```

On the next example the content of example use of *tr* is to translate lowercase into uppercase.

```sh
$ cat example  | tr a-z A-Z > example2
```

With option *-d* (which means delete) will remove all the upper cases from the file.
```sh
$ cat example  | tr -d [:upper:]
```

This will remove all the lower cases from the file.
```sh
$ cat example  | tr -d [:lower:]
```

This command with option *-s* replaces all the upper letter with & but will delete ocurrences.
```sh
$ cat example  | tr -s [:upper:] '&'
```

This command with option *-d* replaces all the upper letter with & but will not delete ocurrences.
```sh
$ cat example  | tr -t [=d=] '*'
```

This command with option *-c* which is complement, will replace all the letters that does not have upper case with a *.

 ```sh
$ cat example  | tr -c [:upper:] '*'
```

### Working with sort

Consider only blanks and alphanumeric characters *-d*
 ```sh
$ sort users -d
```

You can also use the built-in sort option *-o*, which allows you to specify an output file:
 ```sh
$ sort -o output.txt users
```

You can perform a reverse-order sort using the *-r* flag. For example, the following command:
 ```sh
$ sort -r users
```

If you just want to check to see if your input file is already sorted, use the *-c* option:
 ```sh
$ sort -c users
```

Also useful is the option *-n* , which makes sure that numbers are sorted correctly
 ```sh
$ sort -n users
```
