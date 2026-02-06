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
<img width="341" height="102" alt="545715084-0dbcb619-dd43-4841-bed2-ec90016e72b4" src="https://github.com/user-attachments/assets/a5f73e9c-3c5c-401f-99a2-152742d3f44f" />



cat < file2
## OUTPUT
<img width="328" height="162" alt="545715237-bb765009-eda0-4bb2-8d66-d6633743e078" src="https://github.com/user-attachments/assets/64279148-50a1-4ad9-8f7e-d2494f06d67d" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="362" height="44" alt="545715402-8f218ff6-bc3b-46d9-8496-7bb9ccd89b06" src="https://github.com/user-attachments/assets/fb2a1487-6434-4792-b557-7eac3922dbdf" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="545715521-fe328a3d-873b-46b6-8aa6-16cb8195cb3b" src="https://github.com/user-attachments/assets/6a229351-65a3-40de-b21a-7a73ef1d988f" />

 
diff file1 file2
## OUTPUT
<img width="428" height="305" alt="545715889-5d9f7bd4-987e-48b1-897e-53f119da7c39" src="https://github.com/user-attachments/assets/b83acd4b-2a5c-47fc-a738-4971630c8aa4" />


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

<img width="383" height="84" alt="545716444-b6ca6183-ca84-41f8-a5e1-72030885c5b1" src="https://github.com/user-attachments/assets/c3bb0fd1-8bc2-4ce4-9893-cd5fd48a5a3e" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="433" height="109" alt="545716741-0ed38233-8971-4fa5-90a7-1a3b1d369acd" src="https://github.com/user-attachments/assets/9a33812b-111f-4f0f-b747-18184ddba7e5" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="545716957-c3e41e7d-de94-4dcb-b5cb-8edba18c78f1" src="https://github.com/user-attachments/assets/70ad882f-8833-4120-8c0c-62a41eea1d44" />


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

<img width="409" height="56" alt="545717248-252efd85-f3cc-4899-b7ee-50f993798c1f" src="https://github.com/user-attachments/assets/f7f782c8-59b8-4672-9cd3-597e886a2d09" />


grep hello newfile 
## OUTPUT

<img width="400" height="58" alt="545717384-47de37e7-9df9-418a-bbfb-d8ab12b671af" src="https://github.com/user-attachments/assets/4552fdbd-7e3e-4257-9a96-60044770cf9a" />



grep -v hello newfile 
## OUTPUT

<img width="430" height="59" alt="545717489-7938d054-f2e3-4bba-8f00-e0f6532e5439" src="https://github.com/user-attachments/assets/88c8082b-e7ea-4bbb-bdbb-d97e8c5a62a3" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="546" height="81" alt="545718197-29b93fb9-4e18-47f8-926f-03e8481a8230" src="https://github.com/user-attachments/assets/46a06f32-0e94-40a3-b3cd-4ca50d6a5b6f" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="578" height="52" alt="545718356-2be27725-4bbf-46dc-9473-563a2e295e49" src="https://github.com/user-attachments/assets/46763591-4d41-4055-bb2c-385b539b38cc" />



grep -R ubuntu /etc
## OUTPUT

<img width="609" height="218" alt="545718529-1dd2560b-fbe9-4942-bed7-17811c5453d1" src="https://github.com/user-attachments/assets/b3e333f4-0f94-4ae1-8088-1fdedd5794ba" />


grep -w -n world newfile   
## OUTPUT
<img width="474" height="80" alt="545718644-9b9098c0-9bf2-4bdd-bc8e-10a07fb90405" src="https://github.com/user-attachments/assets/57853b86-f5c3-4579-9998-f77c2a9cb67a" />


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

<img width="563" height="78" alt="545718808-359d55a4-b535-483b-bd6d-47452d93fea1" src="https://github.com/user-attachments/assets/0623261f-60f0-404a-bc5a-fb6b017b8269" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="605" height="81" alt="545719069-937ba4b2-5988-4f46-83bd-280557849bb6" src="https://github.com/user-attachments/assets/f41de17d-f055-4ff2-a73a-3f6fe8ae545b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="605" height="81" alt="545719210-1ab5287e-be27-4d2b-9ba6-7f45bf336a64" src="https://github.com/user-attachments/assets/1b0f29ec-fb40-4df6-8802-fdb4044f60f0" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="489" height="58" alt="545719430-e78a6172-a3de-4429-8e72-e34b4d7eacae" src="https://github.com/user-attachments/assets/a019da15-f96b-439f-aa76-2cf59f6bf2d3" />


