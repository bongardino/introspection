# For the goals

![demo](./images/in_action.png)  

I am poor at remembering to spend time in consideration of how I spend my time
So I spent some time on this bit of bash that runs a bit of applescript that runs a bit of bash so I don't have to spend time on that

run on a cron

`5 16 * * * MON-FRI cd $HOME/src/introspection && gtimeout 3600 ./ask_myself`

(brew install core-utils for gtimeout)  
  
##### TODO  
- [ ] automate shipping this to [google sheets w go](https://developers.google.com/sheets/api/quickstart/go)
