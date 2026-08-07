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

<img width="427" height="359" alt="image" src="https://github.com/user-attachments/assets/c01b59d4-0c28-4b09-8817-8000513191d5" />




cat < file2
## OUTPUT

<img width="336" height="404" alt="image" src="https://github.com/user-attachments/assets/16b64b18-c2f4-4e5b-bcc2-4d7fdcbcc9f4" />



# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="590" height="82" alt="Screenshot 2026-08-05 084821" src="https://github.com/user-attachments/assets/e7c70be8-a682-4302-93c1-41f370facf34" />

comm file1 file2
 ## OUTPUT
 
 <img width="768" height="229" alt="Screenshot 2026-08-05 084930" src="https://github.com/user-attachments/assets/bb1fb558-2ddd-4efe-a0a3-3ea766d1edeb" />

diff file1 file2
## OUTPUT
<img width="679" height="280" alt="image" src="https://github.com/user-attachments/assets/3032a4b4-67c9-45c3-b54b-cab95efdb26a" />

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

<img width="642" height="105" alt="image" src="https://github.com/user-attachments/assets/b2bf3a0d-f3b6-4ac0-8900-41779266016c" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="647" height="125" alt="image" src="https://github.com/user-attachments/assets/3898f7f9-545b-4427-bf12-b70e4721d349" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="648" height="127" alt="image" src="https://github.com/user-attachments/assets/f135499f-a046-42b3-9b15-528f1c400b65" />


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

<img width="632" height="76" alt="image" src="https://github.com/user-attachments/assets/e2ba3f96-8bb6-4037-bfcb-e4c8ce027182" />


grep hello newfile 
## OUTPUT

<img width="632" height="84" alt="image" src="https://github.com/user-attachments/assets/4493ea26-3310-416a-8081-665e1184d0b6" />



grep -v hello newfile 
## OUTPUT

<img width="660" height="78" alt="image" src="https://github.com/user-attachments/assets/5bfc554e-f0eb-417a-bc0e-9adcd7504702" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="465" height="97" alt="image" src="https://github.com/user-attachments/assets/9349aa12-df56-47b6-a900-76f1753d295b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="457" height="78" alt="image" src="https://github.com/user-attachments/assets/4479d528-2df7-4490-aa00-588645b45820" />



grep -R ubuntu /etc
## OUTPUT

<img width="1278" height="776" alt="image" src="https://github.com/user-attachments/assets/e3402911-f133-48bc-b044-a1eefa7e71b4" />


grep -w -n world newfile   
## OUTPUT
<img width="340" height="100" alt="image" src="https://github.com/user-attachments/assets/725ad428-01e0-4e53-8a44-c0df00bfeacd" />


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

<img width="447" height="111" alt="image" src="https://github.com/user-attachments/assets/e05b6dd2-25f9-4b25-98df-2560670c1a73" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="432" height="103" alt="image" src="https://github.com/user-attachments/assets/27468810-579c-4f9e-ab4f-889d88aac58d" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="424" height="109" alt="image" src="https://github.com/user-attachments/assets/3ee83d8b-1701-4849-a927-7482d371fef6" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="495" height="93" alt="image" src="https://github.com/user-attachments/assets/7b456f30-c28d-42c7-9721-30a5743d535c" />



egrep '(world$)' newfile 
## OUTPUT

<img width="415" height="111" alt="image" src="https://github.com/user-attachments/assets/c5674730-37d0-4860-b23d-96b95224bfa9" />


egrep '(World$)' newfile 
## OUTPUT
<img width="379" height="80" alt="image" src="https://github.com/user-attachments/assets/89b6e43e-167d-4318-9345-0f7ea74050b8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="538" height="124" alt="image" src="https://github.com/user-attachments/assets/64e6b20a-6fd4-4a71-afa1-e0689df04e41" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="356" height="80" alt="image" src="https://github.com/user-attachments/assets/57aa37b3-bf44-4e8c-beff-b9ce8e8a2e4a" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="398" height="75" alt="image" src="https://github.com/user-attachments/assets/16de99e6-20e3-4768-ba24-82ddc8730862" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="433" height="79" alt="image" src="https://github.com/user-attachments/assets/50196515-b15f-45bd-a2f0-a3c17d7132ad" />


egrep l{2} newfile
## OUTPUT
<img width="367" height="101" alt="image" src="https://github.com/user-attachments/assets/5b96c65e-215c-4b88-bee0-ed338696cdf5" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="391" height="131" alt="image" src="https://github.com/user-attachments/assets/f91fcc7c-244b-4223-ac4e-a085eb3b1f6f" />


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

<img width="406" height="86" alt="image" src="https://github.com/user-attachments/assets/43aecd22-f134-4b23-85fa-3eef4e5a041c" />


sed -n -e '$p' file23
## OUTPUT

