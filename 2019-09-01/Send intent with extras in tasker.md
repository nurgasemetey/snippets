### Send intent with extras in tasker


[\[Request\] Intent for Tasker to Perform a Task? : tasker](https://www.reddit.com/r/tasker/comments/52ru8l/request_intent_for_tasker_to_perform_a_task/)




```shell
Simply use send intent with action "myaction", target broadcast receiver and in the extra task:mytaskname. Then in the intent received Tasker side, you can create a condition with action "myaction" and you should have the variable %task containing mytaskname, you can use the name to perform the task.
```
