# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/6dd54fc4-307f-45ea-b32a-f62d4197d1c0)



cat < file2
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/a1f7d6ee-6ba6-430b-ae93-cdd7b1d4ef1d)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/eaea9c6e-e1fc-4276-87bb-826f5f88e650)

comm file1 file2
 ## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/e54cb632-db30-44a2-8e61-6f114c55ee5d)

 
diff file1 file2
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/4136696f-786d-4cf3-bf4c-6524f78bb07b)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/73772267-86c3-4f6d-8218-2b0ed4ecc166)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/8eb4e3d0-d130-422e-8ca7-a08292847fb8)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/f48724e9-561e-474b-8518-02ab83d4d835)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/12bcf8b4-326d-4efb-95fb-068181ce0b50)



grep hello newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/b0221d4c-244c-4f35-9e18-8b4e9729cc86)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/4547a27a-fca4-4005-a000-c4f01d0b6c3f)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/0ba5e92a-1d12-4902-9984-224b3a55fa46)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/3bbccc92-f007-464c-a7de-805d67bb6207)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/3b2093b7-4953-41c2-adbc-d39e3df16ad8)



grep -w -n world newfile   
## OUTPUT


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/fdc66d0c-6b78-43e4-811f-f671e93d1c16)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/c856debc-b391-4e09-ad49-2c68c68dee34)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/0938097c-3091-478e-8b2a-8d1fe8114953)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/76a2d60b-79a2-47b5-9f56-b044d1fdee1d)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/b1f2bc72-8f01-4651-9344-28cced55614c)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/9afa1d3b-cbf8-416f-a12f-499ac19e7d5d)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/4d3d3a56-075d-433d-90bd-6b02500361b7)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/ca8f2044-e96a-4e9f-aaa6-a707bf831258)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/56967860-eab2-4a76-8ccf-cb50c7f00536)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/c613f6fd-ae34-4895-a118-bcaea1244f27)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/bc4f6e72-b350-452a-8044-cbd19a38c396)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/43137b78-5d78-4b5d-9ea4-719a00cf44e1)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/84f20ccc-e710-4e1e-bd1a-5eef1bf1426c)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/3d830f80-86cd-4b47-91ab-fb5c1c79d9a3)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/cacac2c3-8162-440c-8572-7df2c066e933)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/bc3bad41-5125-497d-9bd5-a474adb37087)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/8d2f290c-ea9e-4e3f-b07a-86a9c9ac9121)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/23f7be4c-2361-42c5-887a-75fcb065f501)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/9a6d81d9-6588-4404-8c4a-c22c551595c9)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/845e5856-36b4-4e27-ba7e-97f908e7b305)


seq 10 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/aa2db961-6eb3-458e-9bc7-d8111ff8453f)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/9431c2fa-abb8-4415-a340-a37249f30751)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/a4df66a8-b85b-454b-9166-438bec80630c)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/bebeeeb6-0f16-4bb3-a9fc-47016bc986a2)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/dc62b988-8c2c-4279-afe2-2653482cce55)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/0707edfc-302c-4a16-aa5d-8b90855b147b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/bf2a2b8c-991b-4ce0-89a7-08290e5c5b8b)



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/8c39d437-4fa1-433c-83fd-7b8291d7651f)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/90944e6c-99c7-4755-96b2-50f5efccd437)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/f99a8c0d-b3f5-4858-a98e-673d898c8a11)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/f48fcab6-1bd8-434c-84fc-02898e6e46bc)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/9f129131-0f06-4184-a880-904f7f29da2b)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/6c6bef99-7b72-437c-a8ee-fdb6109340b0)


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/db1c702b-cc41-49b1-b215-c0705cd3f061)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/74810b17-c385-478f-af6a-b06e651c72d1)

 
ls file1
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/5f2283c1-6383-4504-b56a-fbb8501197d7)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/420c7005-1947-4751-9deb-762d22f8a344)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/4c58f105-3037-40da-9ef8-484cb04baee5)


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/72b6fcea-16bf-4def-83b6-c3f2eec9d414)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/cbab73b8-43f7-46c4-962d-72929b980aea)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/ef4a8379-7f9b-450f-b9cd-ad02b4233e41)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/9b99c860-f3a2-46ef-847d-30036d9837a8)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/0436f168-cbed-4fda-8a2c-6d64e6964a0a)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/7d1869b5-f926-4d71-bd71-5e96ff6de918)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/f28927fb-b2d4-4459-a1c2-ce5fe8d11033)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/422edb9e-2451-4dfb-911e-7a2d3d5fc2ab)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/003214c0-11d1-493b-81be-e67cd6ad7812)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/e9e554cf-2ecd-495b-93b0-f5cff36e0f29)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/44ee34f4-5137-4f4a-8f4b-5d90720c1a29)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/69c82e3e-3ce8-46fe-884e-ce44d533c35c)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/e4f3208d-2381-4f20-8201-c972ae2da92d)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/356db1fd-ac51-4a3e-b193-7bfe717a0668)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/770baef3-aa9c-4980-8ce1-45587797a9ad)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/e2bf06a6-a4fa-4905-9f46-18973f531dac)

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/a028c1d4-c406-4d42-b4f0-ffc829c44c9a)

$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/9161c59d-87a4-4ba6-85de-20c48c96dc41)

$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 ![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/bb9320c9-59fc-4405-95c3-fe8913343b22)

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/c61066df-36f7-48c8-95a2-cb5f4cd3bf12)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/Mrnithishx/OS-Linux-commands-Shell-script/assets/148201573/3ca89964-c060-409d-9935-7f45cda06e5f)


# RESULT:
The Commands are executed successfully.