<img width="278" height="87" alt="image" src="https://github.com/user-attachments/assets/35d1777a-bce8-4f01-94c2-93ec51ab77e6" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="485" height="249" alt="image" src="https://github.com/user-attachments/assets/e1b495ae-e500-4ce2-839b-1e92fc1e317c" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="459" height="252" alt="image" src="https://github.com/user-attachments/assets/54befc0e-009e-4ef4-8ecc-62bee26fca7d" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="483" height="258" alt="image" src="https://github.com/user-attachments/assets/ee164930-cfa3-48e4-b719-6dc22c1cd793" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="451" height="187" alt="image" src="https://github.com/user-attachments/assets/ebfea15f-969e-423b-b3ce-4ada33863bb0" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="413" height="131" alt="image" src="https://github.com/user-attachments/assets/412db410-9a75-4c82-8633-8dab2a29143b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="470" height="108" alt="image" src="https://github.com/user-attachments/assets/bba32973-31ba-4e99-a8df-1b7b52a3c17b" />


seq 10 
## OUTPUT

<img width="400" height="305" alt="image" src="https://github.com/user-attachments/assets/d7f89bc8-a3da-4d8d-a515-caa68e159b82" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="382" height="127" alt="image" src="https://github.com/user-attachments/assets/de324402-f63c-4811-a48f-010570e96a34" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="371" height="134" alt="image" src="https://github.com/user-attachments/assets/a58ecfad-7c22-441a-9046-6ce4b46b7a5e" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="384" height="151" alt="image" src="https://github.com/user-attachments/assets/1525b826-1c5e-4298-8280-49c7650b959d" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="499" height="132" alt="image" src="https://github.com/user-attachments/assets/f0a24cf2-c82b-4d6b-b8ef-b7edd02bd8a3" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="409" height="135" alt="image" src="https://github.com/user-attachments/assets/d5a2bb86-4ff0-4b7c-a752-d37857a2b41c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="470" height="130" alt="image" src="https://github.com/user-attachments/assets/c7fc0cb7-17b1-4e42-ba1f-10d722b5247f" />



sed -n '2,4{s/$/*/;p}' file23
<img width="502" height="129" alt="image" src="https://github.com/user-attachments/assets/33deefe6-4c63-4d42-9f79-7f0afbabdc2d" />


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

<img width="382" height="183" alt="image" src="https://github.com/user-attachments/assets/4d075c85-3d49-43ba-8c0d-0cb95e6c390f" />

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

<img width="383" height="181" alt="image" src="https://github.com/user-attachments/assets/59b3a684-9343-4d1b-85cf-8e89cea7d99a" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="466" height="257" alt="image" src="https://github.com/user-attachments/assets/6141034b-4614-408d-bae9-0a82ef502e91" />




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

<img width="379" height="121" alt="image" src="https://github.com/user-attachments/assets/074956dd-f04a-430f-b960-c90721a0368e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="479" height="125" alt="image" src="https://github.com/user-attachments/assets/d46b27a5-b395-4ccc-afc6-8f89137878fa" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="1167" height="748" alt="image" src="https://github.com/user-attachments/assets/0eea505d-7c61-4b52-82b9-f50af650586d" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1132" height="714" alt="image" src="https://github.com/user-attachments/assets/31259569-9d5a-485c-bdb4-95af07057c59" />


tar -xvf backup.tar
## OUTPUT
<img width="929" height="741" alt="image" src="https://github.com/user-attachments/assets/7b14bf3d-5feb-47fb-82b3-3c721c84edcb" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="574" height="124" alt="image" src="https://github.com/user-attachments/assets/9d705d58-c6c3-45e9-87a0-6f96b34bc465" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="457" height="56" alt="image" src="https://github.com/user-attachments/assets/8a8848a6-8774-491b-b190-7e4f65e69e04" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="679" height="182" alt="image" src="https://github.com/user-attachments/assets/efb929bc-383a-4f9a-a64e-41a2ec2839d0" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="720" height="124" alt="image" src="https://github.com/user-attachments/assets/ac1a443b-8828-4488-bc79-483f11e3b0bd" />

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
<img width="699" height="396" alt="image" src="https://github.com/user-attachments/assets/cd76ed05-8c29-4b5b-8f20-a1b86f53a10e" />

 
ls file1
## OUTPUT
<img width="638" height="78" alt="image" src="https://github.com/user-attachments/assets/17d7aaf1-99ed-4356-a70e-7a5a81f5a9af" />

echo $?
## OUTPUT 
<img width="629" height="77" alt="image" src="https://github.com/user-attachments/assets/7aff4921-a0e4-4d4d-87c4-6a15cfe4dd35" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="681" height="218" alt="image" src="https://github.com/user-attachments/assets/c63b39cc-c084-42da-97ac-9639db632623" />

abcd
 
echo $?
 ## OUTPUT


