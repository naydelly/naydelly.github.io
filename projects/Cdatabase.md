---
layout: project
type: project
image: img/bank3.png
title: "Bank Database Application in C"
date: 2024
published: true
labels:
  - C
  - Vim
summary: "I developed an application that manages a bank's records for ICS 212 - Program Structures using C."
---

<div class="text-center p-4">
  <img width="200px" src="../img/bank2.png class="img-thumbnail" >
</div>

This program serves as a bank record management system. I programmed both the database and the user interface of the application. The user-interface displays a menu of options that a banker can choose from to manage the bank's records. The UI takes in input and displays records. The UI calls functions from the database. Some of the essential functions I wrote for the database include the addRecord, deleteRecord, findRecord, and printAllRecord functions. The database also has functions that read from and write to record files, allowing records to be saved after exiting the program.

This project heavily emphasizes the use of pointers and structures, which are the foundations of the database. This project demonstrates the use of Makefiles to execute the program.

Below is an example of one of my database functions, findRecord, which finds and displays a bank record given the account number.

```c
int findRecord (struct record * start, int uaccountno)
{   
    struct record * temp = start;
    int success = 1;
    
    if (start == NULL)
    {   
        success = -1;
    }
    
    while (success == 1 && temp != NULL)
    {   
        if (uaccountno == temp->accountno)
        {   
            printf("Account Number: %d\n", temp->accountno);
            printf("Name: %s\n", temp->name);
            printf("Address: %s\n", temp->address);
            success = 0;
        }
        else if (temp->next != NULL)
        {   
            temp = temp->next;
        }
        else
        {   
            success = -1;
        }
    }
    if (debugmode == 1)
    {   
        printf("\n-debugmode-\nFunction called: findRecord()\n");
        printf("int uaccountno: %d\n", uaccountno);
        printf("Return value: %d\n\n", success);
    }
    return success;
}

```
