# Lab Report 4

## Step 4: Log into ieng

<img width="570" alt="Screen Shot 2023-05-21 at 8 47 50 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/4ab1d1b5-214f-4bdd-89c5-75b81b75a973">

<img width="533" alt="Screen Shot 2023-05-21 at 8 48 13 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/32b8ee32-0482-4fc7-9c6f-a36538b1aec8">

**Keys:** `<CTRL + R> s <ENTER>`

For this step, as I had already previously set up my SSH keys, removing the need of entering a password when logging in, I just needed to search my command history using `<CTRL + R>` for "ssh", which brought up the correct command of `ssh cs15lsp23rb@ieng6.ucsd.edu`. From there, I just hit `<ENTER>` so that the command would run.

## Step 5: Clone your fork of the repository from your Github account

<img width="568" alt="Screen Shot 2023-05-21 at 9 07 17 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/516cbe14-a471-467a-ae55-f86e2c94730b">


<img width="564" alt="Screen Shot 2023-05-21 at 9 07 31 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/795a7839-d972-4173-8e42-ca1812d58556">

**Keys:** `<CTRL + R> git <ENTER>`

Similar to the previous step, I used `<CTRL + R>` to search for "git", which brought up the correct command of `git clone https://github.com/cjcanaday/lab7.git` which is used to clone the lab7 directory. I once again hit `<ENTER>` to run the command.


## Step 6: Run the tests, demonstrating that they fail

<img width="564" alt="Screen Shot 2023-05-21 at 9 18 06 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/e3ff0480-7c2e-46cc-b663-753760c59ac9">

<img width="567" alt="Screen Shot 2023-05-21 at 9 42 18 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/6aff4fe4-2a3c-4cc9-944c-c18ab823bd29">



**Keys:** `cd l <TAB>`
           `<CTRL + R> javac <ENTER>`
           `<CTRL + R> java -c <ENTER>`
           
           
For this step, I began by moving into the `lab7/` directory, which we will be using to complete all commands going forward. I completed this by typing in `cd` followed by "l" and then `<TAB>` which autocompleted the line to `cd lab7/`, after which I hit `<ENTER>`. From here, I searched my command history using `<CTRL + R>` for "javac" to compile the relavent files for JUnit which brought up the correct command of ` javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` afterwhich I hit `<ENTER>`. Next, I searched using `<CTRL + R>` for "java -c" to run my JUnit tests, bringing up `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`, afterwhich I hit `<ENTER>` to run the the command. This showed that Junit was failing its tests.

## Step 7: Edit and fix code

<img width="569" alt="Screen Shot 2023-05-21 at 9 44 04 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/53d9a9d0-a046-4c84-ba29-928701b770d6">

<img width="574" alt="Screen Shot 2023-05-21 at 9 45 36 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/9ca84516-7341-4973-99f4-8269f1418b98">

**Keys:** `vim L <TAB> .j <TAB>`
            `<UP> (6 times) <RIGHT> (12 times) i <BACKSPACE> 2 <ESC> :wq`
            
            
In order to fix this error, I needed to edit "ListExamples.java" which I did using vim by first typing "vim" and then "L" followed by a tab to autocomplete, and then ".ja" followed by another tab to autocomplete. This yielded the command: `vim ListExamples.java`, which I then pressed `<ENTER>` to run. This opened the file using vim, with the cursor starting at the very bottom left. To reach the point of the bug, I pressed the up arrow 6 times, followed by the right arrow 12 times. Now over the part I wanted to change, I pressed "i" to enter the editing mode, `<BACKSPACE>` to remove the erroneous 1, "2" to correct the bug, `<ESC>` to exit editing mode, and then finally `:wq` to exit and save the file.


## Step 8: Run the tests, demonstrating that they now succeed

<img width="575" alt="Screen Shot 2023-05-21 at 9 46 24 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/e62a4861-88fd-42da-8607-bb52be8c24a1">

**Keys:** `<UP ARROW> (3 times) <ENTER>` `<UP ARROW> (3 times) <ENTER>`

Now back at the terminal, I pressed the up arrow 3 times to return to the ` javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` command. I then pressed the up arrow another 3 times to get to the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` command, pressing enter after both of these commands. This displayed teh Junit result that all tests had passed.

## Step 9: Commit and push the resulting change to your Github account
<img width="573" alt="Screen Shot 2023-05-21 at 9 54 10 PM" src="https://github.com/cjcanaday/labreport4/assets/40177716/5c86fb22-f4aa-4b28-9e46-6787f8df2d05">

**Keys:** `git add ListExamples.java` `git commit -m "Fixed ListExamples.java"` `git push`

Finally, with all bugs fixed, I wrote out the command `git add ListExamples.java` to add the file "ListExamples.java" to the staging area. From here, I wrote out `git commit -m "Fixed ListExamples.java"` in order to commit the changes I made to be ready to be pushed to the main branch on Github. The -m flag I included allows for me to include a message detailing what is in the commit. For the final step, I wrote `git push` to update the branch with changes I committed, now showing on GitHub.
