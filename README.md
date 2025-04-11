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
![Screenshot from 2025-02-25 14-41-37](https://github.com/user-attachments/assets/cff67ef4-87ca-4231-876b-fa56d128602c)


cat < file2
## OUTPUT
![Screenshot from 2025-02-25 14-43-46](https://github.com/user-attachments/assets/bba92c11-80a6-4506-b131-819dc3174a22)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-02-25 14-46-47](https://github.com/user-attachments/assets/3ed5b789-cb66-47c8-acd9-0a419f37802b)


comm file1 file2
 ## OUTPUT

 ![Screenshot from 2025-02-25 14-48-01](https://github.com/user-attachments/assets/88de9378-36a9-41c4-b260-a1eab15e0579)


diff file1 file2
## OUTPUT
![Screenshot from 2025-02-25 14-48-54](https://github.com/user-attachments/assets/d9688e26-0be8-4341-a7bf-3ffd154fface)


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

![Screenshot from 2025-03-04 14-05-02](https://github.com/user-attachments/assets/7960489e-20e1-42f1-ac6b-93746e786a5f)





cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-03-04 14-10-14](https://github.com/user-attachments/assets/9f35ff0a-6284-4e50-adc2-ed6daef7b434)



cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-03-04 14-12-37](https://github.com/user-attachments/assets/5ceb233a-d42a-4c62-ad0b-b92e0996066f)


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

![Screenshot from 2025-03-04 14-16-49](https://github.com/user-attachments/assets/36bcd86b-ef3a-4e6a-93aa-4861e90ac7f1)



grep hello newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-17-35](https://github.com/user-attachments/assets/edc80598-3218-49b2-8568-6807d80e4b5a)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-18-15](https://github.com/user-attachments/assets/1299836a-e76e-4c90-ad49-f4d1b5120412)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2025-03-04 14-19-12](https://github.com/user-attachments/assets/a0969d49-4791-40db-afff-dee602d34f8e)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-03-04 14-20-39](https://github.com/user-attachments/assets/4e977528-87ac-4142-9a90-81b938cf0811)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-03-04 14-28-22](https://github.com/user-attachments/assets/030f3a8b-1ace-47ec-95b5-3cff846aa382)




grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-03-04 14-30-03](https://github.com/user-attachments/assets/cc428127-f562-4428-aee9-2cedfb0fc597)



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
```
 
egrep -w 'Hello|hello' newfile 
## OUTPUT

![Screenshot from 2025-03-04 14-33-01](https://github.com/user-attachments/assets/0c6cc42f-59e0-4295-8a16-adebe5548672)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-03-04 14-34-15](https://github.com/user-attachments/assets/22d4d6b5-897a-423b-a0d1-c466cc4eedc6)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-03-04 14-35-35](https://github.com/user-attachments/assets/94219992-fbd9-44b3-b6b0-e67666b27e52)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-03-04 14-36-21](https://github.com/user-attachments/assets/65c00338-b9a7-4186-8e16-347e108f02d0)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-03-04 14-37-26](https://github.com/user-attachments/assets/0b403a18-3d9b-4bce-a5a9-cf5aff85c83d)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-38-44](https://github.com/user-attachments/assets/8c9b8108-e897-47c1-a9d2-84681285ced7)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-39-19](https://github.com/user-attachments/assets/9779d598-ea81-41b1-a0e2-eb4c7d6873bf)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-39-56](https://github.com/user-attachments/assets/2a85de2c-c5c0-4962-90a5-89e32bd30053)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-40-53](https://github.com/user-attachments/assets/b419d6db-14df-494b-b61e-ff9bced71e67)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-03-04 14-41-26](https://github.com/user-attachments/assets/1e028ff6-99f4-4924-979b-04225e0e1ef3)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-03-04 14-42-12](https://github.com/user-attachments/assets/bad42d1e-442f-4825-bda5-785ab31622bb)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-03-04 14-42-50](https://github.com/user-attachments/assets/ad366b9a-7836-4a36-84c9-d67a4ea86e8e)


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
![Screenshot from 2025-03-04 14-44-35](https://github.com/user-attachments/assets/df17cddd-949f-43bc-875e-37b42d6757f7)



sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-03-08 11-16-44](https://github.com/user-attachments/assets/f27c4429-400c-4b24-9a58-82045eb7acd7)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 11-18-06](https://github.com/user-attachments/assets/56d73c60-7d20-4d09-96ac-ddeb677b61a7)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-03-08 11-18-45](https://github.com/user-attachments/assets/186fc8d2-a534-4d4f-97bc-2a33b1c0c092)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-03-08 11-19-25](https://github.com/user-attachments/assets/23a43c52-e619-44a9-9a18-c877a267d70b)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-03-08 11-20-04](https://github.com/user-attachments/assets/9f8c22e5-55a5-4bfd-affb-358576526c5e)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-08 11-20-35](https://github.com/user-attachments/assets/3a07c7b8-c21b-4b06-b3d2-3b6da0145c5b)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-03-08 11-21-14](https://github.com/user-attachments/assets/dface34d-ee29-4582-864c-f81c8e23618e)



seq 10 
## OUTPUT

![Screenshot from 2025-03-08 11-22-08](https://github.com/user-attachments/assets/522eaebe-9ad3-4025-baa5-6fac6dd366be)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-03-08 11-23-19](https://github.com/user-attachments/assets/682789e0-82e9-432a-824c-abd501ca0278)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot from 2025-03-08 11-23-55](https://github.com/user-attachments/assets/81759447-63c2-44d8-a538-7a1bf7f3ba0f)


seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-03-08 11-24-26](https://github.com/user-attachments/assets/f1c11784-cd4b-40b6-98dc-4571d191b0c0)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-03-08 11-24-58](https://github.com/user-attachments/assets/c5e46558-cd43-45fa-8f6e-f31fd8ca6cad)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-03-08 11-27-01](https://github.com/user-attachments/assets/affc1d68-2e7a-4fc4-94e4-244061bce332)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-03-08 11-28-17](https://github.com/user-attachments/assets/57ceff2d-8239-4383-b6fc-046fd64453df)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-03-08 11-28-46](https://github.com/user-attachments/assets/7692f334-948e-4394-acff-747ca53fa11b)

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

![Screenshot from 2025-04-12 03-40-53](https://github.com/user-attachments/assets/23aff33b-d9d1-4124-8d08-af543c67bf6c)


cat > file22

1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev

uniq file22
## OUTPUT

![Screenshot from 2025-04-12 03-43-06](https://github.com/user-attachments/assets/8ccc3fab-9f3b-4f01-a757-2e07578d5d54)


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
