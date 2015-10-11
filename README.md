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
     
![](https://raw.githubusercontent.com/AOMIDORI/Minix3-Function-Keys-mapping/19e50c3019c00e4d8033786f508d74a335b53bad/screenshot/keymap.png)
