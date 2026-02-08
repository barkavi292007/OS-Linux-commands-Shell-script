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
<img width="258" height="141" alt="image" src="https://github.com/user-attachments/assets/31d41e21-5662-47e2-a424-790efd5992fe" />



cat < file2
## OUTPUT
<img width="442" height="165" alt="image" src="https://github.com/user-attachments/assets/a13c8b06-df1b-42e9-aa4f-40e043cc43d8" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="494" height="329" alt="image" src="https://github.com/user-attachments/assets/ffef0999-808c-4a98-b025-0e044d33346e" />

comm file1 file2
 ## OUTPUT
<img width="480" height="284" alt="image" src="https://github.com/user-attachments/assets/1be04a3d-c4f9-4ec9-98e3-8eb372920139" />

 
diff file1 file2
## OUTPUT
<img width="453" height="228" alt="image" src="https://github.com/user-attachments/assets/3b078cc4-8290-4302-8e12-62c70a362557" />


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

<img width="370" height="128" alt="image" src="https://github.com/user-attachments/assets/63ed9569-179c-4f5a-9df7-68f3c6c81211" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="370" height="128" alt="image" src="https://github.com/user-attachments/assets/ee1046b2-0967-4838-9afd-d849f6bb5c8b" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="370" height="128" alt="image" src="https://github.com/user-attachments/assets/88f76599-6d8c-490f-932e-736c52da93ed" />

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
<img width="349" height="73" alt="image" src="https://github.com/user-attachments/assets/8092ecec-b179-492b-85b5-eca0ceda1ef3" />

grep -v hello newfile 
## OUTPUT

<img width="574" height="138" alt="image" src="https://github.com/user-attachments/assets/49f2b88e-c2ed-46d3-b462-b6f96b2660dd" />

cat newfile | grep -i "hello"
## OUTPUT

<img width="438" height="70" alt="image" src="https://github.com/user-attachments/assets/09bd35d5-d1ef-4e54-973e-f03ca4dab19a" />

cat newfile | grep -i -c "hello"
## OUTPUT

<img width="568" height="85" alt="image" src="https://github.com/user-attachments/assets/e3c8fb82-2e36-4ec8-b9a9-f9f970b9b453" />

grep -R ubuntu /etc
## OUTPUT

<img width="894" height="463" alt="image" src="https://github.com/user-attachments/assets/9fcbd984-b55a-4f79-9e42-eb3abe803521" />


grep -w -n world newfile   
## OUTPUT
<img width="429" height="54" alt="image" src="https://github.com/user-attachments/assets/9edd9d41-464e-4aab-87cb-905a50505567" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUTp 

<img width="500" height="81" alt="image" src="https://github.com/user-attachments/assets/ad43ec89-9a2c-4275-8fa3-94daa2327227" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="500" height="81" alt="image" src="https://github.com/user-attachments/assets/eb94992c-931f-4e17-b6b1-dd7b04e857ae" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="500" height="81" alt="image" src="https://github.com/user-attachments/assets/1bfeab90-fe15-43c3-9df3-21cc60cd1446" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="506" height="57" alt="image" src="https://github.com/user-attachments/assets/ba2df5dc-5177-4844-98f4-547600080c1e" />


egrep '(world$)' newfile 
## OUTPUT

<img width="450" height="72" alt="image" src="https://github.com/user-attachments/assets/3666729c-a1fe-490c-816d-179bea61a3d6" />


egrep '(World$)' newfile 
## OUTPUT
<img width="454" height="50" alt="image" src="https://github.com/user-attachments/assets/280a1512-581f-4c1f-aa15-00a794d9c07d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="466" height="92" alt="image" src="https://github.com/user-attachments/assets/4f272758-92e6-4cdc-96be-e33c34cf342b" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="466" height="52" alt="image" src="https://github.com/user-attachments/assets/1316e8f8-8f95-423d-bcd8-d31d58231484" />


egrep 'Linux.*World' newfile 

## OUTPUT
<img width="466" height="52" alt="image" src="https://github.com/user-attachments/assets/640da16b-44ef-4192-9bbe-089e8f000018" />


