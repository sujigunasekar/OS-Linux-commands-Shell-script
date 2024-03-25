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

![312823451-0119401d-8e53-42c4-ab54-ce749dc6a03e](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e1865b3c-9ba5-4ae3-8130-75314196e683)


cat < file2
## OUTPUT
cat < file2
![312823636-9d6b43a7-9146-4ad3-bd12-6124400fb4d7](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/93397153-426e-49ce-b433-c42790615c81)


## OUTPUT
# Comparing Files
cmp file1 file2
## OUTPUT
 ![312824286-ec7146a1-7dcf-4519-b2bd-bb074874a9f6](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e062edf1-4a63-427b-9a62-37ef061f8eff)

comm file1 file2
 ## OUTPUT
![312824209-2b388c18-8716-471f-86a5-104b81593a8b](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/05c49397-217d-4e0e-9e31-981f43ba8ad3)

 
diff file1 file2


## OUTPUT

![312824501-bdc3e442-d591-40aa-b92a-121299adbb65](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/071153b0-4607-477b-9e5f-1b010506a750)

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

![312824664-141e89e4-c3d8-4296-b12d-a2e6bb80f2df](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/de3f331a-2bb9-4df2-b857-86cde0cdcd16)



cut -d "|" -f 1 file22
## OUTPUT

![312824777-b1f5d32d-f1a3-4a66-9c0e-10d02548f316](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e96044a5-af8e-4155-a777-a0b088bae5e5)


cut -d "|" -f 2 file22
## OUTPUT

![312824982-336fe232-b5b0-424a-88fe-5ca75d10039f](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/9215084c-72d8-4339-8278-e6d65b2937ea)

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

![312823117-fc26c416-54b1-4b9c-b839-1e6a77c2ff12](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/55f2321a-c935-4db9-a6c0-3ba4ded197e3)


grep hello newfile 
## OUTPUT


![312825332-3cfe2166-0ee0-46f4-9b7c-44512aeae4cd](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e141ebcc-5eae-4bd7-95eb-4506a9df818a)


grep -v hello newfile 
## OUTPUT
![312825594-d6dd2db3-b402-47b5-84f7-35e3b2038e37](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/1ea81849-58ba-4460-bbb8-1eaac3752cf3)



cat newfile | grep -i "hello"
## OUTPUT
![312826006-eb5b87a0-bb58-4854-a95f-1063a74d1320](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/933b3400-135a-4f53-92e8-0301035689af)




cat newfile | grep -i -c "hello"
## OUTPUT

![312826766-3c2aa26a-270d-42cf-9f04-ce10dc341942](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/a5c1bfa3-ff30-41a0-bc30-0329535288fe)



grep -R ubuntu /etc
## OUTPUT

![312827082-04c00dca-5051-48a8-9333-c20a7bfd9328](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/907a0c95-4309-48ca-ae05-c59845ca3e27)


grep -w -n world newfile   

## OUTPUT
![312827384-a08e3266-9005-4680-b75a-cb7687d0b869](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/13899c93-f0de-49cc-b523-50675bbaf210)



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



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT



sed -n -e '1,5p' file23
## OUTPUT



sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT

cat > file11

Hello world

This is my world

^d

cat > file22

1001 | Ram | 10000 | HR

1002 | tom | 5000 | Admin

1003 | Joe | 7000 | Developer

^d

cut -c1-3 file11

## OUTPUT
![312824664-141e89e4-c3d8-4296-b12d-a2e6bb80f2df](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/63d888df-a459-453c-a7ea-e2f303a3c781)

cut -d "|" -f 1 file22



## OUTPUT
![312824777-b1f5d32d-f1a3-4a66-9c0e-10d02548f316](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/1fb39f9b-9ba9-4cfa-9a20-d6a5fca9b676)



cut -d "|" -f 2 file22

## OUTPUT
![312824982-336fe232-b5b0-424a-88fe-5ca75d10039f](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/6d20246a-eb9b-45ab-a219-138653eeb9a7)

cat < newfile

Hello world

hello world

