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

<img width="565" height="89" alt="image" src="https://github.com/user-attachments/assets/aa86af6a-3cf3-456c-8eb9-a06fc756df3e" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="404" height="118" alt="image" src="https://github.com/user-attachments/assets/27991c89-b076-4104-a3d3-8fa3955cea82" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="444" height="118" alt="image" src="https://github.com/user-attachments/assets/c1c7fd92-4a74-4632-b338-fd608aef0d22" />


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


<img width="441" height="72" alt="image" src="https://github.com/user-attachments/assets/3fc28c31-5795-49fb-bb54-0069295f860a" />

grep hello newfile 
## OUTPUT

<img width="441" height="72" alt="image" src="https://github.com/user-attachments/assets/3fc28c31-5795-49fb-bb54-0069295f860a" />

grep -v hello newfile 
## OUTPUT
<img width="574" height="138" alt="image" src="https://github.com/user-attachments/assets/49f2b88e-c2ed-46d3-b462-b6f96b2660dd" />



cat newfile | grep -i "hello"
## OUTPUT




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
cat < newfile 
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




## OUTPUT


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
cat > file23
```


sed -n -e '3p' file23
## OUTPUT

<img width="393" height="87" alt="image" src="https://github.com/user-attachments/assets/b9462bde-8189-4b4e-95c4-098a0a76b020" />


sed -n -e '$p' file23
## OUTPUT

<img width="413" height="46" alt="image" src="https://github.com/user-attachments/assets/b1d08d73-b717-4eb8-8299-98a3df44a97b" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="413" height="46" alt="image" src="https://github.com/user-attachments/assets/60c874b6-6b9d-4453-9748-f45b63ec28e0" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="413" height="46" alt="image" src="https://github.com/user-attachments/assets/346f3c05-abd6-4ae5-ab6c-89d134885e09" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="474" height="46" alt="image" src="https://github.com/user-attachments/assets/420a8e57-9df2-4b13-9185-4cd956991f1a" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="474" height="46" alt="image" src="https://github.com/user-attachments/assets/bc0cacb1-4b54-41af-af57-ce254416d624" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="498" height="84" alt="image" src="https://github.com/user-attachments/assets/52fd475c-fd52-45eb-acc3-5cfc4fbed377" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="498" height="84" alt="image" src="https://github.com/user-attachments/assets/bfad175b-2d4a-4d0f-bd6a-4a0cb7502d8b" />



seq 10
## OUTPUT

<img width="483" height="246" alt="image" src="https://github.com/user-attachments/assets/09370f30-4dc2-44f9-ac99-ed4b2e1dc312" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="481" height="92" alt="image" src="https://github.com/user-attachments/assets/4ebb2f3e-332f-4cc2-a4a7-0d8f805060b1" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="481" height="92" alt="image" src="https://github.com/user-attachments/assets/b6d8c0a6-0579-4b73-9550-095df9f7c484" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="485" height="114" alt="image" src="https://github.com/user-attachments/assets/b34382d9-8782-4ba0-a398-1febc5b01daa" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="486" height="88" alt="image" src="https://github.com/user-attachments/assets/22b8f166-9168-4f68-8138-abbf9a459664" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="486" height="88" alt="image" src="https://github.com/user-attachments/assets/60f1a3b1-3fb0-4493-bd7f-dcb324938474" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="486" height="88" alt="image" src="https://github.com/user-attachments/assets/0fe8278e-8c16-4eb1-8242-45d6fb66270a" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="486" height="88" alt="image" src="https://github.com/user-attachments/assets/cb5fa33a-81ae-43e8-ad60-1d12eda07463" />


#Sorting File content
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT

<img width="530" height="163" alt="image" src="https://github.com/user-attachments/assets/6b4a3757-c5c1-4af1-98cf-0f42856916fc" />


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

<img width="338" height="151" alt="image" src="https://github.com/user-attachments/assets/bc86600d-1536-45c7-b1d1-a12ac832cb60" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="539" height="86" alt="image" src="https://github.com/user-attachments/assets/b40ec047-feff-492f-a908-2e49beee4ae9" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
 ## OUTPUT

<img width="381" height="117" alt="image" src="https://github.com/user-attachments/assets/49696d30-5651-4a14-8557-0b7e04c4b8dc" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="530" height="187" alt="image" src="https://github.com/user-attachments/assets/d9e8be93-792d-46f8-9732-f7863771482b" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="681" height="983" alt="image" src="https://github.com/user-attachments/assets/c6fc0745-4f54-47be-b139-c2fd495c0459" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


# RESULT:
The Commands are executed successfully.
