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
<img width="646" height="127" alt="image" src="https://github.com/user-attachments/assets/b7088651-3bc9-49d9-a7d1-f70343b0014f" />



cat < file2
## OUTPUT
<img width="871" height="140" alt="image" src="https://github.com/user-attachments/assets/052ee6e5-8b65-490f-a1a2-74d34d8ed0b7" />


# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT
<img width="655" height="68" alt="image" src="https://github.com/user-attachments/assets/783df3ef-b270-42af-9411-7df2f68c4608" />

 
diff file1 file2
## OUTPUT
<img width="618" height="200" alt="image" src="https://github.com/user-attachments/assets/fe872114-00d5-4cfd-ace4-48a516fed734" />


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
<img width="485" height="95" alt="image" src="https://github.com/user-attachments/assets/ae448df2-47d3-4a40-8ff7-0cb43ccfd02a" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="498" height="103" alt="image" src="https://github.com/user-attachments/assets/10531d8e-e8e1-4f3b-bd7d-e5208cb4e6e0" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="385" height="107" alt="image" src="https://github.com/user-attachments/assets/dcff844f-653d-4516-9cd8-4ab57fcb2cc5" />


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
<img width="426" height="75" alt="image" src="https://github.com/user-attachments/assets/124b91eb-9962-4701-8059-24be0d34ceb2" />



grep hello newfile 
## OUTPUT
<img width="365" height="72" alt="image" src="https://github.com/user-attachments/assets/c3304dd2-a988-4b35-ac4d-ef7b6241c1f9" />




grep -v hello newfile 
## OUTPUT
<img width="433" height="71" alt="image" src="https://github.com/user-attachments/assets/c2d4636f-9316-4c9c-ac07-51fd5e61d696" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="345" height="87" alt="image" src="https://github.com/user-attachments/assets/de64253f-1859-49fb-9ab6-353bd57ebcf1" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="358" height="65" alt="image" src="https://github.com/user-attachments/assets/12b06b29-11d2-410d-806a-21203d8cc63a" />




grep -R ubuntu /etc
## OUTPUT
<img width="318" height="70" alt="image" src="https://github.com/user-attachments/assets/680b131b-2512-42e3-abdb-ce93ca1a0324" />



grep -w -n world newfile   
## OUTPUT
<img width="318" height="70" alt="image" src="https://github.com/user-attachments/assets/002e35a3-341b-40f7-ac27-8dc198630c08" />


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
<img width="370" height="90" alt="image" src="https://github.com/user-attachments/assets/1c2a05c9-5d47-4d18-89b6-38faa6bdd5f0" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="406" height="97" alt="image" src="https://github.com/user-attachments/assets/87e233bb-05fd-464b-9a55-5e6e6f835fa3" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="413" height="91" alt="image" src="https://github.com/user-attachments/assets/f2d3818a-5ba9-4938-b779-d69d06365a7b" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="370" height="75" alt="image" src="https://github.com/user-attachments/assets/9576b088-a8ff-48e2-b3cb-8fa07af50fdd" />



egrep '(world$)' newfile 
## OUTPUT
<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/e8166487-05e7-486f-9c18-1d97382664bb" />



egrep '(World$)' newfile 
## OUTPUT
<img width="445" height="77" alt="image" src="https://github.com/user-attachments/assets/dee91e72-1316-4eb3-aefd-94ab3a758127" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="351" height="102" alt="image" src="https://github.com/user-attachments/assets/38be0203-6d2c-48f6-8792-af1a486c9b4d" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="425" height="75" alt="image" src="https://github.com/user-attachments/assets/5c11237b-e4b9-4ec7-a2e1-af675128a88a" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="355" height="70" alt="image" src="https://github.com/user-attachments/assets/4323c2d6-a401-4c20-abaf-2ba2afa01caf" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="357" height="75" alt="image" src="https://github.com/user-attachments/assets/a5e22f84-8a40-42d2-b8dc-83a8694a4cf5" />


