<b><font size = "+3">Major Project 1</b></font>
    <br>
<b>ENGINE SHELL </b>


<b>Group 14: Anh Nguyen, Olufemi Olumaiyegun, Sena Moon</b>

This is our shell program called engine that implements our built-in commands such as alias, exit, and history. 

<b>Organization of the project</b>
<br>
The project was split into multiple components for effective division of labor. Sena Moon assumed the role of supervisor of the team and took care of dividing the labor.
Anh Tuan Nguyen was tasked with working on the alias function; Sena with the history function; Femi with the exit function and Curtis with path.
<br>
We used MS Teams for organizing and setting tasks and deadlines while also serving as a temporary file storage before uploading to GITlab.
<br>
We used Groupme for urgent communication and planning and also communicated with each other and the instructor via email.
<br>
We used Zoom for collaborative meetings where we needed to work on code together.
<br>
Gitlab served as our code repository and version manager.
<br>
<br>
<br>

<b> Design Overview </b>
<br>
The code was split into three files:
<ul> 
    <li>One is the header file which contaisd all the function declaration and library inclusions.</li>
    <li>Another is the source file "engine_function.c" which contained all the function definitions.</li>
    <li>The last is the main file "main.c" which contains int main().</li>
    </ul>

A makefile as included for easy compilation.

<p><i>For our program to work as inteneded we needed to create a few functions to take care of processes that come up
frequently. These functions include:
<ul>
    <li>void parseLine(char* , char **): This parses user input in interactive mode. It stores the parsed input in a 2d char array.</li>
    <li>int execute(char** const): This handles parent processes, forking, child processes, error handling when command is invalid, and killing processes.</li>
    <li> void signalHandler (int): This handles ctrl z and ctrl c signals and makes sure they do not quit the shell.</li>
    <li>void addHistory (char **, char*, int): This function handles the history operation related to adding commands to history.</li>
    <li>void printHistory(int, char**): This functions prints all the commands to screen when it is called by the user.</li>
    <li>void findHistory(int,char**): This function finds the nth  user command where n is an integer value.</li>
    <li>void deleteHistory(char**,int): This deletes the history of all commands given by user until the command is executed.</li>
    <li> void executeHistory(char **, int): This function executes the nth command that was given by the user where n is the position of the command in history.</li>
    <li> char* getAlias(char *ext): This function works with alias.</li>
    <li> void exit1(): This function exits the shell. </li>
</ul>
</i>
<br>
<br>
<b> Known Bugs </b>
<ul>
<li>alias throws a core dumped at certain times.</li>
<li>path code is not included since it was not delivered by Curtis.</li>
</ul>


<b>How to run </b>
<ul>
<li>using a terminal with a gcc compiler 'cd' into directory where files are saved.</li>
<li>type 'make' into terminal.</li>
<li>type './engine' and run in terminal to access interactive mode.</li>
<li>type './engine <i>filename</i>' and run in terminal to access batch mode. filename is the name of the file containing all the commands to be run in batch mode.</li>
