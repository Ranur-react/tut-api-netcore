### TUTORIAL PRODUCE AN API WITH .NET CORE V. 3.11

1. #### Create Project with tempalate "API Web And Console ASP.Net Core"
    ![alt text](./img/Screen%20Shot%202022-07-04%20at%2016.01.24.png)
2. ####  Select Framework Target 3.1
    ![alt text](./img/Screen%20Shot%202022-07-04%20at%2018.48.55.png)
3. #### Typing your Project names
    ![alt text](./img/Screen%20Shot%202022-07-04%20at%2018.49.26.png)
4. #### Create Model Folder and Model Files as Entity Schema for automatically migrations to database sql server.

    * View of Entity Relations Diagram Structure.
    
       ![alt text](./img/Screen%20Shot%202022-07-04%20at%2018.56.54.png)

    From this diagram we can assumptions the relations type entyty is "one two many" , one branch can using by many employees. if we're look from json side, we can conclusing the branch table object can be have much emplooyes and the employees table can have one by one branch data. 
    * And then, if we want implment this schema on the models we can try write anotaions on models like that picture:

        ![alt text](./img/Screen%20Shot%202022-07-04%20at%2019.40.12.png)

        ![alt text](./img/Screen%20Shot%202022-07-04%20at%2019.40.20.png)