egrep '(world$)' newfile 
## OUTPUT
<img width="495" height="54" alt="545719713-71ea6252-d06c-489a-b6be-dd103168cba8" src="https://github.com/user-attachments/assets/c2dd24cd-5bc4-43ad-9a27-28759a8da6dc" />



egrep '(World$)' newfile 
## OUTPUT

<img width="485" height="49" alt="545719856-7192f144-ba70-4ef7-80e3-69d1cd0643e1" src="https://github.com/user-attachments/assets/3ead11c5-6e43-4b19-b4d8-4068d94f3a07" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="559" height="76" alt="545720002-c350a8a6-f2ac-4088-9140-6c56a530db1e" src="https://github.com/user-attachments/assets/6c1cd9cf-7f94-4f04-8154-6a19bc0c186c" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="475" height="62" alt="545720129-0a6cfce3-1145-4324-a012-e9f73b75d371" src="https://github.com/user-attachments/assets/34186c1f-cb5a-4ec6-8f2e-8fd8c364afc6" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="547" height="55" alt="545720462-ea4c5fed-5933-4c2e-a899-0cd874aa0a6f" src="https://github.com/user-attachments/assets/082410a6-70ce-4b47-8b13-d3c5d3acc7e8" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="540" height="57" alt="545720544-72748e5c-86b9-4105-88fc-452dc26bdb83" src="https://github.com/user-attachments/assets/0a4b9b8d-7882-4a69-8617-016160760ffe" />

egrep l{2} newfile
## OUTPUT

<img width="549" height="76" alt="545720671-645d2137-cdfd-4175-bdc1-c65ea3d9374d" src="https://github.com/user-attachments/assets/11b3f2ee-a68c-4650-ba53-a7e0176e1765" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="545720790-c2cbb080-f4a0-4857-9208-e3b4a5258556" src="https://github.com/user-attachments/assets/1b676a1b-b48a-4f0b-9411-ce9fd782cc69" />


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

<img width="446" height="52" alt="545721026-26ef3e32-ae83-4d77-b0ab-bedd76bd06e3" src="https://github.com/user-attachments/assets/b3664137-e7f6-43a3-8628-74cef17b7d1b" />


sed -n -e '$p' file23
## OUTPUT

<img width="463" height="58" alt="545721213-5fa6280c-083e-4c9a-beb0-1029671f4535" src="https://github.com/user-attachments/assets/247640c9-1c87-46e0-933d-441c2ff3adf7" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="520" height="243" alt="545721561-b9312515-c393-40f9-a8f8-d06bc66a73e5" src="https://github.com/user-attachments/assets/e8d8f0fe-3255-4d86-80c5-30aa0efcc21b" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="521" height="237" alt="545721740-924d78a2-6ff0-4143-b13c-5ab70c2028ca" src="https://github.com/user-attachments/assets/3dce8ad4-0732-453e-abaf-c432e388596b" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="555" height="245" alt="545721966-4fd9ec9f-69b9-4640-a890-4f62ca09a2ca" src="https://github.com/user-attachments/assets/32ebfc85-a2c8-4d60-882f-aba83a2c7eb2" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="481" height="169" alt="545722119-b5bbf561-5af6-4bec-a8d6-581947373088" src="https://github.com/user-attachments/assets/c8590e2c-92bd-4be2-a4a9-ae729fd9e523" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="520" height="108" alt="545722356-12e67cef-7529-4a04-b2b9-e9ccb38c6b36" src="https://github.com/user-attachments/assets/232fb23a-a831-47ab-86f5-b87ae8cf943e" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="560" height="83" alt="545722451-359a6ed8-9706-422e-b439-05f4b609ff41" src="https://github.com/user-attachments/assets/ca546387-a144-4263-8898-e6b17fb397f8" />


seq 10 
## OUTPUT

