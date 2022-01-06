# Assignment 1

This is a personal assignment. Each student has to compile his/her own results. The submission deadline is `2021-11-26, 20 pm`. All parts of assignment 1 are pre-released so that you can look ahead what's coming up in the next weeks. 

## Exercise 1: Join GitHub Classrooms and Markdown (6 pts)

Create a GitHub account and join the [GitHub classroom](https://classroom.github.com/a/Nshauyhh). If you can't find your student id in the classroom's list, please [file an issue](https://github.com/irgroup-classrooms/dis08-2021/issues). I just need your lastname and course of study. No student id in the public list of issues, please.

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

In this assignment, you will work together in groups on a larger project that builds over several weeks. 
The project will focus on getting data from the web, cleaning and writing data in Python.
The exercises will be posted in GitHub as usual.

Form a team of 3-4 students. Give your team a cool name like [The Be Sharps](https://www.youtube.com/watch?v=CWbW1jtFQUo) or [The Blernsballs](https://www.youtube.com/watch?v=oQF8rQaIjUE&list=RDzfvpeVe_i1A)... You get the idea. 
When your team forming process is done, join the [GitHub Classroom](https://classroom.github.com/a/Dmj2sFOl) for assignment 2. Your team can then collaborate via GitHub in its own repository.

The submission deadline is `2022-02-04, 20:00:00`.

## Exercise 1 (8 pts)

We continue with the Disney Plus data set and try to reproduce some of the exercises we did with shell and grep. Work with [Pandas](https://pandas.pydata.org/) when not stated otherwise! We will talk about Pandas in the upcomming weeks.

0. Read chapter 8 to learn more about reading and writing files. I skipped a lot of details.
1. Write a Python program: Read the Disney Plus data as a Pandas Dataframe.
2. Make your program extract a full list of all genre names that are listed in column "listed_in". Make sure to extract only the genres and clean the data from non-letter characters if necessary. Save as a list.
3. Extend your program to count the distinct (unique) genre names. 
4. Next, find how many entries in the disney plus catalog belong to each of the genres. Save the genres and corresponding counts in a dictionary. 
5. Write the results in a new CSV file that contains the genres and the counts. 
6. Count, save in a dictionary and export as a csv the occurances of the terms "Disney" and "Marvel" in the column description. Think about different name variations (like uppercase, etc.).

Commit your Python program and the resulting CSV files. 

## Exercise 2 

### Data transfer (12 pts)
Your task is to transform a dataset on pokemon. Download the dataset [`pokemon.json`](https://github.com/irgroup-classrooms/dis08-2021/blob/main/datasets/pokemon.json) from our Github repository. Write a Python program to:

1. Read in the data from the JSON file (hint: Try the json module or slightly edit the json file and use Pandas),
2. Pokemon have one or more types. Count for each Pokemon type, how many Pokemon of this type exist.
3. Count, how many pokemon of each type have each other type and save as a Pandas dataframe. Create a CSV file where for each type, the counts for each other type are listed. The "same type fields", e.g. grass/grass, water/water etc. should count, how many pokemon have only this type and no other types. 

Make sure to name your columns, your final CSV could look something like this:

type|Grass|Water|Fire|...
-----|------|----------|--------|---
Grass|17|3|0|...
Water|3|22|...|...
Fire|0|...|...|...
...|...|...|...|...

### InfoViz (5 pts)
Create some interesting figures (using Python, in spreadsheet software, with R or any other visualitation software you know) on the pokemon data. You can even draw it by hand and take a photo - As long as the data is derived from the pokemon data, it's fine. If something you have seen somewhere else inspired you, please cite accordingly! There is no shame in inspiration, just be fair and cite your sources! 

## Exercise 3 - Scrape the Wikipedia (25 pts) 

In this final exercise, we would like you to develop a little web scraping project. This is the last part of the second assignment for this semester. It includes a lot of the different tools and skills you learned during this semester.

1. Pick a list within the Wikipedia like the [list of sovereign states](https://en.wikipedia.org/wiki/List_of_sovereign_states). Choose some other list on your own, based on your personal interests. The only requirement is that there are other Wikipedia articles linked within the list. If you have taken this course in the past, make sure to choose a different list!
2. Get all the names and URLs to the corresponding items in the list and export them into a CSV file that has two columns (name and URL).
3. For every Wikipedia article in the CSV list choose a few attributes from the infobox on the right that you would like to extract (e.g., population, name of the head of state, whatever...). These attributes should have at least a little bit in common with the "source list". Extract this information for every entry in your list. Store this information in an appropriate data structure. Make sure to clean your scraped data if necessary!
4. Save your scraped information into a JSON file. Try to export *clean* data.
5. Document your program and development process (in a markdown file). Tell us something about the data you scraped. Why did you choose this data? Can you think of a good use case for this data? As always: Name your files and push everything into your GitHub repository.

## BONUS Exercise
You still are not fed up with juggling your data? Do you need some more points? This task is for you! Surprise us with a cool usecase that uses the scraped data (like an info graphic, an interactive browsing interface, a R-based data analysis, ... ) - We will reward your extra work with up to 10 points.

### Some hints

* Try to be kind to Wikipedia and yourself. You will most likely generate a lot of web traffic while scraping the same webpage again and again. This stresses the Wikipedia's server and takes a lot of time. Try to use a caching method like the one from [requests-cache](https://pypi.org/project/requests-cache/). Alternatively, you can download the HTML content using your script and then work locally.
* Try not to solve the whole problem at once. Remember the tactics desribed in the earlier lectures: [Divide and conquer](https://en.wikipedia.org/wiki/Divide-and-conquer_algorithm) - Step by step. 
* Have a look at the two sample projects from [chapter 11](https://automatetheboringstuff.com/chapter11/). They do something similar.
* A lot of code examples for Beautiful Soup are documented in the [official documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/).
* Again: Documentation is key! Everything that is **not properly documented** is not verifyable by us and will thus get **0 points**. 
