# Installation:

1. https://github.com/bongardino/introspection
1. Clone or Download
1. Download as Zip
1. Unzip
1. Copy the entire `introspection-master` folder to Applications


## Running :

1. Open the Terminal application
1. `/Applications/introspection-master/ask_myself` to run it
1. You should get a popup, and a log.csv should get created in the `introspection-master` folder, which you can open in any spreadsheet viewer

That runs the app, but we want to put it on a timer so it runs automatically!
So, we make an entry in crontab

## Scheduling:

1. Open the Terminal application (beee careful in with this tool! The commands listed here are safe but never copy / paste things into your terminal if you don't trust the source and understand what they will do!)
1. `env EDITOR=nano crontab -e` to open crontab, which will probably be blank. You can type in this window!
1. add `5 4 * * fri /Applications/introspection-master/ask_myself` to this file, which will cause ask_myself to run at 4:05 every Friday
1. `Ctrl + O` to save
1. `Ctrl + X` to exit


## Change Things!

### Want to change the questions?

1. Open the Text Edit Application
1. File > Open > /Applications/introspection-master/ask_myself
1. Edit the list of `opts` at the top of this file. to contain as many or few items as you want
eg:
```
opts=(time_boxed
      prioritized_tasks
      limited_out_of_band_work
      had_fun
      ) 
```
to
```
opts=(drank_wine
      ate_cookies
      won_prizes
      ) 
```

### Want to disable the timer?

1. Open the Terminal application
1. `env EDITOR=nano crontab -e` to open crontab
1. delete the `5 4 * * fri` line
1. `Ctrl + O` to save
1. `Ctrl + X` to exit

### Want to change the timer to a different time?
1. Change the crontab entry to something different! You can figure it out with this  
https://crontab-generator.org/

