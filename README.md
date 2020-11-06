# Automate-Code
Using pygsheet codes in a pycharm project with Anocanda Python interpreter.

## Create bat. file
Open notepad

Paste this paragraph

```
@echo on
call D:\Users\xinyue\Anaconda3\Scripts\activate.bat
D:\Users\xinyue\Anaconda3\python.exe "D:\Users\xinjin\PycharmProjects\Daily_Update_FullyAuto\Auto_Update.py"
Pause
```

Save as filename.bat (type this whole thing into file name)

## Setup a timer in Windows system

Open Task Scheduler from search.

From right side bar Action, click Create Task.

In General bar: Give a task name, check "Run whether user is logged in or not" (this will disable any GUI relate to your code, I used my code with chrome webdriver, so the webdriver doesn't show, but still functionable with webscrapying and files downloading) which also requires your logging Windows password at the same time.

In Trigger bar: click New, check Daily/ Weekly or anything you need. Then set up a time when you want it run everyday.

In Action bar: click New, it will automatically show start a program. Click Browse and select the bat file you created.

Then click OK to finish the setting. It should work.

## Note

You may need to move all your google credential into System32 dir, so it won't ask your permission again.

You have to choose either "Run whether user is logged in or not" or "logged in", otherwise the google API credential doesn't work. (Which means that Create Basic Task doesn't work)

## Author

Xinyue Zhang


