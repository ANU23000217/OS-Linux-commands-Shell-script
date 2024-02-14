![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/bb0996f5-ce24-4e10-8183-95830a7e6fae)# OS-Linux-commands-Shell-scripting
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
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```


cat < file2
## OUTPUT
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```

# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/3d17b2b3-39c8-43a8-abdc-519c900acba8)

comm file1 file2
 ## OUTPUT
![Screenshot 2024-02-12 113955](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/9f15abc6-fa53-4ce6-9690-41d0c5527c64)

 
diff file1 file2
## OUTPUT
![Screenshot 2024-02-12 114122](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/6f0df5d6-6dc0-473f-8764-8f8788dc1423)


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
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/e74cc399-e869-4514-9294-e4d66bdbb553)




cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/45a81470-3b96-4c0b-9c34-21ef65d280c1)


cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/81235175-e464-4178-a1da-d78a36605b9b)


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

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/7d5dc360-1c3a-4ec4-9367-a9d3ebf3da9d)


grep hello newfile 
## OUTPUT


![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/3b622860-62e3-4eba-88ad-9644765927df)


grep -v hello newfile 
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/0a4e551a-c35b-4f53-a343-e0c41baeefdf)



cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/10be401c-081e-4138-af1f-88aa41158c77)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/a2eb2603-767e-486a-bb38-c9e1f53f51a3)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/cb370c18-be74-432d-9314-51f331acf7df)


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
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/2d621e3e-9f9a-44ac-a6db-043fdba5cc21)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/f2413676-3063-4310-9007-e31987305c59)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/7a74a2cf-5316-47fc-8448-8cae00930409)




egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/2097ab41-753f-4c27-bf30-f3c2b3edd826)


egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/d6105214-5e17-4bcf-82c9-256ac369f797)



egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/d3019e06-e463-45ab-bf66-985f54a7edb9)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/c0c28d29-8373-4c75-b10a-e3a1ee97271a)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/d525b4d0-ceaf-456e-b23e-98fc98180629)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/b3b81c41-51b4-406b-b712-21a2a4c9d97c)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/6bb38c3a-f787-4522-9190-8a797f9ec430)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/82fd9878-0b30-4a54-8ab5-18dd15381f65)


egrep 's{1,2}' newfile
## OUTPUT 
cat ![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/c92a0337-816f-4d2f-a34d-6748b3cb1bee)


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

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/a648b63d-4908-491b-83e2-15d2a6549860)


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/084144ca-9506-4676-8b2a-4ce86686c9e6)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/033e8dc7-f710-400f-9fa0-78d15ed14fce)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/b67f110e-2c70-4583-a1be-a37ad91ad49d)



sed -n -e '1,5p' file23
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/4539c59e-1967-4511-aa85-02e0193a1e13)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/30234a9f-dd11-4ae5-b7a5-9045148072a0)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/9a68ec8b-c637-4d4f-b099-279531805f0b)



seq 10 
## OUTPUT


![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/a6426c76-366f-4acd-9a74-05d4c22cd1ef)

seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/be70bf5e-1699-41fc-aa85-bdcde8e946ca)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/4dae8842-394b-4660-98d8-f1ff6de58121)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/98a1731b-3015-45f1-ba23-6cb031f09c8d)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/37f79adc-6b21-4499-bbfa-d74aeae1461a)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/9c4330d4-0447-451d-a81a-cf358636d16d)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/da40ce9b-3d87-4252-90db-988a1f344a81)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/3459be51-4d3f-4d3b-a8ad-e63a1fcadd62)


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
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/6ddff4be-6d23-46ab-9e48-2d436930fea3)



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

![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/0b50c2dc-0ef6-4965-92c6-5b0ff5735bd1)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/ANU23000217/OS-Linux-commands-Shell-script/assets/139117108/734761d9-86e9-4b02-9948-1a8de5e92c36)

 

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
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
