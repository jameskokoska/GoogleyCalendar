# Googly Calendar
Turns your Google Calendar into a task list. Helps to keep your busy school life/regular life organized and balanced. It can be used here: <a href="https://googlycalendar.web.app">https://googlycalendar.web.app/</a>.  
I wanted to improve my React knowledge so I created this. I also use it daily so I think it's pretty good :)

## Features
* Sync to your Google Calendar, with up to 3 calendars supported
* Mark tasks as completed/incomplete
* Stored information inside Google Calendar with emoji, and can be synced across multiple browsers
* Identify course codes in event names
* Display information in a pleasing way and modern UI
* Dark mode and auto dark mode
* Custom animations
* Color coded courses
* Custom course color codes
* Identifies courses automatically of the format ```XXX000``` or ```XXXX000``` where ```X``` is any letter and ```0``` is any number before the task name in the calendar
* Pin tasks top top of list
* Specify key words to highlight tasks
* Specify key words to hide specific events
* Support for description of events
* Overdue events become red
* Can add list of important events to highlight so you don't miss them
* Support for 'all day' events
* All possible sorting combinations are remembered when reloading the calendar
* 7 day view dynamically adjusts to use specification for 'Number of days to view setting'
* Can mark tasks as complete in 7 day view
* Can change the range of days to view in the 7 day view by navigating with arrows
* Sort information based on Course/Completed/Task Name/Date set
* Save settings to web browser cache
* Save last preferred sorting method
* Save last navigated tab
* Specify number of events to load
* Specify number of days to view tasks from
* Load events before the current time (specify in settings)
* Refresh and sync new data from your Google Calendar
* Error detection when session times out
* Welcome message, with change log and first time sign in button
* Auto reload calendar when needed, for example on login
* Configurable Pomodoro timer
* Pomodoro timer sounds
* Pomodoro timer tracking, and motivational messages
* Calculate and track your marks across courses
* Add any course name and keep track of the marks

## Create and run a local copy
### Setting up API keys
1. Setup Google API Keys 
2. Create file in root of project (i.e. ```.\googleycalendar\```) called ```apiGoogleconfig.json```
3. Get ```Client ID (OAuth 2.0 Client IDs)``` and ```Key (API keys)``` from Google Developers website and pass in the following format into the JSON file:
```
{
    "clientId": "[Client ID]",
    "apiKey": "[Key]",
    "scope": "https://www.googleapis.com/auth/calendar",
    "discoveryDocs": ["https://www.googleapis.com/discovery/v1/apis/calendar/v3/rest"]
}
```

### First time install
Ensure React and NPM are properly installed
1. ```cd .\googly-calendar\```
2. ```npm install```

### Running development server after install
1. ```cd .\googly-calendar\```
2. ```npm start```
3. open ```localhost:3000``` in preferred web browser


### Hosting with Firebase
0. Proper project directory ```cd googly-calendar```
1. Install the dependency ```npm install -g firebase-tools```
2. Login to Firebase ```firebase login```
3. Initialize Firebase ```firebase init```
4. ```Yes``` to proceed
5. Select ```Hosting: Configure and deploy Firebase Hosting sites``` and hit enter
6. Select ```Use an existing project```
7. Select ```googly-calendar (Googly Calendar)```
8. Answer: What do you want to use as your public directory? ```build```
9. Answer: Configure as a single-page app (rewrite all urls to /index.html)? ```No```
10. Answer: Set up automatic builds and deploys with GitHub? ```No```
### Deploy to Firebase
#### Option 1:
1. Build the project ```npm run build```
2. (Optional) Check out built project ```firebase serve --only hosting```
3. Deploy to Firebase ```firebase deploy```
#### Option 2:
1. Add to ```package.json```
    ```
    "scripts": {
        ...
        "predeploy": "npm run build",
        "deploy": "firebase deploy"
    }
    ```
2. Use ```npm run deploy``` for all deployment