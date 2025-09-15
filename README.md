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

![WhatsApp Image 2025-09-15 at 17 47 48_bdfbbda7](https://github.com/user-attachments/assets/99a7e7ab-8fec-4c95-920f-40e857164e2d)


cat < file2
## OUTPUT

<img width="287" height="154" alt="Screenshot (563)" src="https://github.com/user-attachments/assets/deede165-4923-47a2-93ca-b9bbd7667d1a" />



# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="363" height="44" alt="Screenshot (564)" src="https://github.com/user-attachments/assets/18f543a8-f12a-4791-8107-4ed6b447fbcf" />

comm file1 file2
 ## OUTPUT

<img width="370" height="182" alt="Screenshot (565)" src="https://github.com/user-attachments/assets/b503b965-2068-4433-ba75-b5132ebea1df" />

 
diff file1 file2
## OUTPUT

<img width="372" height="183" alt="Screenshot (567)" src="https://github.com/user-attachments/assets/103c77d6-4cde-406d-a046-f31413db1b69" />


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

<img width="365" height="86" alt="Screenshot (568)" src="https://github.com/user-attachments/assets/443c782b-099b-43fe-9a7b-abbbd652bab5" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="418" height="106" alt="Screenshot (569)" src="https://github.com/user-attachments/assets/d71b53d0-3fa7-4b38-a804-1a9d9243e3ea" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="460" height="130" alt="Screenshot (570)" src="https://github.com/user-attachments/assets/be864309-cc01-4761-9299-c698d07d885e" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world

## OUTPUT

<img width="307" height="73" alt="Screenshot (571)" src="https://github.com/user-attachments/assets/26a19a71-34fc-46bc-8cbb-38cf30b1e3f5" />


grep Hello newfile 
## OUTPUT

<img width="437" height="40" alt="Screenshot (572)" src="https://github.com/user-attachments/assets/2c6c6db9-04ab-4025-a458-b652f1789ae4" />


grep hello newfile 
## OUTPUT

<img width="402" height="41" alt="Screenshot (576)" src="https://github.com/user-attachments/assets/88f6a028-a922-4951-adf2-431390dc3004" />



grep -v hello newfile 
## OUTPUT

<img width="413" height="69" alt="Screenshot (574)" src="https://github.com/user-attachments/assets/6edfecd8-02d5-46cc-afaa-af5a285de566" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="489" height="75" alt="Screenshot (575)" src="https://github.com/user-attachments/assets/58436db6-1362-41ed-8424-44d65931ee0a" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="629" height="54" alt="Screenshot (577)" src="https://github.com/user-attachments/assets/ef4299d5-5f6a-44dd-83f2-7eb566f5e655" />



grep -R ubuntu /etc
## OUTPUT

<img width="936" height="516" alt="Screenshot (578)" src="https://github.com/user-attachments/assets/7dd7b305-cce7-4261-a9a4-d7c549ca7711" />


<img width="811" height="525" alt="Screenshot (579)" src="https://github.com/user-attachments/assets/d197e78e-de1e-4b0e-9572-da86de0b3b59" />





grep -w -n world newfile   
## OUTPUT

<img width="502" height="70" alt="Screenshot (580)" src="https://github.com/user-attachments/assets/9ae90209-5a18-483e-940b-0bcac195ab65" />


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

<img width="569" height="70" alt="Screenshot (581)" src="https://github.com/user-attachments/assets/4c29ea83-8396-4b9d-90f0-c3277a37e624" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="554" height="71" alt="Screenshot (582)" src="https://github.com/user-attachments/assets/6774c2ad-86ac-4ac6-a1a9-12e423093799" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="529" height="72" alt="Screenshot (583)" src="https://github.com/user-attachments/assets/3ec7ab2e-b114-40d3-981e-c07bdff18886" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="460" height="49" alt="Screenshot (584)" src="https://github.com/user-attachments/assets/27e16b76-ad01-4f5e-8c57-4a67a49481b1" />


egrep '(world$)' newfile 
## OUTPUT

<img width="465" height="68" alt="Screenshot (585)" src="https://github.com/user-attachments/assets/21e42cd5-fc8b-4981-a75f-6f9f04f10c95" />


egrep '(World$)' newfile 
## OUTPUT

<img width="623" height="58" alt="Screenshot (586)" src="https://github.com/user-attachments/assets/5fb09393-9fe8-4ada-b9d2-c6f4d839fdf4" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="635" height="131" alt="Screenshot (589)" src="https://github.com/user-attachments/assets/4258d383-ed67-41da-8b59-c79165560654" />


egrep '[1-9]' newfile 
## OUTPUT

![WhatsApp Image 2025-09-15 at 15 22 32_11d97df4](https://github.com/user-attachments/assets/50131bb6-fc92-48f6-a992-6acbb439c0cb)


egrep 'Linux.*world' newfile 
## OUTPUT

![WhatsApp Image 2025-09-15 at 15 26 15_881bdc47](https://github.com/user-attachments/assets/eda8d473-003d-482e-8d91-b0dccd0084e3)

egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-09-15 at 17 41 30_5a312e75](https://github.com/user-attachments/assets/ee36d36e-ded4-4f80-a8c5-6745b78ae9e2)



egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-09-15 at 15 33 01_1c042193](https://github.com/user-attachments/assets/3ebdaddb-3897-4e89-9bbd-ca74a493c884)


egrep 's{1,2}' newfile
## OUTPUT 

![WhatsApp Image 2025-09-15 at 15 35 01_b95ebd95](https://github.com/user-attachments/assets/916084f0-308d-4332-8436-43acd2d24bc1)


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

<img width="524" height="52" alt="Screenshot (473)" src="https://github.com/user-attachments/assets/8973fea6-27cd-4b8b-b5ff-b11d4f45dc67" />



sed -n -e '$p' file23
## OUTPUT

<img width="453" height="50" alt="Screenshot (474)" src="https://github.com/user-attachments/assets/85598457-114f-4cc6-9297-9e43ca4691a3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="453" height="50" alt="Screenshot (474)" src="https://github.com/user-attachments/assets/22393ad5-435a-4883-b007-06c21876808f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="568" height="197" alt="Screenshot (476)" src="https://github.com/user-attachments/assets/964f71bb-1cd9-4aee-a05b-20ed431fe8c4" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="577" height="203" alt="Screenshot (477)" src="https://github.com/user-attachments/assets/64469e4e-e919-4c6f-b3aa-626bedb91679" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="566" height="167" alt="Screenshot (500)" src="https://github.com/user-attachments/assets/36ced942-9055-474d-9f35-171fdf934f0d" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="565" height="108" alt="Screenshot (501)" src="https://github.com/user-attachments/assets/6a230c29-fe80-4a9b-8d84-ccf80941eb89" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="731" height="77" alt="Screenshot (502)" src="https://github.com/user-attachments/assets/a7cc1323-931e-409c-904f-667e97b1245e" />



seq 10 
## OUTPUT

<img width="520" height="293" alt="Screenshot (503)" src="https://github.com/user-attachments/assets/e4c98dd5-a158-46ad-8711-c67d7ee86036" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="584" height="110" alt="Screenshot (504)" src="https://github.com/user-attachments/assets/f2748842-34b9-4ae9-a33b-1c2b4f200301" />


seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="619" height="111" alt="Screenshot (505)" src="https://github.com/user-attachments/assets/0e736973-9fd7-43c5-ad29-331075063dc3" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="651" height="127" alt="Screenshot (506)" src="https://github.com/user-attachments/assets/251ed0d8-26a8-4d14-b2af-60ebdc1e0f6f" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="498" height="109" alt="Screenshot (507)" src="https://github.com/user-attachments/assets/2aa4def7-5a00-4621-a767-ee327acc4200" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="553" height="104" alt="Screenshot (508)" src="https://github.com/user-attachments/assets/a70dd7e8-d6d5-4d86-adad-03884a16fd85" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="690" height="102" alt="Screenshot (509)" src="https://github.com/user-attachments/assets/fbea4970-0282-421e-b7dd-8d1f6edf95fd" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="643" height="105" alt="Screenshot (510)" src="https://github.com/user-attachments/assets/0f9a6734-965b-48c1-bb3b-5102b186d346" />


#Sorting File content cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```

<img width="522" height="158" alt="Screenshot (511)" src="https://github.com/user-attachments/assets/120bf95e-399b-44a4-beca-b0da971812b1" />

sort file21
## OUTPUT

![WhatsApp Image 2025-09-15 at 16 01 17_ba05fd94](https://github.com/user-attachments/assets/41f2e405-f005-433c-8d90-b8f76f33c37f)

cat>file22

```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
cat>file22

<img width="436" height="182" alt="Screenshot (512)" src="https://github.com/user-attachments/assets/06183b20-e072-48c5-a8a3-23e2576e1895" />

uniq file22
## OUTPUT

<img width="454" height="162" alt="Screenshot (513)" src="https://github.com/user-attachments/assets/6e4bc925-6f91-43c2-9f97-e3e41b83a91b" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


<img width="685" height="233" alt="Screenshot (514)" src="https://github.com/user-attachments/assets/e9f23af7-874b-412a-928a-6bd8e6638e7f" />

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

<img width="639" height="132" alt="Screenshot (515)" src="https://github.com/user-attachments/assets/105e4b07-2a92-48b7-a434-3373a27a9914" />


cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="565" height="132" alt="Screenshot (516)" src="https://github.com/user-attachments/assets/e0475524-3a54-4608-9fad-89e1998d4aab" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="710" height="138" alt="Screenshot (517)" src="https://github.com/user-attachments/assets/807ab5b3-b9e3-43da-977f-e0c3a706829f" />


#Backup commands tar -cvf backup.tar *
## OUTPUT

<img width="741" height="430" alt="Screenshot (518)" src="https://github.com/user-attachments/assets/07cfdfd2-c882-4baa-ab31-0822aa10ff40" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="820" height="522" alt="Screenshot (519)" src="https://github.com/user-attachments/assets/3135be9f-808c-461a-9bb0-2239f94390ed" />


tar -xvf backup.tar
## OUTPUT


<img width="758" height="525" alt="Screenshot (520)" src="https://github.com/user-attachments/assets/21c5e7c5-c683-4168-96b0-b56094aa1897" />


gzip backup.tar

ls .gz
## OUTPUT

<img width="796" height="489" alt="Screenshot (521)" src="https://github.com/user-attachments/assets/69a2c4c9-c932-4771-b0e8-e13e500f8764" />

 
gunzip backup.tar.gz ls

## OUTPUT

<img width="674" height="132" alt="Screenshot (522)" src="https://github.com/user-attachments/assets/2f895973-c29d-4b10-8cfd-4bb0b73b71f5" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="804" height="133" alt="Screenshot (523)" src="https://github.com/user-attachments/assets/3f46e6d3-67dd-440a-9d95-a7887ad44967" />

 

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="449" height="125" alt="Screenshot (524)" src="https://github.com/user-attachments/assets/6644e462-939d-45f8-9f05-9769abf1e9ae" />


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
 ## OUTPUT

 <img width="531" height="318" alt="Screenshot (525)" src="https://github.com/user-attachments/assets/97bc2622-cd7c-409a-989f-05a897e83041" />
 

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

<img width="736" height="430" alt="Screenshot (526)" src="https://github.com/user-attachments/assets/292b2987-dd4b-4799-bbf8-118c121d3b04" />


 
ls file1
## OUTPUT

<img width="425" height="53" alt="Screenshot (527)" src="https://github.com/user-attachments/assets/0b875e0e-2b45-4506-855c-424a85f57e2b" />


echo $?
## OUTPUT 

<img width="392" height="56" alt="Screenshot (528)" src="https://github.com/user-attachments/assets/e4ada54b-083d-486e-98b9-f8a81e71ae95" />


./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="699" height="101" alt="Screenshot (529)" src="https://github.com/user-attachments/assets/c1fe2c8c-e9d3-49fe-a5e6-287ff5b59542" />

abcd
 
echo $?
 ## OUTPUT

<img width="398" height="50" alt="Screenshot (530)" src="https://github.com/user-attachments/assets/c7a1fc55-942d-4654-be25-3c71100c47b6" />

 
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

<img width="717" height="284" alt="Screenshot (531)" src="https://github.com/user-attachments/assets/e8d0f3ae-4e40-4d53-9905-074797c7c066" />


chmod 755 strcomp.sh 
./strcomp.sh 
## OUTPUT

<img width="815" height="114" alt="Screenshot (532)" src="https://github.com/user-attachments/assets/7893ffe5-843c-4fc5-8681-4e91922fa843" />


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
## OUTPUT

![WhatsApp Image 2025-09-15 at 15 43 16_3ab6c072](https://github.com/user-attachments/assets/4e726264-6002-4898-9810-a76f569cc8a6)

./ifnested.sh 

## OUTPUT


<img width="534" height="57" alt="Screenshot (535)" src="https://github.com/user-attachments/assets/5d2c4dc0-2f6b-479b-8095-5207f13c6534" />

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
##OUTPUT

<img width="633" height="398" alt="Screenshot (536)" src="https://github.com/user-attachments/assets/35e24055-9c22-4e77-9877-f18303c9a970" />


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

<img width="760" height="157" alt="Screenshot (537)" src="https://github.com/user-attachments/assets/1ba6a323-e083-4a9d-b257-6bb01b50b0d8" />


# check if a file

cat > ifnested.sh 

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
##OUTPUT

![WhatsApp Image 2025-09-15 at 15 43 16_d04980f4](https://github.com/user-attachments/assets/c72290e1-6524-4696-86c0-14d9ebbf1ec7)


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

![WhatsApp Image 2025-09-15 at 18 02 18_d6af7272](https://github.com/user-attachments/assets/311553d4-2c09-4a49-a744-33a73b1fe316)



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

<img width="781" height="108" alt="Screenshot (539)" src="https://github.com/user-attachments/assets/b9c5bff3-e1c5-413e-9314-42849f438af2" />


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

<img width="774" height="112" alt="Screenshot (540)" src="https://github.com/user-attachments/assets/7403b6e3-ca07-4c60-8998-64aada3363cc" />

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


 ##OUTPUT


<img width="776" height="107" alt="Screenshot (541)" src="https://github.com/user-attachments/assets/1d200eaa-d0a0-46cb-9264-2a8d5007338a" />


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

 ##OUTPUT

 <img width="705" height="307" alt="Screenshot (542)" src="https://github.com/user-attachments/assets/6436ee69-0d19-4ee6-8968-3cbd4b46dfc9" />

 
cat untiltest.sh 

```
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

 ##OUTPUT

 <img width="650" height="184" alt="Screenshot (543)" src="https://github.com/user-attachments/assets/2225d9b9-1058-4067-83e6-1dc03b59f83b" />
 

```
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 

##OUTPUT


<img width="746" height="265" alt="Screenshot (544)" src="https://github.com/user-attachments/assets/437412b6-b97f-4edd-92fe-fc1f2ff63ce6" />

```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 

##OUTPUT

<img width="746" height="183" alt="Screenshot (545)" src="https://github.com/user-attachments/assets/79c135f8-1196-4f5d-892f-3fdf141acc7d" />


```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 ##OUTPUT

 <img width="711" height="193" alt="Screenshot (546)" src="https://github.com/user-attachments/assets/77725079-794c-4ced-a6d9-dfb6890e1a0a" />

cat forin3.sh 
```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 

##OUTPUT

<img width="741" height="260" alt="Screenshot (547)" src="https://github.com/user-attachments/assets/8a6893ba-cc94-4635-be1b-7e0055e341be" />

```
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

<img width="791" height="110" alt="Screenshot (548)" src="https://github.com/user-attachments/assets/481b5b73-ee36-44a6-80dc-5801d5c820f5" />

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

<img width="631" height="78" alt="Screenshot (549)" src="https://github.com/user-attachments/assets/969ef9c0-c31e-4793-81ac-feb1f3b9ff1e" />


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

<img width="537" height="177" alt="Screenshot (550)" src="https://github.com/user-attachments/assets/4644cc0b-495e-4066-bcec-719dcdf96f87" />


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

<img width="643" height="91" alt="Screenshot (552)" src="https://github.com/user-attachments/assets/bb9d68a3-8ec2-483d-aec7-cc3194730c1a" />

cat >fornested1.sh 
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


 ![WhatsApp Image 2025-09-15 at 16 32 10_4292794b](https://github.com/user-attachments/assets/79850571-a0bd-4063-a0fa-5cf68985737d)

 

cat forbreak.sh 
```
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

 ![WhatsApp Image 2025-09-15 at 16 40 32_0e3101ab](https://github.com/user-attachments/assets/1960bc6c-004c-4442-bfbf-f57c20502982)
 

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


<img width="573" height="179" alt="Screenshot (555)" src="https://github.com/user-attachments/assets/412ba562-cf3f-45e6-a94d-32fe44dda315" />

 
cat >exread.sh 
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


<img width="596" height="87" alt="Screenshot (556)" src="https://github.com/user-attachments/assets/c28e1587-a1da-4b5e-b38c-03d10f3b08ea" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT

 <img width="596" height="87" alt="Screenshot (556)" src="https://github.com/user-attachments/assets/d5c1fc03-2cac-4ed9-b9d4-185a4bbd38ad" />

 
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


<img width="513" height="66" alt="Screenshot (557)" src="https://github.com/user-attachments/assets/09dc578a-99fd-4051-8d6b-244947fd727a" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT


 <img width="546" height="114" alt="Screenshot (558)" src="https://github.com/user-attachments/assets/5e043d1a-0c34-4c28-92aa-b4674792f504" />

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
$ ./argshift.sh 1 2 3

## OUTPUT

<img width="452" height="107" alt="Screenshot (559)" src="https://github.com/user-attachments/assets/6bffb76d-c0eb-4a2e-bdc2-11ff227d14c9" />

 
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
 
 <img width="494" height="371" alt="Screenshot (560)" src="https://github.com/user-attachments/assets/999c62fa-665b-4876-96f9-1ecdad98f89a" />

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

![WhatsApp Image 2025-09-15 at 16 40 54_26eaa35b](https://github.com/user-attachments/assets/9bd8b191-e26e-4bdf-b03e-2ff7e284d341)

 
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

<img width="517" height="89" alt="Screenshot (561)" src="https://github.com/user-attachments/assets/7370aefa-6bde-401d-b7cf-e7d01bd33812" />

# RESULT:
The Commands are executed successfully.
