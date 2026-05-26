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

<img width="605" height="150" alt="image" src="https://github.com/user-attachments/assets/fe340ddc-4ccf-465d-9832-951a04c2c5ed" />


cat < file2
## OUTPUT

<img width="610" height="176" alt="image" src="https://github.com/user-attachments/assets/910f4466-e094-44f5-b5ef-e5419ebb9312" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="607" height="77" alt="image" src="https://github.com/user-attachments/assets/28d505b9-2ea3-40aa-b432-f84c0ca7e2a7" />

 
comm file1 file2
 ## OUTPUT

<img width="661" height="228" alt="image" src="https://github.com/user-attachments/assets/39aaef28-d77f-4757-b568-b727ff8852ea" />

 
diff file1 file2
## OUTPUT

<img width="619" height="270" alt="image" src="https://github.com/user-attachments/assets/c1e7d0f9-6ca9-4f95-a6ab-d094221cb3b6" />


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

<img width="608" height="97" alt="image" src="https://github.com/user-attachments/assets/da28f347-1c9a-4d83-bd3a-de2708f43403" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="648" height="124" alt="image" src="https://github.com/user-attachments/assets/4a692076-7348-49dc-ba37-41bc1874804b" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="621" height="124" alt="image" src="https://github.com/user-attachments/assets/965590ae-aa2f-484a-b493-a87a19a88ace" />


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

<img width="598" height="80" alt="image" src="https://github.com/user-attachments/assets/5f099c85-7392-4991-800b-e3ef22db27c1" />


grep hello newfile 
## OUTPUT

<img width="603" height="76" alt="image" src="https://github.com/user-attachments/assets/16777010-0782-48a2-a02f-cd44d9a30a47" />



grep -v hello newfile 
## OUTPUT

<img width="605" height="77" alt="image" src="https://github.com/user-attachments/assets/c3fe9e83-2b60-4485-923d-d5913eceef37" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="610" height="103" alt="image" src="https://github.com/user-attachments/assets/533f1079-ea8b-416d-8157-fb953984b674" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="611" height="75" alt="image" src="https://github.com/user-attachments/assets/1fd9a05c-6c88-4d99-a3fe-d886fd48b07d" />



grep -R ubuntu /etc
## OUTPUT

<img width="1271" height="348" alt="image" src="https://github.com/user-attachments/assets/1eb38eae-22da-4713-8982-6a82557ae4a9" />


grep -w -n world newfile   
## OUTPUT

<img width="601" height="101" alt="image" src="https://github.com/user-attachments/assets/9afff136-58ff-4c97-a51d-21ff918bcc03" />


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

<img width="601" height="104" alt="image" src="https://github.com/user-attachments/assets/878973b4-64fa-42bb-97b2-411a28a0ac37" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="610" height="100" alt="image" src="https://github.com/user-attachments/assets/62dd7e2f-ea18-48aa-9e8e-51b5cc36296b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="600" height="99" alt="image" src="https://github.com/user-attachments/assets/a6f5a363-de19-41b3-8dcb-3d23cfebaf23" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="602" height="79" alt="image" src="https://github.com/user-attachments/assets/09b65be0-a0cd-4409-ad70-d7e0fc03e682" />


egrep '(world$)' newfile 
## OUTPUT

<img width="614" height="93" alt="image" src="https://github.com/user-attachments/assets/5d4d400d-daf0-47c8-b148-a52e34f4a30e" />


egrep '(World$)' newfile 
## OUTPUT

<img width="598" height="74" alt="image" src="https://github.com/user-attachments/assets/d871b79b-a25f-4ec9-8a24-6a3b463e27df" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="601" height="147" alt="image" src="https://github.com/user-attachments/assets/786dae52-f21a-4376-adcd-401602eaa8da" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="602" height="76" alt="image" src="https://github.com/user-attachments/assets/afa826fd-32b5-4305-bfce-646c4a4bc8a6" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="605" height="73" alt="image" src="https://github.com/user-attachments/assets/b6051fa4-9a68-41bb-b16c-9e36e6cc63c9" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="611" height="75" alt="image" src="https://github.com/user-attachments/assets/310a5921-3ad5-4021-8014-99dceed62c58" />


egrep l{2} newfile
## OUTPUT

<img width="605" height="97" alt="image" src="https://github.com/user-attachments/assets/168771ca-1e48-42ea-9272-ebb7263f7936" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="634" height="121" alt="image" src="https://github.com/user-attachments/assets/4c579a96-5f80-40b1-b815-eb096831909f" />


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