egrep l{2} newfile
## OUTPUT
<img width="377" height="61" alt="image" src="https://github.com/user-attachments/assets/7e9312c8-bafb-43c1-ac79-828d8fac79a1" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="393" height="87" alt="image" src="https://github.com/user-attachments/assets/57293d43-5ce6-4c7b-ae50-e8ed0d38eae1" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom | 5000  | Admin
1003 | Joe | 7000  | Develope
1005 | Sam | 5000  | HR
1004 | Sit | 7000  | Dev
1003 | Joe | 7000  | Develope
1001 | Ram | 10000 | HR
^d
```
sed -n -e '3p' file23

## OUTPUT
<img width="361" height="78" alt="image" src="https://github.com/user-attachments/assets/34772824-51c0-4955-846f-91847af6e682" />

sed -n -e '$p' file23

## OUTPUT

<img width="360" height="62" alt="image" src="https://github.com/user-attachments/assets/0680a347-74db-4366-a924-8d0a93e392a1" />


sed  -e 's/Ram/Sita/' file23

## OUTPUT

<img width="449" height="269" alt="image" src="https://github.com/user-attachments/assets/606a3dde-17de-458e-8d61-6821cb2adb63" />


sed  -e '2s/Ram/Sita/' file23

## OUTPUT

<img width="449" height="269" alt="image" src="https://github.com/user-attachments/assets/3a71078b-af1d-4582-ac3e-b35e720108ae" />


sed  '/tom/s/5000/6000/' file23

## OUTPUT

<img width="449" height="269" alt="image" src="https://github.com/user-attachments/assets/e60ebc53-d8f1-43d1-8b28-56bcd69049cd" />


sed -n -e '1,5p' file23

## OUTPUT

<img width="397" height="171" alt="image" src="https://github.com/user-attachments/assets/2a13310d-6d5a-4287-967d-1d8778270f53" />


sed -n -e '2,/Joe/p' file23

## OUTPUT

<img width="445" height="125" alt="image" src="https://github.com/user-attachments/assets/e7b7a333-a95b-4bda-9f6f-e55f584063eb" />



sed -n -e '/tom/,/Joe/p' file23

## OUTPUT

<img width="467" height="76" alt="image" src="https://github.com/user-attachments/assets/2cc77bc6-5d83-4469-822b-f9e70a66fc97" />


seq 10

## OUTPUT

<img width="265" height="253" alt="image" src="https://github.com/user-attachments/assets/74d832ae-8425-428c-884f-9a19c4c41bd7" />

seq 10 | sed -n '4,6p'

## OUTPUT

<img width="413" height="91" alt="image" src="https://github.com/user-attachments/assets/8e37f4e5-37de-486c-9d68-f5731dc5dc51" />


seq 10 | sed -n '2,~4p'

## OUTPUT

<img width="413" height="91" alt="image" src="https://github.com/user-attachments/assets/9127b407-60de-454c-ab18-2a8b6c820ce1" />

seq 3 | sed '2a hello'

## OUTPUT

<img width="417" height="116" alt="image" src="https://github.com/user-attachments/assets/7725c300-8956-400f-a279-71c0d6af169c" />


seq 2 | sed '2i hello'

## OUTPUT

<img width="428" height="95" alt="image" src="https://github.com/user-attachments/assets/b690fbc5-5073-49e1-baea-2a51669bc074" />


seq 10 | sed '2,9c hello'

## OUTPUT

<img width="428" height="95" alt="image" src="https://github.com/user-attachments/assets/d983d017-eb97-41a3-a05d-2db3ee1dd220" />

sed -n '2,4{s/^/$/;p}' file23

## OUTPUT

<img width="446" height="92" alt="image" src="https://github.com/user-attachments/assets/ab9528fb-bbf2-4423-9ef4-acc465c66b99" />


sed -n '2,4{s/$/*/;p}' file23

#Sorting File content cat > file21

1001 | Ram | 10000 | HR
1002 | tom | 5000  | Admin
1003 | joe | 7000  | develope
1005 | Sam | 5000  | HR
1004 | Sit | 7000  | Dev

sort file21

## OUTPUT

<img width="451" height="107" alt="image" src="https://github.com/user-attachments/assets/86212c20-9924-47c9-b172-09d070af2136" />


cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="345" height="142" alt="image" src="https://github.com/user-attachments/assets/1f6d209e-d45c-407d-852f-cedcb851eed1" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]

 ## OUTPUT

<img width="499" height="271" alt="image" src="https://github.com/user-attachments/assets/37ca07e9-f15f-4efa-b566-243df81ae663" />


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
cat urllist.txt | tr-d''
 ## OUTPUT

<img width="605" height="91" alt="image" src="https://github.com/user-attachments/assets/65ab9c8a-5b05-4eca-a0e2-b52b6af968c1" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'

## OUTPUT

<img width="566" height="80" alt="image" src="https://github.com/user-attachments/assets/01fd4658-66c5-40e3-8c9d-879ac4210d3a" />


#Backup commands
tar -cvf backup.tar *

## OUTPUT

<img width="867" height="750" alt="image" src="https://github.com/user-attachments/assets/972e15a1-4469-455d-9a72-c52dfd578591" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar

## OUTPUT

<img width="1572" height="727" alt="image" src="https://github.com/user-attachments/assets/7b74996c-a305-4b0e-9d82-6f77d971d8a5" />


tar -xvf backup.tar

## OUTPUT

<img width="942" height="732" alt="image" src="https://github.com/user-attachments/assets/9d526d19-c499-4c2c-bc6f-b73794b75fa5" />


gzip backup.tar

ls .gz

## OUTPUT

<img width="484" height="102" alt="image" src="https://github.com/user-attachments/assets/d864d97e-fbce-46cf-9b31-7fc8d9b2f306" />

 
gunzip backup.tar.gz

## OUTPUT

 <img width="720" height="96" alt="image" src="https://github.com/user-attachments/assets/f064715a-266f-4902-9871-9b66ce1343c8" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="588" height="203" alt="image" src="https://github.com/user-attachments/assets/97b4cc6a-2e75-4c35-ac24-d9f5b59fa4aa" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="432" height="103" alt="image" src="https://github.com/user-attachments/assets/6d99831a-8fa8-416b-914b-bc85ee4b3f3a" />


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

<img width="541" height="662" alt="image" src="https://github.com/user-attachments/assets/920b2168-44d9-49a8-9abe-19333ef736e9" />

 
ls file1

## OUTPUT

<img width="404" height="58" alt="image" src="https://github.com/user-attachments/assets/e9b5e58c-6680-4826-ab82-5fdaa2075848" />

 
echo $?

## OUTPUT 

<img width="404" height="50" alt="image" src="https://github.com/user-attachments/assets/8b6a3d20-8ad7-4617-a167-ef70402eed00" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="619" height="109" alt="image" src="https://github.com/user-attachments/assets/efddec2a-f67b-40b9-989d-1a8b6ee92b39" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="476" height="261" alt="image" src="https://github.com/user-attachments/assets/81e2a194-5bc8-473a-b999-b38777e7c14a" />

 
# mis-using string comparisons

cat < strcomp.sh 
```
bash
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
```
bash
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

chmod 755 strcomp.sh
 
./strcomp.sh 

## OUTPUT

<img width="625" height="147" alt="image" src="https://github.com/user-attachments/assets/48ae9a23-8db3-47f9-9f30-8e1f20ea6d25" />


# check file ownership

cat passwdperm.sh
```
bash
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