egrep l{2} newfile
## OUTPUT
<img width="498" height="88" alt="image" src="https://github.com/user-attachments/assets/365e4075-aa68-40da-a771-39e1e1d1cb87" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="392" height="102" alt="image" src="https://github.com/user-attachments/assets/9ff6f41a-6f1e-49dd-9c76-be387a92f044" />


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
<img width="395" height="68" alt="image" src="https://github.com/user-attachments/assets/9793598d-6b49-46ce-9df3-a33edfe6293f" />



sed -n -e '$p' file23
## OUTPUT
<img width="345" height="75" alt="image" src="https://github.com/user-attachments/assets/f7834244-8cb4-4c6f-9f20-d86971b5fd49" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="390" height="191" alt="image" src="https://github.com/user-attachments/assets/3b63269e-c925-41d0-98c1-37a16d2c88a8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="383" height="185" alt="image" src="https://github.com/user-attachments/assets/8345dcb7-2aa5-4b3b-9d69-c234e538138d" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="488" height="192" alt="image" src="https://github.com/user-attachments/assets/71a5acea-8113-4c03-9586-cab382c0f0e4" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="387" height="140" alt="image" src="https://github.com/user-attachments/assets/f96dcccd-febf-4b3e-9c02-26ffa45b0cd7" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="412" height="115" alt="image" src="https://github.com/user-attachments/assets/9b796624-2de6-45fc-bda6-258219cc409b" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="465" height="76" alt="image" src="https://github.com/user-attachments/assets/319d5b5f-dd96-4741-be6d-3d053574c72a" />



seq 10 
## OUTPUT
<img width="438" height="221" alt="image" src="https://github.com/user-attachments/assets/1f108d2c-d07b-4ea8-b34e-6222466b022a" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="372" height="103" alt="image" src="https://github.com/user-attachments/assets/ee890151-3f4c-4e14-9537-7cd4be247c1e" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="432" height="106" alt="image" src="https://github.com/user-attachments/assets/e0d1e5bc-d801-460a-a058-7aacd2d630eb" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="451" height="115" alt="image" src="https://github.com/user-attachments/assets/02ff6e93-aa57-4b53-b22d-557c537f4a1d" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="365" height="103" alt="image" src="https://github.com/user-attachments/assets/51c1975e-1f08-43a9-ab81-508822a5f093" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="377" height="100" alt="image" src="https://github.com/user-attachments/assets/562155a6-b30c-4c6c-8b8e-0e88e5b1a5d4" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="405" height="110" alt="image" src="https://github.com/user-attachments/assets/ed72dfa6-03bf-44a1-bc13-cf9f804ac280" />



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
<img width="405" height="145" alt="image" src="https://github.com/user-attachments/assets/a3f92c2d-baf1-4652-a002-7fe19cb3be32" />


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
<img width="458" height="161" alt="image" src="https://github.com/user-attachments/assets/0be23736-e071-4a84-a6c3-979e7c1bc868" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="457" height="190" alt="image" src="https://github.com/user-attachments/assets/2d3e0466-0377-4cba-aec1-f8bdc57d5156" />

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

<img width="407" height="102" alt="image" src="https://github.com/user-attachments/assets/58d97cef-ea94-499f-a216-d5212707e45a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="447" height="100" alt="image" src="https://github.com/user-attachments/assets/0b0e0742-bff2-48b3-80bb-cca3f6e402fa" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="935" height="977" alt="image" src="https://github.com/user-attachments/assets/bc11e7b9-f67e-40e4-8a47-ba141363c25a" />


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="605" height="208" alt="image" src="https://github.com/user-attachments/assets/32887488-0b91-4e24-96e5-3a4a24c82f37" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="371" height="217" alt="image" src="https://github.com/user-attachments/assets/2eb34274-c7cc-44f6-a8b8-a08212b07723" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
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
<img width="877" height="256" alt="image" src="https://github.com/user-attachments/assets/ae193293-e304-41bf-a240-79aebd37b7fa" />

 
ls file1
## OUTPUT
<img width="383" height="68" alt="image" src="https://github.com/user-attachments/assets/485e5876-09ad-4249-99ac-fdbb731710dd" />