<img width="896" height="107" alt="image" src="https://github.com/user-attachments/assets/c225b89d-5ea2-47f3-8696-7609ec9130aa" />



sed -n -e '$p' file23
## OUTPUT

<img width="890" height="103" alt="image" src="https://github.com/user-attachments/assets/34fc091c-d8bd-4e21-b92b-fa04c69e9552" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="904" height="346" alt="image" src="https://github.com/user-attachments/assets/820c31cd-0434-4573-a910-4133c6bcec62" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="950" height="344" alt="image" src="https://github.com/user-attachments/assets/9a0a3acf-8de3-4bd5-a576-7995e3b376d2" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="905" height="343" alt="image" src="https://github.com/user-attachments/assets/c2177b8b-9db6-4d64-bb0b-2aa0be78fdf3" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="909" height="239" alt="image" src="https://github.com/user-attachments/assets/eee3cd99-8983-44ad-a650-61b5ed8c3459" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="952" height="179" alt="image" src="https://github.com/user-attachments/assets/6b146a1d-9a6d-46b9-87e5-bf53ab3c1613" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="904" height="140" alt="image" src="https://github.com/user-attachments/assets/9538bec3-f079-4f82-a35e-cfe3b1397d59" />


seq 10 
## OUTPUT

<img width="933" height="421" alt="image" src="https://github.com/user-attachments/assets/e60733f9-d542-412f-9e40-e74658b20859" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="905" height="178" alt="image" src="https://github.com/user-attachments/assets/95ef929d-a8df-422f-af5e-ec12ca01278d" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="891" height="165" alt="image" src="https://github.com/user-attachments/assets/d5009514-928e-4512-bae1-f6f2f9464fa8" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="923" height="195" alt="image" src="https://github.com/user-attachments/assets/99df6b0d-816e-4fe2-8169-4ae7c70344e1" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="939" height="178" alt="image" src="https://github.com/user-attachments/assets/5a8242b2-b7cf-4820-bd6c-fb8267bbcc5f" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="949" height="172" alt="image" src="https://github.com/user-attachments/assets/a2b4d690-d385-4abf-a0d9-e8ad96f1f0d6" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="923" height="172" alt="image" src="https://github.com/user-attachments/assets/d8a0cf29-bc9e-4457-ba47-da0b07b98230" />



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
<img width="907" height="242" alt="image" src="https://github.com/user-attachments/assets/839a564a-4713-46f6-b1b8-3ffd2892036c" />


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

<img width="904" height="242" alt="image" src="https://github.com/user-attachments/assets/cb67846a-ab5c-4bdd-9dd2-134336823567" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="936" height="351" alt="image" src="https://github.com/user-attachments/assets/8a0342e3-6daa-43e3-b59c-2ac7c40fbbb9" />

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

<img width="920" height="175" alt="image" src="https://github.com/user-attachments/assets/b5609b9e-bc9d-4be0-a45a-14c8bdeab1d1" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="915" height="174" alt="image" src="https://github.com/user-attachments/assets/81cc11b2-f3f3-4d65-864f-861937dd78a3" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="938" height="670" alt="image" src="https://github.com/user-attachments/assets/7e2fdb3e-dba9-4fc5-b43b-395988e97092" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="1085" height="631" alt="image" src="https://github.com/user-attachments/assets/bb2aac4d-67a4-40b0-ba5d-cfedc04d95c7" />


tar -xvf backup.tar
## OUTPUT

<img width="1098" height="746" alt="image" src="https://github.com/user-attachments/assets/e00c26d3-2aa8-472a-b876-70b7599ed39e" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="1051" height="105" alt="image" src="https://github.com/user-attachments/assets/df217bbb-3c40-41cc-8ecb-8625592816cb" />

gunzip backup.tar.gz
## OUTPUT

<img width="1050" height="68" alt="image" src="https://github.com/user-attachments/assets/f511f562-d95c-4e9e-967b-b9e3144a776a" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="785" height="154" alt="image" src="https://github.com/user-attachments/assets/e57ddf53-a76e-4fde-a775-7e9d8d012bfb" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="802" height="144" alt="image" src="https://github.com/user-attachments/assets/706bc71a-6d3d-48b1-8855-43104f51f3e0" />


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

<img width="906" height="541" alt="image" src="https://github.com/user-attachments/assets/73b6a92a-5c76-44a1-879f-b3349456f6ab" />

 
ls file1
## OUTPUT

<img width="808" height="82" alt="image" src="https://github.com/user-attachments/assets/e0d846c4-2206-4238-94f7-1696c909159f" />

echo $?
## OUTPUT 

