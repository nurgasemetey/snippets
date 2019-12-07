### group by duplicate rows in dplyr 


[r - group by duplicate rows in dplyr - Stack Overflow](https://stackoverflow.com/questions/45254087/group-by-duplicate-rows-in-dplyr "r - group by duplicate rows in dplyr - Stack Overflow")


 

```R
x %>% group_by(Ship_No) %>%
    filter(duplicated(Number)) %>%
    summarize(Number = paste0(unique(Number), collapse = ','))

```
