# Assignment 1

## Exercise 1: Join GitHub Classrooms and Markdown (6 pts)

Create a GitHub account and join the [GitHub classroom](https://classroom.github.com/a/Nshauyhh).

Once the cloning process is done create a new file in this repository via the web interface. Use `introduction.md` as file name. For all .md-files of this assignment, use the markdown syntax ([markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)).

Inside the file, first enter the following information:

* **Name**: {your name here}
* **E-Mail**: {your smail address here}

Then, answer the following questions in a short text (at least 3 sentences each!):

1. Do you have any prior experience in the field introduced in the introductory session? If so, give a short overview on them.
2. What expectations or wishes do you have on the data modeling course?

Make use of some Markdown formatting like headings and lists when answering these questions, when appropriate.

Below the editor, leave the option "Commit directly to the master branch." checked and click "Commit new file".

## Exercise 2: The Unix Shell (6 pts)

### 2.1: Shell Tutorial
Complete the lessons from the interactive online course at [linuxjourney.com](https://linuxjourney.com/lesson/the-shell) on learning the command line. Do the quizes in each of the lectures.

Prove your completion with a photo that shows your student ID card and the correct results of the quizes. Make at least 3 photos according to the last three digits, of your student ID. Subtract these three digits from 10. For example: Your student ID is 1110341 -> Photos of quizes 7, 6, and 9, according to 10-3=7, 10-4=6, and 10-1=9. In case this rule of thumb does not work, calculate the sum of the double digits or last two digits. For example: Your student ID is 1110288 -> Photos of 8, 2 and 16 (8+8). 

### 2.2: Count the Lines
Use your new knowledge to count the number of lines in your `introduction.md` file from exercise 1.
Redirect the result to a file, e.g. `lines.txt`.
Print the content of the file to the console.

To submit your solution, copy the commands and their outputs from the shell (including prompt) to a new *markdown-formated file* `exercise2.md`. Make use of the markdown markup for verbatim code blocks to render it nicely in monospace font.

More on markdown-formatting can be found at this [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) from `adam-p` or the official [GitHub Guide to Markdown](https://guides.github.com/features/mastering-markdown/).

## Exercise 3: Git (10 pts)

1. Clone your own repository into your local file system.
2. Play around with the [git visualization tool](https://git-school.github.io/visualizing-git/) shown in the lecture. Create at least 5 commits, branches and tags there and watch the graph grow. (Hint: Typing help will show you all the available commands.)
3. Make a screenshot of your work when you’re finished. Save the screenshot on your machine to your working directory (where you cloned your repository into). Give the screenshot a reasonable filename containing your name and the exercise number, for example `schaer-ex03.png`.
4. On the command line:
  * navigate to the directory
  * check your git status
  * add the new file to git
  * and commit the change.
  * Finally, push your changes to the remote repository.
5. Visit your repository on GitHub to verify that your new file is present. 

## Exercise 4: Mine Twitch Data (12 pts)

Download the dataset [`data_twitch.zip`](https://github.com/irgroup-classrooms/dis08-2021/tree/main/datasets/data_twitch.zip) and unzip it.

The dataset consists of chat logs of the streaming platform twitch.tv.

Write a set of shell commands to do the following things:

1. Twitch Emotes
 * The first task consists of finding twitch emotes (platform-specific emojis, compare [on twitch emotes](https://www.twitch.tv/creatorcamp/de-de/learn-the-basics/emotes/). Print an overview of the number of lines per `.csv` file with occurrences of the terms `kappa` or `trihard` occures. These are two of the most popular emotes on twitch. Count all lines, in which at least one of those appears. 
 * In a separate command, count the total number of lines with occurrences across all files. 
2. Again for all files, search for occurences of `911` or `110` within the pseudo username column.  _Hint: Make use of the `cut` command and its delimeter option._
3. Count the number of lines that contain a chat message with at least 20 characters in all `.csv` files. _Hint: Check on the correct pattern with `grep`._
4. Print all usernames appearing in all `.csv` files into a new file `user_list.txt`.
5. Print an overview of unique usernames in all `.csv` files. _Hint: Make use of the `uniq` command._
6. Print all unique chat messages from all `.csv` files, sort them alphabetically and print the output to a new file `unique_comments.txt`.

Create a file `exercise04.sh` that will contain your solutions to the 6 tasks. Be careful with whitespace characters and restrict your submission to the tasks, there is no bonus points!

* First line has to be `#!/bin/bash`
* Each line contains a command to solve one of the tasks above OR A PART OF THE TASK. Although preferred, you DO NOT have to solvve the tasks in one line!
* We want to see one commit in GitHub per solution! (for clarification: JUST one, not one per sub task)

Additionally, create a text file `exercise04.md` and comment on each solution. To do that,

* copy your commands into the Markdown file,
* and explain what you did and why.
* we highly recommend to also show the output produced by the commands.

Push all commits to your repository.

## Exercise 5: Clean-up Disney Plus (16 pts)

In this exercise, you will be working with the dataset [`disney_plus_titles.csv`](https://github.com/irgroup-classrooms/dis08-2021/tree/main/datasets/disney_plus_titles.csv). The original data set can be found on [Kaggle](https://www.kaggle.com/shivamb/disney-movies-and-tv-shows?select=disney_plus_titles.csv). 

1. Document and describe the different data fields. (1 point)
2. Identify "dirty" data fields and clean them up. Use regex replace, spreadsheets or whatever you like, if you think it is required. Document your working steps in a file `exercise05.md`. Export your data set as a clean TSV file. Add both files to your repository. (2 points)
3. Analyze the data set using shell scripts and/or regex. Document the commands in an additional section in `exercise05.md`. (5 points)
    * Find the unique genres and the total number of genres in the Disney Plus catalogue. (1p)
    * How many movies, how many tv shows are available on Disney Plus? (1p)
    * What are the top 5 directors with the most movies (count only media with a single director)? (1p)
    * How many movies and shows have been produced at least partially in Germany? (1p)
    * How many movies with a play time of more than two hours can be found on Disney Plus? (1p)

Documentation is key! Everything that is **not properly documented** is not verifyable by us and will thus get **0 points**. Do not overdo your documentation either- we do not want to know about every click you performed! Complete and concise, please!

# Assignment 2

Form a team of 3-4 students. Give your team a cool name like [The Be Sharps](https://www.youtube.com/watch?v=CWbW1jtFQUo) or [The Blernsballs](https://www.youtube.com/watch?v=oQF8rQaIjUE&list=RDzfvpeVe_i1A)... You get the idea. 
When your team forming process is done, join the [GitHub Classroom](https://classroom.github.com/a/Dmj2sFOl) for assignment 2. Your team can then collaborate via GitHub.

## Exercise 1 (8 pts)

We continue with the Disney Plus data set and try to reproduce some of the exercises we did with shell and grep. Work with [Pandas](https://pandas.pydata.org/) when not stated otherwise! We will talk about Pandas in the upcomming weeks.

0. Read chapter 8 to learn more about reading and writing files. I skipped a lot of details.
1. Write a Python program: Read the Disney Plus data as a Pandas Dataframe.
2. Make your program extract a full list of all genre names that are listed in column "listed_in". Make sure to extract only the genres and clean the data from non-letter characters if necessary. Save as a list.
3. Extend your program to count the distinct (unique) genre names. 
4. Next, find how many entries in the disney plus catalog belong to each of the genres. Save the genres and corresponding counts in a dictionary. 
5. Write the results in a new CSV file that contains the genres and the counts. 
6. Count, save in a dictionary and export as a csv (like in 1-4) the occurances of the terms "Disney" and "Marvel" in the column description. Think about different name variations (like uppercase, etc.).

Commit your Python program and the resulting CSV files. 
