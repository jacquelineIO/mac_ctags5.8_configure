mac_ctags5.8_configure
======================

Configure wrapper for exuberant ctags-5.8, using 10.7.5 OX Lion

Wrapper to run the conifgure for ctags-5.8, place  this script in 
ctags src directory and run. First change mode to execute and do the following:
  cp my_configure ctags-5.8/
  cd ctags-5.8/
  ./my_configure


This corrects errors such as:
  Missing lib...
  configure:2315: gcc    conftest.c  >&5 
  ld: library not found for -lcrt1.10.6.o

  Cannnot find include files...
  conftest.c:10:19: error: stdio.h: No such file or directory
  109 conftest.c:11:23: error: sys/types.h: No such file or directory
  110 conftest.c:12:22: error: sys/stat.h: No such file or directory


Apparently, once you get the include and library errors straight you do not run
into the /lib/cpp No such file or directory error that I was having, 
but my_configure is setting the CPP variable either way.