<img width="470" height="241" alt="545722562-6e2b785d-e910-4e04-b44a-4a028ed88e2a" src="https://github.com/user-attachments/assets/cf65bdc4-d2f8-44ab-a4a6-744891ad93cc" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="468" height="97" alt="545722705-7f15a008-0a21-4569-ac30-4b7f7b40c0ff" src="https://github.com/user-attachments/assets/c432c113-9cbc-4741-baab-eb8e360871b5" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="545722923-8eee58a9-fdd9-4bf2-b575-c2eac6dd4472" src="https://github.com/user-attachments/assets/c360607e-4a03-41c5-84fe-92a2332cfee9" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="476" height="116" alt="545723073-ffd87372-c552-45c6-b96e-11022988f0b2" src="https://github.com/user-attachments/assets/cbff23fa-ee9a-4d03-956f-169d73955e0f" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="545723246-097f3277-d23a-42fb-bff6-aba27afa0bbe" src="https://github.com/user-attachments/assets/9f2970a4-0a4e-41bb-a262-5965ac8800f3" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="478" height="94" alt="545723377-693b322b-65ba-4342-9af9-b50b5e1029b0" src="https://github.com/user-attachments/assets/5e82e108-4454-4479-9795-86dd56341f81" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="542" height="102" alt="545723561-6d8ddcd2-899d-47cf-9e08-f931218538ff" src="https://github.com/user-attachments/assets/396ff897-6efe-404a-adb2-c8511603851d" />


sed -n '2,4{s/$/*/;p}' file23

<img width="565" height="112" alt="545724699-f78cfd79-6ac5-4182-ad89-ee7625396e8f" src="https://github.com/user-attachments/assets/8696ac8a-2901-4344-bde7-1243575e6fd6" />

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
<img width="343" height="156" alt="545724896-b8c2d4b7-2624-4bdf-836d-b280ab298d5a" src="https://github.com/user-attachments/assets/ee009f1e-3b75-4e49-a1ed-40a93927da48" />


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
<img width="363" height="160" alt="545725071-fc329060-d42b-410b-bdf4-8e4745a6a9ef" src="https://github.com/user-attachments/assets/30372229-b9e9-430f-b2eb-b22c2e2c286b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="652" height="243" alt="545725245-bad19a45-d1aa-4624-aa5b-1cc85e286545" src="https://github.com/user-attachments/assets/58121fc5-c330-40d4-ab49-fb3cb492aec4" />

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

<img width="536" height="113" alt="545725406-1cc5cc00-160f-4132-8861-577703e95934" src="https://github.com/user-attachments/assets/448fc467-90b1-4557-97a5-7dcbf8fbb77c" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


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
<img width="337" height="97" alt="545732391-53497101-bc58-4fc4-86f9-1b46c4f0a5a7" src="https://github.com/user-attachments/assets/ca481849-feb5-4f1f-b66d-f86fc77828d1" />


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
<img width="430" height="331" alt="545732562-f92f3999-872a-4eab-a1d8-7ba4a476822b" src="https://github.com/user-attachments/assets/19b936b8-cbf6-4ddf-95fd-8ee47911d8af" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="545732675-6b466065-fc0a-41f3-b72a-af1e2463e723" src="https://github.com/user-attachments/assets/6eb32e5f-56bc-41b0-99b3-7a03ddf181f1" />


echo $?
## OUTPUT 
<img width="285" height="54" alt="545732951-a62cb0df-44c2-4eb6-a585-ee0625848b28" src="https://github.com/user-attachments/assets/861fe824-35d9-4f72-b92f-f2d3eb6c2abe" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="285" height="54" alt="545733419-3a7085ed-415b-401e-81e7-ddb358d5c666" src="https://github.com/user-attachments/assets/205d978c-01e2-43c8-a19d-3cc4d96281a6" />

abcd
 
echo $?
 ## OUTPUT
<img width="469" height="221" alt="545733533-3734e3fa-7b53-4a35-b356-486182fcfa80" src="https://github.com/user-attachments/assets/576a2d01-7904-4c0c-9aeb-b043d777a9f6" />


 
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

<img width="476" height="243" alt="545734204-c8988e15-bd7e-4fbc-90b7-b58792152690" src="https://github.com/user-attachments/assets/2b5f23eb-b5f9-44e5-8034-904add8c1a33" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="545734370-b4de53ad-9521-4a80-aacc-449b8db0d14f" src="https://github.com/user-attachments/assets/dfcdfae5-0405-48a1-ab0a-e2e1e9376cd8" />


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
<img width="631" height="256" alt="545734548-294cf245-9b79-4a70-bd21-1bb47f7d87cb" src="https://github.com/user-attachments/assets/968721e5-f6a8-4103-935f-311b28faeb00" />

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

