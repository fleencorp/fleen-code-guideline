### Description

When you clone a project through [https://github.com/fleencorp/fleen-code-guideline/blob/main/HOW_TO_CLONE_REPO.md](HOW TO CLONE REPO GUIDE)
You need to **download and install the dependencies** of the application before you can run the application.

When you clone the **Fleen Corp** project, you need to do some authentications before you can download dependencies like https://github.com/fleencorp/api-service
API-Service is a Github package that contains reusable codes found in FC Projects.

The first thing you need to do open the .m2 folder on your system's folder.

**.m2 folder** is where all your Maven projects dependencies are stored, Just like **node_modules** for Node.js projects.

**For Windows:**
You need to show hidden folders before you can be able to find the .m2 folder because folders that have a **.** are hidden by default. You can change this settings from your control panel.
You can go through this https://support.microsoft.com/en-us/windows/show-hidden-files-0320fe58-0117-fd59-6851-9b7f9840fdb2

1. Open
   - Command Prompt (CMD) on Windows
   - Terminal on Linux or MacOS

2. You can use the
    ```ls``` to see the files in a folder on Linux or MacOS
    ```ls -a``` to see the files in a folder including the hidden ones like **.m2** on Linux or MacOS
    ```dir``` to see the files in a folder on Windows. Hidden folders are visible automatically with ```dir``` command

4. Open the .m2 folder like
    ```cd ~/.m2``` for Linux or Mac OS
    ```cd C:/Users/John/.m2``` for Windows

5. Check if there is a file called **settings.xml** using
     ```ls``` for Linux or Mac Os
     ```dir``` for Windows


<img width="1512" alt="Screenshot 2024-09-09 at 12 48 47" src="https://github.com/user-attachments/assets/ff2e641e-c7d3-4aef-92aa-692c377aee3c">


<br/><br/><br/>
7. If there is no file, create a file in the **.m2** folder called **settings.xml**, make sure the file extension **is .xml and not .txt**
8. Then paste the followings in the file
<br/><br/><br/>

```
<?xml version="1.0" encoding="UTF-8"?>
<settings
    xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.1.0 http://maven.apache.org/xsd/settings-1.1.0.xsd"
    xmlns="http://maven.apache.org/SETTINGS/1.1.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <servers>
        <server>
            <id>github</id>
            <username>username</username>
            <password>token</password>
        </server>
    </servers>
</settings>
```
<br/><br/><br/>
9. If the **settings.xml** already exists, look for the **<servers>** tag and **add just**
<br/><br/><br/>

```
        <server>
            <id>github</id>
            <username>username</username>
            <password>token</password>
        </server>
```

**```so it will now be <servers><server>.......</server></servers>```**

<br/><br/><br/>
10. Replace the **username** part with your **Github username** and the token part with the **Github Personal Access Token** you created earlier.
```
    - The Github username is case sensitive, if your username is written as **John** like https://www.github.com/John, then you've to type it like that, if it is written as john.
    - In the image below, the username is volunux and not Volunux
```
  
<img width="433" alt="Screenshot 2024-09-09 at 12 44 40" src="https://github.com/user-attachments/assets/3d2c176a-d7a5-4965-a24c-781afd121171">


<br/><br/><br/><br/>
11. Save the file and confirms **there is a file called settings.xml in the .m2 folder**

<img width="1512" alt="Screenshot 2024-09-09 at 12 48 47" src="https://github.com/user-attachments/assets/bc32439d-9edb-475d-8f41-3bc847eba97f">


<br/><br/><br/><br/>
12. Navigate to the Fleen project folder you cloned earlier.

<br/><br/><br/>
13. Run the following to clean the cache
    - ```mvnw clean``` on CMD for Windows
    - ```./mvnw clean``` on PowerShell for Windows
    - ```./mvnw clean``` on Terminal for Linux or MacOS

<img width="1512" alt="Screenshot 2024-09-09 at 12 53 48" src="https://github.com/user-attachments/assets/a746192d-b506-47c5-9ac1-f56eae1bb6b4">


<br/><br/><br/>
14. Run the following to download all the dependencies for the project.
    - ```mvnw install``` on CMD for Windows
    - ```./mvnw install``` on PowerShell for Windows
    - ```./mvnw install``` on Terminal for Linux or MacOS

<img width="1512" alt="Screenshot 2024-09-09 at 12 54 33" src="https://github.com/user-attachments/assets/ab37cd0b-67a9-40f5-a959-719199f0dd93">


<br/><br/><br/>
15. If there are secret or environment keys, ask your co-worker or team lead and also how to set the keys
16. If you've like a script file that sets the keys for example ```script.sh``` for Linux or MacOs or ```script.bat``` for Windows
17. Run the script using
    - ```script.bat``` on CMD for Windows
    - ```source ./script.sh``` on Terminal for Linux or MacOS


<br/><br/><br/>
16. Run your application with
    - ```mvnw spring-boot:run``` on CMD for Windows
    - ```./mvnw spring-boot:run``` on PowerShell for Windows
    - ```./mvnw spring-boot:run``` on Terminal for Linux or MacOS



<img width="1512" alt="Screenshot 2024-09-09 at 12 57 08" src="https://github.com/user-attachments/assets/481d9fe6-ab31-42e4-ac19-a0d811899050">

