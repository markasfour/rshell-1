# rshell
command shell written with cpp

## How to Build and Run
in rshell folder, type `make` to build and type `/bin/rshell` to run 

## Known Bugs
cd command does not work 

## Connectors 
Connectors are `&&` `||` and `;`.
They work form left to right.
<table>
	<tr>
    		<th>Connector</th>
	    	<th>Usage</th>
	</tr>
	<tr>
		<td>&&</td>
		<td>right of connector will run only if left succeds</td>
	</tr>
	</tr>
		<td>||</td>
		<td>right of connector will run only if left fails</td>
	</tr>
	<tr>
		<td>;</td>
		<td>right of connector will run no matter what</td>
	</tr>
</table>

## Quitting Program 
The program can be exited with the exit command.
It will work with connectors. 
If command has and characters trailing or leading it will not work. 

##Bugs
Program will always be in english.
Program does not tell you what commands you inputed when wrong.

##Edge
If nothing is put before the connector, if is assumed to be false.
|| [command] assuming command is a valid bash command, it will run. 
&& [command] command will not run 

#ls
ls program from unix rewritten in cpp it lists files and dir.

##Building and Running
Just type `make` to build or `make ls` to only compile ls.
Type `bin/ls` to run followed by flags and/or files/dir.

##Flags
Currently my ls program only supports the flags -R -a and -l.
You can type them in after a (-).
There must be no extra spaces.
It has to be after the (-) or ls will act as if it is a dir or file.
You can add multiple flags with extra (-) followed by the flag followed by a space and another (-) followed my a flag.
ie -a -R
You can also add other flags after the previous flag as long as there are no spaces.
ie -aRl
You can repeat the same flags without error. 
ie -aaaaaRlaa

##Folders and Dir
You can add a folder or a directory after ls or after flags.

##Bugs
My ls program is in alphabetical order while unix ls program is in different order

##Edge
You can combine flags and files or dir. 
You can add flags then dir or dir then flags. 
You can even have flags followed by a dir followed by more flags.
ie ls -a ~/ -R .. -l
If a flag is not valid, ls will not output anything.
