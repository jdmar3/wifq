#  Welcome to Wifq v0.1!

Copyright 2011 John D. Martin III
http://youcantmakemistakes.com

# License

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

# Notes

Please note that there are two scripts available. 'wifq' has some
unicode characters which do not work in some terminal environments. If
you are not able to see the 𝛽 [beta] character, then instead use
'wifq-nu,' which is free of unicode characters in the script.

There is no need to install this script. You may simply run it in any
terminal using a bash shell. You may have to make it executable first 
if it is not already. To do so type the following while in the 
directory to which you extracted the files:

> `chmod +x wifq`

If you put the script in a PATH available to your user (e.g. -
/usr/local/bin in most Linux distros) then you can invoke the script
like any other program.

Example:
> `wifq 3 1 15`

If you wish to just run the program from anywhere, provided it is
executable and you have suitable permissions, then add ./ in front.

Example:
> `./wifq 3 1 15`

See below for usage instructions and further explanation. The help text
as below can be invoked by running the program with '-h' or '--help'

# Usage

Usage:	wifq [n] [𝛽] [S] ...
alias vncstart='screen -dmS "vnc-server" x11vnc -forever -usepw -ncache 10 -httpdir /usr/share/vnc-java/ -httpport 5800'
	wifq ...
Derive values for use in the construction of a magic square of any size
n x n.
Example:	wifq 3 1 15

  -h, --help			Displays this help screen. 
      --readme			Displays the README for the program.

If no values or invalid values are supplied in the command, the user 
will be prompted for values. 
Example:	wifq
		... 
		Please enter a value for n: ...

The input values correspond to the square as follows:

   n	: the 'size' of the square or the number of elements on a given 
		side
       𝛽	: the increment of the sequence of elements within the square
   S	: the 'magic constant' of the square or the sum of any row, 
		column ordiagonal

The following equation describes the relationship between these values:

   S = A + (𝛽 * n/2)(n^2 - 1)

The script tests whether or not the square is possible and then 
caluculates the following values:

   A	: the value of the lowest sequential element in the square
   Amin	: the same value as A
   Amax	: the value of the highest sequential element in the square
       𝜎 	: the sum of Amin and Amax
   T	: the sum of all elements in the square
   T+S	: the sum of three rows OR columns and one diagonal
   T*	: the sum of all rows AND columns AND both diagonals

The script in its current state does NOT output the arrangement of the 
magic square itself.

This script will find a set of values related to the construction of a 
'magic square' according to parameters derived from the works of 
Abu-l-'Abbas Ahmad b. Ali b. Yusuf al-Qurashi al-Buni (d. 622H/1225AD) 
and other sources and developed by Prof. Saiyad Nizamuddin Ahmad into 
a set of equations. His equations were used to develop the algorithms 
utilized in this script. wifq

For further information,  see al-Buni, Manba' Usul al-Hikma, Cairo: 
Mustafa al-Babi al-Halabi, ND.

Report bugs to: john.d.martin.iii@gmail.com

Visit the author's website: http://youcantmakemistakes.com

This is version 0.1.

Copyright 2011 John D. Martin III

