#Here The event will occurs in s3 bucket i.e tsstukaram. In tsstukaram there is an two subfolder i.e emp and dept. whenever the event occurs in dept the first lambda will trigger that event and 
it will find out the no. of object from emp and 
dept subfolder.If count is same in both subfolder then it will invoke the lambda function.same thing will happen with emp subfolder. wheneveer event occurs in emp bucket 2nd lambda will trigger that 
the event and it will
find out the count both emp and dept subfolder. If the count will same it will invoke the 3rd lambda function and it will start the execution step function.In step Function
It will start the first crawler. after the starting of first it will get state of of that crawler. if it is in running it will weat for 5sec after that when crawler is in ready state it will start the second
crawler and it will get the state of second crawler.If it is running state it will weat for 5sec. after crawler is in ready state. then Athena start query execution. it is as sync means we have to e to mark the complete task in athena start query execution.
After that athena get query execution. FInally what evevr result will get it will send to respective mail id with the help of SNS.