echo $?
## OUTPUT 
<img width="360" height="65" alt="image" src="https://github.com/user-attachments/assets/47185402-858f-4604-8394-9823358ca967" />

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
<img width="360" height="115" alt="image" src="https://github.com/user-attachments/assets/f7bdf88f-86be-41e8-9598-c8cfc7b7b4bc" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="622" height="115" alt="image" src="https://github.com/user-attachments/assets/2571103e-7f5b-459d-8958-f01ff6e729d9" />


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
<img width="582" height="152" alt="image" src="https://github.com/user-attachments/assets/c70a412f-17f9-491c-94f8-45adc636db2d" />

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
<img width="490" height="162" alt="image" src="https://github.com/user-attachments/assets/24fc83c8-a82c-4e7b-b9f1-abf1aceb9126" />



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
<img width="512" height="268" alt="image" src="https://github.com/user-attachments/assets/ff85050c-cf84-4560-8810-b9c7ca04f914" />

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
<img width="532" height="311" alt="image" src="https://github.com/user-attachments/assets/5b5a4ebe-6227-4ef4-983d-0e517345fc26" />

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
<img width="551" height="75" alt="image" src="https://github.com/user-attachments/assets/1420c69e-07dc-4672-896b-2c7704d452d0" />


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
<img width="442" height="157" alt="image" src="https://github.com/user-attachments/assets/a147b410-e952-4da6-b04d-a931249fbc58" />

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
<img width="561" height="257" alt="image" src="https://github.com/user-attachments/assets/74da3a76-e374-4f34-94aa-4abd9e9f13e0" />

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
<img width="437" height="165" alt="image" src="https://github.com/user-attachments/assets/f267d3b2-179d-4c00-9de6-ef0466ef2dbc" />


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
<img width="388" height="152" alt="image" src="https://github.com/user-attachments/assets/4a421674-e2ba-46e9-b7d6-06b3929fc0e0" />

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
<img width="388" height="152" alt="image" src="https://github.com/user-attachments/assets/d428f182-8e1b-42d1-be08-f83dcf326d48" />

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
<img width="406" height="175" alt="image" src="https://github.com/user-attachments/assets/5888bd22-a45b-43ee-965d-52478698ef45" />

 
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
<img width="517" height="236" alt="image" src="https://github.com/user-attachments/assets/f270e54a-625d-447a-a112-dee22594a106" />

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
 <img width="517" height="236" alt="image" src="https://github.com/user-attachments/assets/dd7d8915-e892-48ef-9ee4-aa2f3c808d13" />

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
<img width="425" height="143" alt="image" src="https://github.com/user-attachments/assets/c38a899b-04d5-4fd0-a3b8-064dbe8c3e91" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="425" height="138" alt="image" src="https://github.com/user-attachments/assets/ba7711e3-4b0b-46c7-9880-355920a2c0cc" />


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
<img width="575" height="225" alt="image" src="https://github.com/user-attachments/assets/3e441f60-a6d8-4fc5-9fa8-dbce5ac7a85a" />

 
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
 <img width="515" height="153" alt="image" src="https://github.com/user-attachments/assets/1c233057-56ff-42d6-ac4a-49223f2a0358" />

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
 <img width="437" height="101" alt="image" src="https://github.com/user-attachments/assets/caf26e97-f0d9-4ad5-9e19-6dd8f13e0c4c" />

 
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
 <img width="578" height="493" alt="image" src="https://github.com/user-attachments/assets/f7c50d6e-ca58-42c8-b331-ad83ad9e162a" />

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

<img width="590" height="645" alt="image" src="https://github.com/user-attachments/assets/a201a110-ca6e-447f-8192-dfbb36963445" />

# RESULT:
The Commands are executed successfully.
