# Lab Report 4 - Vim

![step_4](images/lab-4/step-4.PNG)  
**Keys pressed:** `<up><enter>`  
Pressing `<up>` cycles through the previous terminal history, which in this case is the `ssh` since it was the last one ran. `ssh` allows me to connect to the ieng6 server after running said command with `<enter>`.

![step_5](images/lab-4/step-5.PNG)  
**Keys pressed:** `git clone ^v<enter>`  
I create a copy of the repo by typing out `git clone` and pasting the repo link with `^v` (CTRL + v).

![step_6](images/lab-4/step-6.PNG)  
**Keys pressed:** `cd l<tab><enter><up><up><up><up><enter><up><up><up><up><enter>`  
Typing out `cd l` and tabbing autocompletes to `lab7/` since there are no other items that start with 'l'. Both the `javac` and `java` commands were four up in the history, so pressing `<up>` for each accesses both. These commands change the working directory into the lab7 repo, then compiles the java files and runs 'ListExamplesTests'.

![step_7](images/lab-4/step-7.PNG)  
**Keys pressed:** `vim L<tab>.j<tab>i<backspace>2<esc>:wq<enter>`  
First run the `vim` command by typing the filename. `L` will autocomplete to 'ListExamples' then typing `.j<tab>` after will get the full filename, 'ListExamples.java'. With my cursor at the top of the file, I would press `G6ker2:wq<enter>` while inside Vim. This would have the effect:
- `G` - move cursor to end of file
- `6k` - move cursor 6 lines up
- `e` - move cursor to end of next word (index1, in this case)
- `r2` - replace character at cursor with '2'
- `:wq<enter>` save and quit  
  
![step_8](images/lab-4/step-8.PNG)  
**Keys pressed:** `<up><up><up><enter><up><up><up><enter>`  
Since the `javac` and `java` commands are now only 3 up in the history, only 3 arrow key presses are needed to access and run them. They compile and run the code, like in step 6, to verify the changes are correct.

![step_9](images/lab-4/step-9.PNG)  
**Keys pressed:** `git add L<tab>.j<tab>; git commit -m "bug fix"; git push`  
Typing out each git command into one bash command saves the need to execute each one individually. Tabbing 'L' will autocomplete to 'ListExamples', then typing out '.j' and tabbing will autocomplete to 'ListExamples.java'. Altogether, the command stages ListExamples for commit, creates a commit with the message "bug fix", and pushes the commit to github.
