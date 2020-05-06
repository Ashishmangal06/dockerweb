# dockerweb
Hello everyone.
This is a project which would automate everything after developer commits code in GIT
Prerequities: **GIT , Docker, ngrok and Jenkins** should be pre installed
Create new file after each major step

**How to deploy the project**
1) In GIT bash go to Your project_folder/.git/hooks//
2) create post-commit file and copy paste data from post-commit
3) In github set up hooks.
4) a. Copy paste code of Master1
   b. Set trigger to **GitHub hook trigger for GITScm polling**
   c. Save
5) a. Copy paste code of Master2
   b. Set trigger to **Build after other projects are built**
   d. Set project to watch as Master1
   c. Save
 6) For test1 and test2 repeat steps 4 and 5 respectively
 7) In sourcecode management
    a. Select git 
       Provide Repository URL and Credentials of github
       In additional behaviour select merge before build and provide necessary details
    b. Set trigger to Trigger builds remotely and provide Authentication Token
    c. In Post Action Build goto Git Publisher 
       Select Push Only If Build Succeeds and Merge Results options
       Put necessary details in Branches option
  8) Refer ss for further clarifications

Step 1 and 2 are used for auto pushing just after commit automatically.
Step 4 is used to copy the files of repo in linux
Step 5 is used to launch docker and share it to docker
Step 7 is used when Quality Assurance Department gives green signal to run the code in productiom world.
In this step secondary branch will merge to master branch

