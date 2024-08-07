# OpenLogs
A Powerfull Project managing DSL (Domain Specifig Language) Designed for small and bigger project management with ease!

This also allows you to write projects with ease and quickly backing up your projects! Isn't it good ?

Not only this but it allows you to customise the language if you knew C++ and your open contributions are also good for improvements

# Tutorial
Starts with file extension - Open Logs doesnot has a fixed file extension but an OpenLogs code can be intepreted in any file format but commonly we uses .openlog for better file management.

## Macros
OpenLogs has inbuilt macros which are too powerfull for file and project management let's explore those 

### remove: (Macro)
<code>remove:</code> is an inbuild macro of OpenLogs which is used to remove the conent from any file without physically deleting it.

For example : I want to remove the content of a.txt or completly wipe out the data of a.txt so i can write
```OpenLogs
remove:a.txt
```

### updated: (Macro)
<code>updated:</code> is an inbuild macro of OpenLogs which is used to add the updated file to the updated directory of OpenLogs which can be furture used for many purposes including backups

For example : I want to store the a.txt file as updated file which further i can restore as backup so i can write
```OpenLogs
updated:a.txt,a.txt
```

Here i used a comma with another a.txt because <code>update:</code> macro takes two values 1 for the file path which must be stored and 2nd is the stored file path which will be stored as main file and even if the names are different you do not need to worry because OpenLogs manages everything for you

Another example : I want to store a.txt as updated with the name of b.txt i can do this by
```OpenLogs
updated:a.txt,b.txt
```

## Odems
Odems are the keywords which are used to perform certain actions based on there work! Odems do not takes any value but they performs certain actions

### UPDATE_FILES; (Odem)
<code>UPDATE_FILES</code> is used for updating all the files which are stored as updated files and even if there names are different still we can use <code>UPDATE_FILES;</code> Odem will still update the files bacause OpenLogs keeps the track of orignal files.

Example : I lost my a.txt but i knew that it was stored as b.txt in previous example as updated so i can backup it by
```OpenLogs
UPDATE_FILES;
```

# Note :
Use remove:updated/UPDATE_LOGS at the begning of the OpenLogs file as it is a good practise which cleans the UPDATE_LOGS file before appending new things to it. But only do this if you are going to repeteadly use single OpenLogs file because it wipes the UPDATE_LOGS file which contains the track of all the updated files with there uodated and orignal names and these can be used for backups.

# A Demo Project
```OpenLogs
remove:updated/UPDATE_LOGS
updated:a.txt,updated-a.txt
updated:b.txt,b
UPDATE_FILES;
```

This example demonstrates a safe atmosphere for a and b text documents which are always updated and stored twice

Hope you enjoyed this.

OpenLogs v1.0