<img width="772" height="89" alt="image" src="https://github.com/user-attachments/assets/d9b67d53-a921-40fd-96ee-deb938f4e040" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="855" height="175" alt="image" src="https://github.com/user-attachments/assets/bcbcb672-7fd5-4991-9ab6-c4a6f77194c0" />

 
abcd
 
echo $?
 ## OUTPUT

<img width="836" height="176" alt="image" src="https://github.com/user-attachments/assets/668bd5e0-70a6-4b42-8969-f2f009aa4c41" />

 
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
## OUTPUT

<img width="803" height="329" alt="image" src="https://github.com/user-attachments/assets/b5772363-e7d0-44f2-87eb-31cb81120d40" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="788" height="120" alt="image" src="https://github.com/user-attachments/assets/78fe7ad4-3c00-4242-88c2-2f898ea9a6ff" />


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

<img width="781" height="87" alt="image" src="https://github.com/user-attachments/assets/0fb305fb-3eda-47d0-9aa2-4cb66dea15e8" />

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

<img width="788" height="91" alt="image" src="https://github.com/user-attachments/assets/2b7907b2-59ec-45c5-a08f-9e2a05cafb5d" />


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
## OUTPUT

<img width="875" height="150" alt="image" src="https://github.com/user-attachments/assets/56b093c3-6827-4486-90ce-9df1dcabc285" />

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
## OUTPUT

<img width="837" height="187" alt="image" src="https://github.com/user-attachments/assets/e2689392-33c6-4521-b895-0739b8284034" />

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

<img width="840" height="120" alt="image" src="https://github.com/user-attachments/assets/88d47cbf-78ff-48b9-8c28-8ad2c6a29796" />


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

<img width="830" height="122" alt="image" src="https://github.com/user-attachments/assets/1df22185-64db-4097-9309-f1b1d6787370" />

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
## OUTPUT

<img width="792" height="95" alt="image" src="https://github.com/user-attachments/assets/5f12b77f-95e1-4634-90a6-b9d6e4839b81" />

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
## OUTPUT

<img width="826" height="357" alt="image" src="https://github.com/user-attachments/assets/93b552af-f0fd-424b-ade3-5f5c4b3184f9" />

 
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

##OUTPUT

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

<img width="1046" height="306" alt="image" src="https://github.com/user-attachments/assets/4741a418-bf98-4edb-a273-b0a54456b24c" />


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

<img width="812" height="208" alt="image" src="https://github.com/user-attachments/assets/8682b817-776d-46ec-948c-b7782462624a" />

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

<img width="787" height="94" alt="image" src="https://github.com/user-attachments/assets/37c6f33e-e9ca-4527-a6ab-3029cc93ad14" />

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

<img width="800" height="419" alt="image" src="https://github.com/user-attachments/assets/5e1a984e-2b33-4378-81f4-302a9a7e0141" />

 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT

<img width="915" height="150" alt="image" src="https://github.com/user-attachments/assets/9b76132f-6a34-42fb-a991-ebab0d0880d2" />
 
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

 <img width="965" height="205" alt="image" src="https://github.com/user-attachments/assets/dce78bfe-5049-4319-b222-0f7a6ef16e1e" />

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

<img width="805" height="126" alt="image" src="https://github.com/user-attachments/assets/d1f0362a-c701-4205-8428-acbd48e55760" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh $ ./exread1.sh 

## OUTPUT

<img width="902" height="123" alt="image" src="https://github.com/user-attachments/assets/74c6794a-ae89-4d09-b14c-07e442a056aa" />



 
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
./funcex.sh ./funcex.sh 1 2
## OUTPUT
 
<img width="833" height="179" alt="image" src="https://github.com/user-attachments/assets/b684070f-cb45-4f87-b8e0-1dd7235993a0" />

 
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
<img width="832" height="156" alt="image" src="https://github.com/user-attachments/assets/7338cdb8-429f-4f09-a250-f2db5862206b" />

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
<img width="807" height="145" alt="image" src="https://github.com/user-attachments/assets/63a33514-7582-49c9-abb6-df66a81632f2" />

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

<img width="832" height="472" alt="image" src="https://github.com/user-attachments/assets/bb263518-4314-46f0-885c-6cb4c687dbfc" />
 
 
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

<img width="788" height="449" alt="image" src="https://github.com/user-attachments/assets/d700027a-6f43-4d29-a813-37c87f054e4f" />

 
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

<img width="1042" height="719" alt="image" src="https://github.com/user-attachments/assets/58b6c508-899b-4f8e-881a-61c11d139cbc" />


# RESULT:
The Commands are executed successfully.
