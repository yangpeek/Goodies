* [GDB reverse next](https://stackoverflow.com/questions/1206872/how-to-go-to-the-previous-line-in-gdb)

#### gdb load bid project failed on debian with 7.7.1
  * choose the version from: http://ftp.gnu.org/gnu/gdb/
  * [install gdb 8.2.1](http://www.gdbtutorial.com/tutorial/how-install-gdb)
  * make install failed at some: gdb-8.2.1/missing: makeinfo: not found
  * [sudo apt-get install texinfo](https://stackoverflow.com/questions/338317/what-is-makeinfo-and-how-do-i-get-it)
  * using: /usr/local/bin/gdb load the big binary success.
  * todo: gdb still goes to the default 7.7.1, need to figure out to replace it.