<img width="524" height="391" alt="545734652-0e6cd444-f780-4875-8133-c19539a45213" src="https://github.com/user-attachments/assets/c73fd817-67d9-439d-97f3-68b1c109f303" />


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
<img width="524" height="391" alt="545734932-dd8674f4-80c0-453b-832d-12b700986578" src="https://github.com/user-attachments/assets/712c7903-1c48-4f30-a6fa-6fb98776b1d2" />

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
<img width="573" height="471" alt="545735185-0730cf1d-91e5-43d9-89da-994dde3198fe" src="https://github.com/user-attachments/assets/226c31c6-8934-4dda-8cf4-e0321116419a" />

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
<img width="573" height="471" alt="545735333-2e23f89b-a75f-4f9d-a88f-817df6c7d389" src="https://github.com/user-attachments/assets/a8e57cf1-4c0f-4fed-806a-8aae82f3d4ca" />


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
<img width="541" height="248" alt="545735444-8177e846-e99f-4855-8d14-50ce097bd4e1" src="https://github.com/user-attachments/assets/eac019ae-7887-494f-99df-6fc7799cf67f" />

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
<img width="504" height="160" alt="545735735-d61d981b-694f-4dd0-b736-7e8029916c69" src="https://github.com/user-attachments/assets/82c6fcfc-b436-487b-9afe-6a508c2bca30" />

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
<img width="446" height="201" alt="545735919-8cf1c20a-2b82-4134-9fb4-8d1b20b36e99" src="https://github.com/user-attachments/assets/89da4b96-4f1e-4462-a8e6-0f75b2e98043" />


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
<img width="397" height="204" alt="545736099-4a90ca87-e14b-4d50-a6b6-1dbed82c79e9" src="https://github.com/user-attachments/assets/bd5e9a90-4645-4c3c-9525-b7bc11fb24b9" />

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
<img width="397" height="204" alt="545736266-586040a3-ea19-43d6-a47d-02b8debd24dc" src="https://github.com/user-attachments/assets/fe44204d-66a4-4f00-9e89-58d69122637c" />

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
<img width="412" height="201" alt="545736398-5062367f-2e3f-4f48-b710-75b5823717b5" src="https://github.com/user-attachments/assets/004a24ad-a27e-45c9-80db-fd1bbb8f5f3e" />

 
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
<img width="756" height="275" alt="545736797-c3730244-90cd-4605-a148-502142bb340a" src="https://github.com/user-attachments/assets/e1b6a86f-a21b-496f-bc0d-363760f3c6ea" />

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
 <img width="481" height="144" alt="545736897-148ee4fd-9000-4ebe-a273-24d4d6e95d74" src="https://github.com/user-attachments/assets/eade093e-f878-4a94-abb7-0139bcf9b82e" />

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

<img width="774" height="137" alt="545737073-e232cdbf-3840-49f1-a397-1a11877909a3" src="https://github.com/user-attachments/assets/d7d25bd6-25b4-498f-b9dd-a1c8a6b1126e" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="774" height="137" alt="545737073-e232cdbf-3840-49f1-a397-1a11877909a3" src="https://github.com/user-attachments/assets/d9aacf4f-ef50-4dff-9d17-7bd3a2d77ff9" />


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
<img width="755" height="44" alt="545737354-67a62aaa-157f-4e01-a8aa-9b97472ad2a0" src="https://github.com/user-attachments/assets/e3f852bc-a6b1-4b99-8412-43a43b258e5e" />

 
 ./funcex.sh 1 2

 <img width="762" height="38" alt="545737557-3e33b5d0-2080-4e5e-971c-6d549a7c9178" src="https://github.com/user-attachments/assets/d9e1d6ab-74ce-4492-8ab1-362582dbd357" />

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
<img width="758" height="63" alt="545737852-36a18ae9-35e0-47b5-b28e-d84c927cbeab" src="https://github.com/user-attachments/assets/5423b72a-ba6c-4d56-8603-9f05f68dd2a7" />

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
<img width="762" height="87" alt="545738026-1350d147-3ec4-4ef5-add1-3d30100cdbaa" src="https://github.com/user-attachments/assets/db9480a2-291a-4098-a422-91d75505eade" />

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
 <img width="765" height="327" alt="545738182-f9f707f6-5930-4513-8292-068bbc0964b7" src="https://github.com/user-attachments/assets/6b8c10f6-9a93-4cb9-b3d7-895583312dd1" />

 
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
 <img width="783" height="218" alt="545739108-b0fcf24f-9be4-4d43-9f11-06cb5fb51ea7" src="https://github.com/user-attachments/assets/8b999cb3-2372-43e0-8123-dd4d0a4164f6" />

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
<img width="772" height="70" alt="545739339-adb5393c-330b-4aba-a359-c3f5e037aa68" src="https://github.com/user-attachments/assets/99c04712-ddba-4f93-bdef-da1a49812aa0" />


# RESULT:
The Commands are executed successfully.
