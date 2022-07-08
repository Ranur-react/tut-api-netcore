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


5. #### Create Folder Context and make an MyContext.cs File for Entity Framework can be build tables autoamte by the MyContex Script.

    * Before MyContext.cs Script creating in this Context folder, we're must have a few Nuget plugin :


        ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.12.41.png)
        ![alt text](./img/Screen%20Shot%202022-07-04%20at%2021.46.29.png)
        You can install they plugin in the Toold -> Nuget Package Solutions -> Browse, and they plugin it must still install on the old version (V. 5.0.11)
    * After Their plugin had install u can try create MyConetext.cs Files and typing this code in this File looks like this bellow:
         ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.18.02.png)

6. #### Configurations Database Connections and Startup.cs configurations.

    * Set appsetting.json file to be can connect with database MS. SQL Server by API variable configurations look like bellow of:
      ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.31.03.png)
    * After App setting Json was configure, you can try set MyContext as Context configurations sql server by Startup.cs files looks like bellow:
     ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.27.30.png)


7. #### type migration command in to NuGet Pacakage Console looks like bellow:

    ```
        add-migration 'lable migrations'
    ```

 ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.34.25.png)

 make sure migration success looks like that bellow:
  ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.37.20.png)

8. #### after type migration command we must typing 'database-update' to be implement entity database firsth code into real database our have:

        ```
        > update-database
        ```

  ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.39.32.png)

  make sure command succcss looks like that bellow:

  ![alt text](./img/Screen%20Shot%202022-07-04%20at%2022.42.12.png)

8. #### After this migration affected to databse we can show of the database have several tabel like what i write in the models as entity. 

 ![alt text](./img/Screen%20Shot%202022-07-07%20at%2018.40.35.png)

8. #### Migration Entity by Automate Framework has ben clear, next you can continue with CRUD API.

------
Crud Configurations
----------

9. #### Create Folder Repository on this Project 

10. #### Create Folder Interface on this Project
11. #### Create Interface File for Entity Data 
    * Create Interface File for Employee with Names "IEmployeeRepository.cs".
    * TYpe on this files like thi bellow
    


