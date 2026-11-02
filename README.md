# L73 – Lyrics Finder

**Student:** NIV HIRPARA | **Roll:** D17 | **Division:** H | **Enrollment:** 24004501210108

## Problem
Build a search tool over a folder of song lyric text files (write your own short lyrics).

## Who will use it
Music fans and songwriters.

## Folder structure
- main.sh: Main menu and program execution.
- lib/functions.sh: Contains functions for all project features.
- data/lyrics/: Stores song lyrics text files.
- reports/: Stores generated top 10 words reports.
- backups/: Stores backup archives of project data.
- logs/activity.log: Records project activities.
- logs/cron.log: Records scheduled cron job output.
- README.md: Contains project documentation.

## Features
1. Find songs containing a word (grep -ril)
2. Count how many times a word appears (grep -o | wc -l)
3. Show the longest song by lines (wc -l | sort)
4. Show the 10 most used words (tr | sort | uniq -c)
5. Replace a word and show a preview (sed, no -i)

## How to run
1. Open the Ubuntu terminal.
2. Go to the project folder:
   cd ~/linux_project/lyricsfinder
3. Give execute permission:
   chmod +x main.sh
4. Run the program:
   ./main.sh

## My crontab line and what it means


Crontab command:
0 20 * * 0 cd /home/niv/linux_project/lyricsfinder && /bin/bash -c 'source lib/functions.sh; cron_task' >> /home/niv/linux_project/lyricsfinder/logs/cron.log 2>&1

Explanation:
0 - Minute (0)
20 - Hour (8 PM)
* - Every day of the month
* - Every month
0 - Sunday

## Commands I used and why
- grep: Searches for words in lyric files.
- wc: Counts words, lines, and occurrences.
- sort: Sorts the results.
- uniq: Counts repeated words.
- sed: Replaces words and displays a preview.
- tar: Creates a compressed backup.
- cron: Runs the scheduled report automatically.
- chmod: Gives execute permission to the script.
- nano: Edits project files.

## What I learned
Through this project, I learned how to write and execute Bash shell scripts in Linux. I learned to search lyric files using grep and count words using command-line tools. I also learned how to create backups, maintain activity logs, and schedule tasks using cron. This project improved my understanding of Linux commands and shell scripting.
