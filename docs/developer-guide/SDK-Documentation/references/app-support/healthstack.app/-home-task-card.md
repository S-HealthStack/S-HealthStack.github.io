
[App-Support](../../app-support.html) > [healthstack.app](index.html) > [HomeTaskCard](-home-task-card.html)



# HomeTaskCard



[androidJvm]\




@Composable



fun [HomeTaskCard](-home-task-card.html)(title: [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html), state: [TaskViewModel.TasksState](../healthstack.app.viewmodel/-task-view-model/-tasks-state/index.html), onReload: () -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = { }, onStartTask: (Task) -&gt; [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) = { })



A composable function that displays a card view for a list of tasks.



## Parameters


androidJvm

| | |
|---|---|
| title | the title of the card. |
| state | the state of the tasks. |
| onReload | a callback function to reload the tasks. |
| onStartTask | a callback function to start a task. |