^d ` cat > newfile

Hello world

hello world

^d

grep Hello newfile
## OUTPUT
![312823117-fc26c416-54b1-4b9c-b839-1e6a77c2ff12](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/a0268508-b658-4d64-8c27-a16996ed9e67)

grep hello newfile


## OUTPUT
![312825332-3cfe2166-0ee0-46f4-9b7c-44512aeae4cd](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/85b4540c-3720-4935-88b3-81f063e9a0e8)
grep -v hello newfile



## OUTPUT
![312825594-d6dd2db3-b402-47b5-84f7-35e3b2038e37](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/7ae9e843-83c3-4ca0-8e37-8cce63d18e8b)
cat newfile | grep -i "hello"


## OUTPUT
![312826006-eb5b87a0-bb58-4854-a95f-1063a74d1320](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/032817fb-7117-4055-87b8-a3eb33609680)
cat newfile | grep -i -c "hello"


 ## OUTPUT
![312826766-3c2aa26a-270d-42cf-9f04-ce10dc341942](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/79571480-1e83-4d53-be2b-06d1ac1d66d4)
grep -R ubuntu /etc


 ## OUTPUT

![312827082-04c00dca-5051-48a8-9333-c20a7bfd9328](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/68baa075-f57a-4b03-9b98-1c609955cdfd)
grep -w -n world newfile


 
## OUTPUT
![312827384-a08e3266-9005-4680-b75a-cb7687d0b869](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/6f375ae3-dfff-4807-9c6a-2e0cf077e663)

cat < newfile

Hello world

hello world

Linux is world number 1

Unix is predecessor

Linux is best in this World

^d

cat > newfile

Hello world

hello world

Linux is world number 1

Unix is predecessor

Linux is best in this World

^d

egrep -w 'Hello|hello' newfile
## OUTPUT
![312830227-2e1abf54-ea02-4eb8-b1f6-fff5fef677e0](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/d886a2ed-37a9-481e-9bf7-cc2f266e4354)
egrep -w '(H|h)ello' newfile




## OUTPUT
![312830407-618c12f7-7069-417f-8616-481edb3859ad](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/15375789-eaae-40e4-aa81-a16255065ca2)
egrep -w '(H|h)ell[a-z]' newfile



## OUTPUT
![312830642-cc45623c-2d8c-40a7-901e-488b36d5ed02](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/8d2038be-a5bd-4882-902d-98d29fb2dd8d)

egrep '(^hello)' newfile


## OUTPUT
 ![312831337-705b8878-2407-4f14-b7ec-1a92f9a81314](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/eb22284b-c1bd-46fb-99a7-c5e6bc0cd7da)
egrep '(World$)' newfile


## OUTPUT
![312831486-740a21f7-daab-4ba2-8a61-4c282f7e7766](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/25c8136c-09a6-45ff-952f-e4dd1741ad8e)
egrep '((W|w)orld$)' newfile


## OUTPUT
![312831660-25ac512f-2dfb-4038-925f-0b2818d8a912](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/26d5b2dc-b1e5-4e3f-b27a-ff7bbe596897)
egrep '[1-9]' newfile


## OUTPUT
![312831851-27139ca7-cf2a-4851-8047-cd30f39b3da4](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/d8422c26-cf2a-4254-bd2f-18316763c64b)

 egrep 'Linux.*world' newfile


 
## OUTPUT
![312832122-65f9c469-4f04-4490-b7b8-75268e22fbce](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/cfcdb071-faa8-4301-9463-782814ff7b94)
egrep 'Linux.*World' newfile


## OUTPUT
![312832282-82dd6efa-a158-4a99-b1d3-60ec8d16d18c](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/3f7edf2b-93b2-48e6-9f24-362b4dec42f9)
egrep l{2} newfile



## OUTPUT 
![312832569-7878b983-dcc0-4fad-96df-0eabfaff7a9c](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e0a6d95f-f3dc-4404-a6a4-a304c475df22)
egrep 's{1,2}' newfile


## OUTPUT 
 ![312833039-5743baa7-5209-46b3-89ff-1398ce18f46d](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/b66f6083-34b1-48ee-bb6c-aab952faec08)

cat > file23

1001 | Ram | 10000 | HR

1001 | Ram | 10000 | HR

1002 | tom | 5000 | Admin

1003 | Joe | 7000 | Developer

1005 | Sam | 5000 | HR

1004 | Sit | 7000 | Dev

1003 | Joe | 7000 | Developer

1001 | Ram | 10000 | HR

^d

sed -n -e '3p' file23
 ## OUTPUT
![312890522-6ea57d36-ce6c-4daf-8d42-39476d4518a4](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/4087e342-6d0d-4a29-91c6-32b449cc6768)
sed -n -e '$p' file23



## OUTPUT
![312890691-ecf7119f-656f-4dfe-89fa-6e49e0f9104c](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/7c1c1260-8d28-441c-b2bd-73c4e17a5fc6)

sed -e 's/Ram/Sita/' file23



## OUTPUT
![312890912-677587a1-2033-4bcc-8394-4e7253d8906c](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/dfde99f0-fa3c-4ee9-9308-4b156fbb6f19)
sed -e '2s/Ram/Sita/' file23



## OUTPUT
![312891134-b00debdd-71b6-4595-8af4-8dd502d1e9d1](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/94f9b8e5-12cb-44c6-bd55-20afef336f33)

sed '/tom/s/5000/6000/' file23


## OUTPUT

![312891478-8f6fb32f-68c3-4685-8377-895403873fdf](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e343e5fa-f4d3-4e67-bef2-a5f03724e8cc)

sed -n -e '1,5p' file23





## OUTPUT
![312891653-a57f600b-bf98-4ccf-8ea3-c966a7e7097c](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/03e49e12-01a0-4e2d-9222-9b828fa5e625)
sed -n -e '2,/Joe/p' file23



## OUTPUT
![312892738-65246582-bd0f-490b-8352-01ff92960b8f](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/cc066302-85e9-411c-8e4c-78d2d947b99b)
sed -n -e '/tom/,/Joe/p' file23



## OUTPUT

![312891961-ca015e97-51d3-46b3-a4b2-883386487e96](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/c8f94558-cc4c-48c2-acdc-33ce86aafaf1)
seq 10



## OUTPUT
![312892165-d89684e2-6e84-4c92-b8f7-05a1c425b8f6](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/1ee2a815-d4fc-4ff2-a59b-c14a74634867)
seq 10 | sed -n '4,6p'

## OUTPUT
![312892951-f2346439-9a61-4e57-a9fb-66a7fe066be9](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e56ed090-4f4f-4d82-a643-2025d2ab0bea)

seq 10 | sed -n '2,~4p'\

## OUTPUT
![312893365-782ae142-f59f-4252-a128-61f12027a343](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/46709a93-225d-44e6-8349-fe29796d2d5c)
seq 3 | sed '2a hello'


## OUTPUT

![312893553-a198c8b4-6c65-4fe9-ba15-3b9106f603af](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/e11a6367-6206-4d6c-9994-0aeb589941eb)
seq 2 | sed '2i hello'


 ## OUTPUT
![312893738-cc2be9dc-529d-48a8-8006-8d9658906ac7](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/be2a6191-c0af-49f5-b1b2-b914b2346679)
seq 10 | sed '2,9c hello'


## OUTPUT
![312894013-1ff68b19-cd1a-4152-930d-191cdf0a400a](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/8aba6349-ac13-468a-9ff4-fccdf4cfe7bb)
sed -n '2,4{s/^/$/;p}' file23


 
## OUTPUT
![312894616-26180a7a-ef81-4172-b7aa-275a1a5545b3](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/1366e637-0936-4835-ade7-828cdc0cf9c6)

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![312894885-4082ae2d-91db-4998-95a9-336e7a63e3e4](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/81d415b2-296d-4f18-8bfd-63a0a612508a)
#Sorting File content

cat > file21

1001 | Ram | 10000 | HR 1002 | tom | 5000 | Admin 1003 | Joe | 7000 | Developer 1005 | Sam | 5000 | HR 1004 | Sit | 7000 | Dev

sort file21

## OUTPUT
![312896921-924b5e4f-b6d9-4ce3-894b-2b1edbf587c0](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/442de1b3-bb1e-4d39-9c94-97063f9eac81)
cat > file22

1001 | Ram | 10000 | HR 1001 | Ram | 10000 | HR 1002 | tom | 5000 | Admin 1003 | Joe | 7000 | Developer 1005 | Sam | 5000 | HR 1004 | Sit | 7000 | Dev

uniq file22


## OUTPUT
 ![312897587-94e1fa19-3646-4f72-97c8-eff4a0e11279](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/3d563768-5240-43a1-b0c4-69b65ea5c6f1)
#Using tr command

cat file23 | tr [:lower:] [:upper:]

## OUTPUT

![312897917-b286bcd8-f51d-4f2b-a6ae-c06dd89621f6](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/327b277e-56c9-4a8e-aea7-f6225f1f6060)
cat < urllist.txt

www. yahoo. com

www. google. com

www. mrcet.... com

^d

cat > urllist.txt

www. yahoo. com

www. google. com

www. mrcet.... com

cat urllist.txt | tr -d ' '
## OUTPUT
![312898870-de7ce8af-1855-4dec-99f3-734859a20a00](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/5f4bd05b-cbbf-4233-83e4-65aef6bdd135)
cat urllist.txt | tr -d ' ' | tr -s '.'


## OUTPUT
 ![312899242-255942df-5e83-4d32-b128-ee2fe540cebe](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/8a7259ee-0f46-4862-b9cd-4721c9d8d8c6)
#Backup commands tar -cvf backup.tar *
## OUTPUT 
![312900431-8c62851c-a964-43f2-86cc-74216fecdaf3](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/f1995523-039c-4bab-93ca-3c4fc400bc80)
cat << stop > herecheck.txt

hello in this world

i cant stop

for this non stop movement

stop

cat herecheck.txt
## OUTPUT 
![313092740-3eb2f341-b2a9-463b-9314-97f5a3971a76](https://github.com/sujigunasekar/OS-Linux-commands-Shell-script/assets/119559822/d39be17a-18da-4c6d-9ba1-3cbe6809b696)


# RESULT:
The Commands are executed successfully.
