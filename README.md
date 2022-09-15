# CSCI 201 FALL 2022
Lab 3 Starter Code:

None!

Welcome to GitHub and your third CS201 Lab!

### Learning Goals:
- perform more advanced computations
- use methods to make our main method more readable
- structure output in an easy to read way



## Lab 3

### Creating a .java file

Program are written in .java files and compiled into .class files.
1) Click the arrow next to the Lab1 folder in the Project Viewer Pane. This will expand the project folder.
2) Write click on the `src` folder and navigate to `New`. Click `Java Class`. When prompted for a name, name the class `Lab3`.

The Text Editor Pane will now contain a page with the following:

```
public class Lab3{
}
```

Your program should:
- prompt the user for a number of seconds.
- pass the entered number of seconds to a method called `secondsAnalyzer` which performs the following task: convert that number of seconds to the amount of weeks, days, hours, minutes, and leftover seconds that is. It does NOT convert the entire amount to each, but the total quantity. For example 3600 seconds is 1 hour so your program would display:
- the secondsAnalyzer method should return the String generated to the main method where it can be printed. 

Below are some examples:

```
Enter a number of seconds: 3600
3600 seconds is 0 weeks, 0 days, 1 hours, 0 minutes, and 0 seconds
```

OR

```
Enter a number of seconds: 137
137 seconds is 0 weeks, 0 days, 0 hours, 2 minutes, and 17 seconds
```

Note: you should never have more than 59 seconds since that would just give you another minute. 

**Implementation Tips:**

***The `main` method:***

The main method should only do 3 things:

1) prompt the use for a  number of seconds, allow them to respond, and store the value as `enteredSeconds.`
2) pass this value to the `secondsAnalyzer` method which will return a string.
3) print the string that is returned from `secondsAnalyzer.`

***The `secondsAnalyzer` method:***

In the secondsAnalyzer method you'll pass a single integer parameter, call it `x`. 

You can create 5 integer variables `weeks, days, hours, minutes, seconds`

You can process the number of minutes using the division operator. Since the number of seconds will be known as `x` by the method, the number of minutes is the result of 

```minutes = x / 60;```

Since both are integers, this will return an integer value.

To find the leftover number of seconds after accounting for minutes, you can compute 

```seconds = x - (minutes * 60);```

Fun question: can you explain why this works?

Now, you can repeat this process with the number of minutes you have, converting it to `hours`, converting `hours` to `days` and converting `days` to weeks. 

Finally, you'll create a string which represents the data as desired: 

```java
x seconds is [weeks] weeks, [days] days, [hours] hours, [0] minutes, and [1] seconds
```

The `secondsAnalyzer` method should return that string to the `main` method where it can be printed.

Hint: If you're struggling with the math portion of this, just try converting to minutes and left over seconds first. Once that works reliably, shoot for hours. Once that works, work on days, etc. One step at a time making sure everything works as desired. 

### Submitting the project

When you're done, you can upload your files to this Repo and commit the changes. 

1) Click `Add files ` at the top right of the Repo page.

There are two options:

A) Click "Add Files" to create new Java files in the repo manually. Create new files with name `Lab3` You can re-type or copy paste your code into that file.

B) Click "Upload Files" to just upload the .java files you already created. Navigate to the `src` folder on your computer and upload `Lab3.java`.

2) Once you've created the file you want, or uploaded them, navigate to the bottom of the Page and hit "Commit changes". Ensure "Commit directly to the `main` branch." is selected. You'll need to "Commit changes" once for each file you "Create" in GitHub, but can upload multiple files before a single Commit. 


