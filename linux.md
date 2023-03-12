# Linux :


change from formatting branch

#commands :

**date**

**cal** (calender)

**memory** : 

**df**

**free**

**pwd :** shows the present working directory on the shell op.

path : if the path start with a ‘/’ , the path is absolute vs if you have path w/o ‘/’ it’s relative.

**cd** : change directory

**ls** : lists all the files/folders in a folder.

```bash
ls path 
```

commands have options , these options are 

1. single alphabet (-)
2. verbose ( - -)

| -l | long format |
| --- | --- |
| -a | hidden files |
| -t | time |
| -s | size |

##wildcard : 

“*” File* → match any number or chars 

? FILE? → match a single char

[[:char_classes]] → upper,lower,digit,alpha,alnum

************mkdir************  :used to create directories

```bash
mkdir dir_name
//to create multiple
mkdir dir1 dir2
```

************touch************ 

```bash
touch file_name #to create files, can create multiple if they are space seperated
```

**********rm :********** 

```bash
rm path //can be a folder or a file
rm -r folder //to remove a folder
rm -i for warning
```

********cp :********

```bash
cp file1 file2 #can be absolute path or relative path
cp file1 folder #copies file1 into folder
cp -r folder1 folder2 #copies all the contents of a folder into another

```

3 components for processes :

**stdin** → 0

**stdout** → 1

**stderr** → 2

1. using the > symbol.

output > where_to_redirect (normally some file)

by default redirect will overwrite.

to append instead of overwrite while using redirection 

output >> where_to_redirect_append (normally some file)

to redirect error 

stderr 2> where_to_redirect

to redirect both : 

cat command_with_stdout_and_stderr > output_file 2>&1

vi editor:

i for insert mode → make changes

esc to escape insert mode

:q! to exit without saving changes

:wq! to exit and save changes

**history**

**man :**

```bash
man command #opens up the manual  for the command press q to exit
```

**pipeline :** 

|

```bash
command1 | command2

ls fol1 fol2 | sort | less 
```

****wc****

word count

```bash
wc filename
wc -l filename
```

********grep********

```bash
ls | grep keyword #grep by def is case sensative
ls | grep -i keyword #for case insensitivity
#to look at the contents of a file with a keyword highlighted:
cat file_name | grep keyword
```

********************head/tail******************** 

```bash
head -n no_of_lines file_name #first n lines of a file
tail -n no_of_lines file_name #last n lines of a file
tail -f file_name
```

**echo** 

```bash
to give output on shell

```

******{}******

```bash
{} can be used to create multiple file/folders

touch file_{1..4} #creates file_1, file_2, file_3, file_4

```

User access: 

entities that can access a resource

1. User
2. Group 
3. World

Access signature for a file/folder :

-rwxrwxrwx → file

drwxrwxrwx → folder

Firsth char of access signature represents file/folder :

-→ file

d → folder

rwx   rwx  rwx

**chmod** 

```bash
chmod ooo # [0-7][0-7][0-7]
chmod – Change File Mode
0 000 ---
1 001 --x
2 010 -w
3 011 -wx
4 100 r--
5 101 r-x
6 110 rw
7 111 rwx

chown 
```