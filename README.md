# Minix3-Function-Keys-mapping
Map the Shift+F7 to displaying how many processes are currently running

  1. Modify the "dmp.c" file (/usr/src/servers/is/dmp.c). Find the struct hook_entry.
  
     Add one hook entry (e.g. {SF7, pscount\_dmp, "Display how many processes are running" }) into it.


  2. Modify the "dmp_kernel.c" file (/usr/src/servers/is/dmp_kernel.c).
    
     Add the pscount\_dmp function into it. Add include "../pm/mproc.h".

  3. Modify the "proto.h" file (/usr/src/servers/is/proto.h). Add "void pscount_dmp(void);" to it
  4. cd /usr/src
  5. make build
  6. reboot
  7. Try to press Shfit+F5, and Shift+F7 :)
     
![](http://b.picphotos.baidu.com/album/s%3D1100%3Bq%3D90/sign=a86cddab364e251fe6f7e0f997b6f266/b3fb43166d224f4ac9fc0c820ff790529822d13e.jpg)