<img width="679" height="150" alt="image" src="https://github.com/user-attachments/assets/100e0a46-48fb-4728-bfe5-7fe5a9ed8ffa" />


 
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
<img width="719" height="531" alt="image" src="https://github.com/user-attachments/assets/14d9a055-10de-4d16-a177-97ae5f167076" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="626" height="152" alt="image" src="https://github.com/user-attachments/assets/961339d6-68fa-4bee-98d1-7125ae85fd9c" />




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
<img width="673" height="181" alt="image" src="https://github.com/user-attachments/assets/6b484c04-5ee1-4544-b627-aa7ff359e31e" />

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

<img width="671" height="199" alt="image" src="https://github.com/user-attachments/assets/80a4a944-3c98-4c76-b1a4-fb8a881fecd3" />


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
<img width="640" height="174" alt="image" src="https://github.com/user-attachments/assets/6ae7d562-50cd-471b-b9a4-6c9abb5bfc5d" />

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
<img width="627" height="211" alt="image" src="https://github.com/user-attachments/assets/31bc642c-0ec8-4868-9ec4-9f761cd797dd" />

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
<img width="682" height="153" alt="image" src="https://github.com/user-attachments/assets/56ca8661-e3a6-484b-bdd3-d4c24023ae61" />


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
<img width="631" height="147" alt="image" src="https://github.com/user-attachments/assets/79d75e10-40b4-4303-810b-07792f10f1c8" />

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
##output
 <img width="669" height="166" alt="image" src="https://github.com/user-attachments/assets/07f0f281-ca5f-4159-9dff-b9f9c409480d" />

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
##output

<img width="421" height="338" alt="image" src="https://github.com/user-attachments/assets/60306309-85f5-464f-8ce7-6bf0e8c7999e" />

 
 
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
 
 ##output
 <img width="626" height="222" alt="image" src="https://github.com/user-attachments/assets/d8f4c1b3-3560-44e0-83eb-6e3e46ccd361" />

 
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
 
 ## output 
 <img width="640" height="311" alt="image" src="https://github.com/user-attachments/assets/d9ca1581-e51a-411f-9cbc-0e4b3c15a632" />

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
 <img width="642" height="229" alt="image" src="https://github.com/user-attachments/assets/ab0f5247-7f4a-43d6-be06-f9e59ec427d9" />

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
  <img width="642" height="229" alt="image" src="https://github.com/user-attachments/assets/ab0f5247-7f4a-43d6-be06-f9e59ec427d9" />
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
 <img width="639" height="309" alt="image" src="https://github.com/user-attachments/assets/42b8ba65-76d2-4efc-93aa-ef1c0f5578ed" />

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
<img width="598" height="254" alt="image" src="https://github.com/user-attachments/assets/89acfa37-0bf4-4b38-b0b3-20c73d90b24c" />

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

<img width="371" height="227" alt="image" src="https://github.com/user-attachments/assets/90a8a460-3f12-499a-9a4d-bbfa1d44ade6" />

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
<img width="499" height="176" alt="image" src="https://github.com/user-attachments/assets/3d0be00e-6b90-4526-b94a-40eb843d9bfa" />

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
<img width="529" height="236" alt="image" src="https://github.com/user-attachments/assets/fc26f277-886d-4733-9204-5ae1ab0f6d81" />

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

 <img width="590" height="392" alt="image" src="https://github.com/user-attachments/assets/1add5b24-5d81-4a45-a603-ea2d9a26e5c3" />

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
<img width="684" height="152" alt="image" src="https://github.com/user-attachments/assets/26771d10-aeaa-477e-977f-642cc8f362e8" />
 
 
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
 <img width="663" height="202" alt="image" src="https://github.com/user-attachments/assets/1ee66632-9b03-4139-89e0-0eea198ca61a" />

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
<img width="625" height="166" alt="image" src="https://github.com/user-attachments/assets/e89a44c5-cba5-471f-b1e5-992a3ba028a5" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="787" height="260" alt="image" src="https://github.com/user-attachments/assets/8450a716-fb90-48c6-9db6-32b433deeec7" />



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

 <img width="374" height="82" alt="image" src="https://github.com/user-attachments/assets/95b3d9a9-d97e-4d88-b21d-20e3a88dd635" />

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
 <img width="470" height="176" alt="image" src="https://github.com/user-attachments/assets/859af58e-d98c-43f2-a810-a07a33d91a0b" />

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
<img width="570" height="178" alt="image" src="https://github.com/user-attachments/assets/01d82e3c-bac8-464b-a933-59b62b0fda23" />

 
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
 <img width="612" height="462" alt="image" src="https://github.com/user-attachments/assets/83338022-81ca-477d-b071-80790d8c019c" />

 
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
 <img width="526" height="374" alt="image" src="https://github.com/user-attachments/assets/cf520164-d446-40c6-b8d6-e5576178abd6" />

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
<img width="715" height="126" alt="image" src="https://github.com/user-attachments/assets/26806ba2-6403-46c2-99b7-c10d62bbfff1" />


# RESULT:
The Commands are executed successfully.
