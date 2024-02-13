# proc_list_win
A very simple code written in c language to get a list of processes on Windows

# Example

``` c
#include "proc_list.h"

int main(){
  app_list_s* list;
  
  new_app_list(list);
  
  get_process_list(list);
  
  // print
  for(int i = 0 ; i < list->count; ++i){
    printf("%s\n",list->names[i]);
  }
 
  del_app_list(list);
  
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
count - Number of processes (size_t)

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
