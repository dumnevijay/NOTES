This is the notes made by vijay about the linux commands from the youtube class of tech with jatin.

i am using vi editor to edit txt file used for heavy files and better save options

( cat tac head tail commands)
cat
	multi purpose command used to see file edit file (when the file have less lines use cat to open file)
 
cat f1.txt 
	to show the file content in the terminla.
 
cat > f2.txt
line1
line2
ctrl+D
	this command will create the new f2.txt file and write the line1 and line2 in that file.
 
cat f1.txt f2.txt 
	this is used to see multiple file contents such frist f1.txt content then f2.txt content.
 
cat f1.txt >> f2.txt 
	to append f1.txt content into the f2.txt file.
 
cat -n f1.txt
	show file content with line numbers.
 
tac f1.txt
	show file content in reverse order.
 
head f1.txt 
	to show only initial 10 lines out all lines.
 
tail f1.txt
	to show only last 10 lines out all lines.
 
head -n 20 f1.txt
	to show only initial 20 lines. shows lines which we give after -n.
 
tail -n 25 f1.txt 
	to show only last 25 lines. shows lines which we give afer -n.

(copy move commands)

cp f1.txt f3.txt
	this will copy f1.txt content and create new f3.txt file in the current folder as we did gave any path and copy the content into that file.
 
cp -r app/ demoapp
	this will copy all files and folders present in the app folder and create new demoapp and paste them in that.
 
cp filename.txt /c/Users/admin/Desktop
cp filename path
	this will copy the file to that particular path
 
cp filename.txt /c/Users/admin/Desktop/newfile.txt
	this will copy the filename.txt content to newfile.txt use this to copy to particular path.

mv filename or folder/ path

mv file.txt /c/Users/admin/Desktop
	this will move file.txt to the specified path.
note : if folder name is new Folder then type as new\ Folder in terminal to copy or move something to this folder other wise it will them as separate folders or show name error.

mv file.txt ../ 
	this will move the file to parent folder her to Desktop is parent folder.
 
mv file.txt file1.txt
	to rename a file this will create new file file1.txt and move content of file.txt to file1.txt then it will delete file.txt.

( grep golbal regular expression print this will look into the file content used to find particular word or pattern in a file.)

grep "vijay" names.txt
	this will look for vijay word or pattern present in the names.txt file. this is case sensitive.
 
grep -i "Vijay" names.txt
	this is not case sensitive.
	if the pattern or word is not present then it will not show anything.
 
grep -li "vijay" *.txt
	this will look for vijay in all .txt files in the current folder. l stands list i stands case insensitive * stands for all.
 
grep -ci "vijay" *.txt
	this will return count of word in all .txt files it shows count after the filename. c stands for count.
 
grep -ci "vijay" *.*
	this will return count of word in all format files.
 
grep -v "vijay" names.txt
	this will show all content of names.txt except the vijay word.

nos.txt contains
1
2
3
4
5
6

grep -A 2 -i "2" nos.txt
	this will print 2 3 4 prints 2 more data after given input data.
 
grep -B 2 -i "3" nos.txt
	this will print 1 2 3 prints 2 more data before given input data.
 
grep -C 2 -i "3" nos.txt
	this will print 1 2 3 4 5 prints 2 more data before and after given input data.
 
grep -i "shah" names.txt
	this will find pattern then return like shahrukh.
 
grep -wi "shahrukh" names.txt
	this will try find exact word in the file.

( find this will see same names of folders or names of files not the content )

find . -name "*.java"
	this will look for .java files in the child folders.
 
find . -name "name"
	this will look for name folder in the child folders.
 
find . -type d
	this will show all directories and sub-directories in the child folders and print them.
 
find . -type f
	this will show all files and sub-directories files in the child folders and print them.

( sort )

sort filename.txt
	to sort in ascending order.
 
sort -r filename.txt 
	to sort in descending order.

hisory 
	this is used to all previous commands used in the terminal.
