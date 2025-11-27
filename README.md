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

![Screenshot from 2025-03-06 09-28-33](https://github.com/user-attachments/assets/d057f45d-7968-455b-a3bd-9bb6206192e7)


cat < file2
## OUTPUT
![Screenshot from 2025-03-08 21-04-36](https://github.com/user-attachments/assets/3cab4789-0b52-4ba2-a73b-bcc8515707e3)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-08 21-04-44](https://github.com/user-attachments/assets/360f1f8e-0467-4e5a-bfc2-0df2e74c1bea)
 
comm file1 file2
 ## OUTPUT
![Screenshot from 2025-03-08 21-04-50](https://github.com/user-attachments/assets/d2542806-6ff6-4552-8644-76c5d2917597)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-08 21-04-57](https://github.com/user-attachments/assets/a962143f-2a62-4180-9f4d-6ae271b1f533)


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
![Screenshot from 2025-03-08 21-05-09](https://github.com/user-attachments/assets/f5c80fb5-f9a9-4ac8-be0a-5776ff80b413)




cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-03-08 21-05-09](https://github.com/user-attachments/assets/1019b76d-2723-4c6f-a28c-27ed0af2fbbd)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-08 22-25-20](https://github.com/user-attachments/assets/17e91b39-2fc2-497e-91d7-c038acff4cc3)


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



grep Dhinesh newfile 
## OUTPUT
![Screenshot from 2025-03-08 22-27-26](https://github.com/user-attachments/assets/49d1abb8-9d60-405a-8306-97041dfb6321)




grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-08 22-29-19](https://github.com/user-attachments/assets/d0ccbbc4-9f3a-4c82-8416-18ce6b226e4d)



cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-08 22-30-09](https://github.com/user-attachments/assets/57ccb842-3f71-44df-ba89-6766abf6f051)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-03-08 22-30-44](https://github.com/user-attachments/assets/36c8eaaa-c736-4334-b8ce-bec26a489f18)



grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-08 22-31-08](https://github.com/user-attachments/assets/a8aec486-3ee2-4ee6-a35c-58aae6615797)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-08 21-02-40](https://github.com/user-attachments/assets/73ae3560-001a-46df-84e9-49ba6a33e329)


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

![Screenshot from 2025-03-08 21-03-08](https://github.com/user-attachments/assets/af678d33-6217-42a1-a91e-e20967a7710f)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-08 21-03-11](https://github.com/user-attachments/assets/548308f0-3a36-4e39-b72d-687e14f516a2)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-03-08 21-03-15](https://github.com/user-attachments/assets/551eac5a-0830-4b8e-bde6-86198e5fe595)



egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-03-08 21-03-21](https://github.com/user-attachments/assets/007caae4-00f4-40b7-a49f-32420205b07f)



egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-03-08 21-03-26](https://github.com/user-attachments/assets/ef1a9399-92bb-4c2f-a184-f48ca5d256f5)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-08 21-03-26](https://github.com/user-attachments/assets/521a3f1d-f83f-4b9e-8b2a-b8586055623b)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-03-08 21-03-32](https://github.com/user-attachments/assets/01926c3d-fa45-4b95-a6e6-de864c19ce47)


egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/0ee0baea-b287-4622-a853-379ffc97c609)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-08 21-03-38](https://github.com/user-attachments/assets/4b5f5253-4380-4728-b9bd-e84ab0f086cb)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-08 21-03-38](https://github.com/user-attachments/assets/c056f1bc-3849-475f-8b11-bc90f5eb8e74)


egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-08 22-18-17](https://github.com/user-attachments/assets/f5324740-2924-41f3-909a-402909c707b3)


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

![Screenshot from 2025-03-08 21-00-14](https://github.com/user-attachments/assets/3f423e23-9598-4b52-813e-80e8932f92b2)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-03-08 22-37-05](https://github.com/user-attachments/assets/a3ba9b03-52c9-467a-aaf5-19dac6d75170)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 21-00-29](https://github.com/user-attachments/assets/79de9c9b-6081-45b5-9c31-277d880b46a2)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 21-00-29](https://github.com/user-attachments/assets/90f22814-51ae-4985-b21f-c4328d90a21c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-03-04 21-56-30](https://github.com/user-attachments/assets/42609b69-1df0-4ab9-b86f-204ac03d5fc7)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-03-08 20-57-43](https://github.com/user-attachments/assets/c96e2180-bc51-4da9-81d0-4c5fb032e053)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-03-08 20-57-52](https://github.com/user-attachments/assets/76bb2a46-1ff5-4d7d-adb1-941e8bf5f997)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-08 20-57-59](https://github.com/user-attachments/assets/c6031da1-b85b-4b6b-8315-a529d71e098a)



seq 10 
## OUTPUT

![Screenshot from 2025-03-08 20-58-05](https://github.com/user-attachments/assets/5581d85b-f0b9-41cc-b7f1-cf642aa96e59)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-03-08 20-58-12](https://github.com/user-attachments/assets/f3e09bf3-d013-4137-a97e-cd160e5fa0b9)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-03-08 20-58-17](https://github.com/user-attachments/assets/c404ed36-2d2d-452d-b63c-5747d6897ef0)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-08 20-58-24](https://github.com/user-attachments/assets/d752e3d2-9245-4931-a434-e3a9c1294232)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-03-08 20-58-30](https://github.com/user-attachments/assets/8a962c5f-4651-402c-b875-3a40200995fa)

seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-08 20-58-34](https://github.com/user-attachments/assets/53cafd93-5122-4d48-a4b4-1628516be13b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-08 20-58-40](https://github.com/user-attachments/assets/edc2abe3-082f-405a-b02d-1cfaaa17083e)



sed -n '2,4{s/$/*/;p}' file23
![Screenshot from 2025-03-08 20-56-19](https://github.com/user-attachments/assets/65c41390-e087-4db7-a889-fcac22bb02d6)


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

![Screenshot from 2025-03-08 20-56-29](https://github.com/user-attachments/assets/18282f54-2096-45cc-94a3-7415554405e0)

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

![Screenshot from 2025-03-08 20-56-42](https://github.com/user-attachments/assets/cada4716-1cc1-4d6d-9dce-bb6d70efce16)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2025-03-08 20-54-55](https://github.com/user-attachments/assets/c28231ac-5fb6-4928-8433-266684048baf)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
![Screenshot from 2025-03-08 20-55-10](https://github.com/user-attachments/assets/d4444f74-dfbe-4a66-9c3e-d5b614ffcb37)

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot from 2025-03-08 20-55-17](https://github.com/user-attachments/assets/e05e2753-2ace-41ee-ba25-40e8046f0990)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-03-08 20-55-24](https://github.com/user-attachments/assets/8465acb4-3182-4b70-a76b-423b25320f1c)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-03-08 20-52-31](https://github.com/user-attachments/assets/cd254579-4391-4162-9ad3-be3784050b76)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot from 2025-03-08 20-52-39](https://github.com/user-attachments/assets/555c5a6b-10a2-4fca-ab08-506f1f88b9e9)


tar -xvf backup.tar
## OUTPUT
![Screenshot from 2025-03-08 20-52-46](https://github.com/user-attachments/assets/389bec83-3cf1-4e0c-8ecc-6655eaf3fc8a)

gzip backup.tar

ls .gz
## OUTPUT
![Screenshot from 2025-03-08 20-53-30](https://github.com/user-attachments/assets/d70e812c-b80e-4f33-9f8b-62da961822f6)

gunzip backup.tar.gz
## OUTPUT
![image-56](https://github.com/user-attachments/assets/89d205e5-4429-446a-8b51-b54f5dea82da)

 
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
![Screenshot from 2025-03-08 20-50-41](https://github.com/user-attachments/assets/98771b2c-3931-48da-b97b-961da58072dd)

 
ls file1
## OUTPUT

echo $?
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot from 2025-03-08 20-50-30](https://github.com/user-attachments/assets/98bd76ca-0fe3-429e-bc64-bb8d9029d073)

 
abcd
 
echo $?
 ## OUTPUT

![Screenshot from 2025-03-08 20-49-15](https://github.com/user-attachments/assets/0fe2cdbb-b7db-4df1-ae94-916951abf1aa)

 ![Screenshot from 2025-03-08 20-49-25](https://github.com/user-attachments/assets/865ec280-4565-4094-a189-3864352d1453)

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

![Screenshot from 2025-03-08 20-49-32](https://github.com/user-attachments/assets/a6f6ea8a-26d2-4fac-a8c2-c5e5be8adbd6)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2025-03-08 20-49-47](https://github.com/user-attachments/assets/c5e52392-0b55-4993-b4d0-c9f4584c393b)


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
![Screenshot from 2025-03-08 20-50-00](https://github.com/user-attachments/assets/3208c26b-50f3-45cd-ae20-31e9a3e7a92d)


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

![Screenshot from 2025-03-08 20-42-56](https://github.com/user-attachments/assets/31dd1db2-3dfd-4494-a731-24acc5f6e320)


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
![Screenshot from 2025-03-08 20-47-33](https://github.com/user-attachments/assets/6f846e90-17ae-4f11-9613-611bca4a5ade)


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
![Screenshot from 2025-03-08 20-39-58](https://github.com/user-attachments/assets/7eb268fd-3429-4431-b3b4-abaede451b24)


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
![Screenshot from 2025-03-08 20-40-14](https://github.com/user-attachments/assets/117eb802-9306-49b9-a6ab-1837710e63cd)

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
![Screenshot from 2025-03-08 20-39-18](https://github.com/user-attachments/assets/f161d0da-1fa6-4bc1-8c5f-301fa12df165)

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
![Screenshot from 2025-03-08 20-38-19](https://github.com/user-attachments/assets/cdddaeef-5b21-4eb5-888c-8f4c4a3cdaa2)


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
![Screenshot from 2025-03-08 20-38-35](https://github.com/user-attachments/assets/be962b41-9a86-4d20-b58d-1fc282e1e076)

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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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

 ![Screenshot from 2025-03-08 20-31-12](https://github.com/user-attachments/assets/8915a162-e075-4e9d-b4f2-4573100f3560)

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
$ ./argshift.sh 1 2 3
 ![Screenshot from 2025-03-08 20-28-46](https://github.com/user-attachments/assets/900992dd-350d-449b-b5b5-8798659d499c)

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
$ ./argshift.sh 1 2 3
 ![Screenshot from 2025-03-08 20-28-46](https://github.com/user-attachments/assets/9431c435-3591-4bbb-abdd-35d2b4fb0e4b)

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
 ![Screenshot from 2025-03-08 20-29-02](https://github.com/user-attachments/assets/58ba5b0c-27ec-4607-ae8c-448602bb85c3)

 
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
 ![Screenshot from 2025-03-08 20-27-38](https://github.com/user-attachments/assets/70463bfa-9595-4297-abe9-e7416b027afe)

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
![image](https://github.com/user-attachments/assets/b4666fee-0420-43c7-8bc2-d5871ce904cf)


# RESULT:
The Commands are executed successfully.