<img width="627" height="196" alt="image" src="https://github.com/user-attachments/assets/6e960da0-5147-4496-bbdb-8ecdaf90011c" />


# check if with file location

cat>ifnested.sh 
```
bash
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

<img width="560" height="595" alt="image" src="https://github.com/user-attachments/assets/df1c271b-5d27-4853-a8cc-4baae56492ab" />


# using numeric test comparisons

cat > iftest.sh 
```
bash
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
```
bash
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

##Output

<img width="555" height="441" alt="image" src="https://github.com/user-attachments/assets/3a754689-1fbe-4f80-aca9-b65d524ea87e" />


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
```
bash
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

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

<img width="571" height="119" alt="image" src="https://github.com/user-attachments/assets/5ee70672-6337-4a69-b727-2aa8dcd23416" />


# looking for a possible value using elif

cat elifcheck.sh 
```
bash
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

<img width="571" height="119" alt="image" src="https://github.com/user-attachments/assets/1c7ba4a0-84b9-450a-9167-b180b602ddb1" />


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

<img width="571" height="316" alt="image" src="https://github.com/user-attachments/assets/0e64333d-647d-4536-860e-dfbd91115872" />



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

<img width="679" height="267" alt="image" src="https://github.com/user-attachments/assets/078e18de-cb2e-4a45-9526-ee95d4d31134" />


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

<img width="424" height="243" alt="image" src="https://github.com/user-attachments/assets/f1b13f71-eaee-4a11-ae16-5ddeca742a50" />

 
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

<img width="419" height="261" alt="image" src="https://github.com/user-attachments/assets/d70568dc-e6b5-44a2-8498-4ffc57826354" />


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

<img width="439" height="269" alt="image" src="https://github.com/user-attachments/assets/e2ce8b25-3125-452a-882b-d1aa0797a9f2" />

 
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

<img width="686" height="122" alt="image" src="https://github.com/user-attachments/assets/afcfb4cb-1c8e-4d15-948b-6a78b26be6ca" />



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="580" height="114" alt="image" src="https://github.com/user-attachments/assets/b4115c06-ae0a-45af-a4e9-78a4574e99e3" />


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
./funcex.sh 


## OUTPUT

<img width="579" height="294" alt="image" src="https://github.com/user-attachments/assets/cd8ecbac-a09e-4c79-80db-5872bd360b46" />


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

<img width="318" height="137" alt="image" src="https://github.com/user-attachments/assets/f1595213-ff73-44d3-a046-4ebc33559582" />


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

<img width="418" height="236" alt="image" src="https://github.com/user-attachments/assets/90047bcb-8acd-46af-890a-88308b91d4cc" />


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
./argshift.sh 1 2 3

## OUTPUT


<img width="457" height="244" alt="image" src="https://github.com/user-attachments/assets/5a3733aa-a3ce-4ab8-b774-15ae381661d5" />

 
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

<img width="473" height="660" alt="image" src="https://github.com/user-attachments/assets/3083f727-ea36-46ba-a8fb-5d2c5233dae0" />



 
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

<img width="527" height="559" alt="image" src="https://github.com/user-attachments/assets/ef4af3b0-e050-4c84-b5fc-86fd2dbae06f" />



# RESULT:
The Commands are executed successfully.
