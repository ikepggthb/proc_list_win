# proc_list_win
A very simple code written in c language to get a list of processes on Windows

# Example

``` c
#include "proc_list.h"

int main(){
  app_list_s list;
  
  new_proc_list(&proc_list);
  
  get_process_list(&proc_list);
 
  del_proc_list(&proc_list);
  
  return 0;
}
```

# About the app_list_s structure


``` c

typedef struct APP_LIST {
    size_t count;
    char** names;
} app_list_s;

```

```
count - The number of processes (size_t)

names --- process name (char *)
       |
       |- process name (char *)
       |
       |- process name (char *)
       |
       .
       .
       .
```
