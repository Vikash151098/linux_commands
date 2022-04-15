# linux commans bellows:-

```sh 
pwd- show current path
cd - change directory e.g. cd .., cd ../.., cd foldername, cd ~
/ for root directory
~ for home directory

e.g. cd ~/Desktop
```

## Creating file and folder

```sh
mkdir /tmp/tutorial
cd /tmp/tutorial
mkdir dir1 dir2 dir3
mkdir -p dir4/dir5/dir6
ls
cd dir4
ls
cd dir5
ls
cd ../..
mkdir "folder 1"
mkdir 'folder 2'
mkdir folder\ 3
mkdir "folder 4" "folder 5"
mkdir -p "folder 6"/"folder 7"
ls
```

## Creating files using redirection
```sh
ls
ls > output.txt
cat output.txt
```
```sh
echo "This is a test"
echo "This is a test" > test_1.txt
echo "This is a second test" > test_2.txt
echo "This is a third test" > test_3.txt
ls
```
```sh
cat test_1.txt test_2.txt test_3.txt
cat test_1.txt test_2.txt test_3.txt
cat test_?.txt
cat test_*
```
```sh
cat t* > combined.txt
cat combined.txt
```
```sh
cat t* >> combined.txt
echo "I've appended a line!" >> combined.txt
cat combined.txt
```
```sh
less combined.txt
echo "Lower case" > a.txt
echo "Upper case" > A.TXT
echo "Mixed case" > A.txt
```
## Moving and manipulating files

```sh
mv combined.txt dir1
ls dir1
```
```sh
mv dir1/* .
mv combined.txt test_* dir3 dir2
ls
```
```sh
ls dir2
mv dir2/combined.txt dir4/dir5/dir6
ls dir2
```
```sh
ls dir4/dir5/dir6
cp dir4/dir5/dir6/combined.txt .
ls dir4/dir5/dir6
ls
```
## Copy file and folder
```sh
cp combined.txt backup_combined.txt
ls
mv backup_combined.txt combined_backup.txt
ls
mv "folder 1" folder_1
mv "folder 2" folder_2
mv "folder 3" folder_3
mv "folder 4" folder_4
mv "folder 5" folder_5
mv "folder 6" folder_6
ls
```
## Deleting files and folders

```sh
m dir4/dir5/dir6/combined.txt combined_backup.txt
rm folder_*
rmdir folder_*
rm -r folder_6
ls

rm -i foldername or filename
```

## A bit of plumbing

```sh
wc -l combined.txt
```
```sh
ls ~ > file_list.txt
wc -l file_list.txt
rm file_list.txt
```
```sh
ls ~ | wc -l
```
```sh
ls /etc|wc -l
```
```sh
ls /etc | less
```
```sh
cat combined.txt | uniq | wc -l
```
```sh
cat combined.txt | uniq | less
```
```sh
man uniq
```
```sh
sort combined.txt | less
```
```sh
sort combined.txt | uniq | wc -l
```

## Super User 

```sh
cat /etc/shadow
sudo cat /etc/shadow
```
## Hidden files

```sh
cd /tmp/tutorial
ls
mv combined.txt .combined.txt
ls
```
```sh
cat .combined.txt
mkdir .hidden
mv .combined.txt .hidden
less .hidden/.combined.txt
```
```sh
ls
ls -a
ls .hidden
ls -a .hidden
```
```sh

tree
tree -a

```
```sh
rm -r /tmp/tutorial
ls /tmp

```
