
## Overview

I have two subprojects that contain multiple tasks.

I want to create task named `rootTask` that run all the subprojects tasks.

but when I using `tasks.register` then dependsOn of `rootTask` it seems not working as expected.

## Reproduce steps

1. run `./gradlew taskRoot`

2. see the terminal results

   ```
   > Task :taskRoot
   taskRoot dependsOn: [task ':project2:myTask4']
   ```
   
## Expected results

   ```
   > Task :taskRoot
   taskRoot dependsOn: [task ':project1:task2', task ':project2:task3', task ':project2:task4'] 
   ```