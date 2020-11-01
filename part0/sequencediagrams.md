### 0.4 new note

title new note

browser->server: HTTP POST [https://studies.cs.helsinki.fi/exampleapp/new_note](https://studies.cs.helsinki.fi/exampleapp/new_note)  
note right of browser: from form data, note: "42"  
note left of server: server creates a new note object that has two fields: content and date  
server-->browser:HTML-code  
note left of server: URL redirect to location: notes  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/notes](https://studies.cs.helsinki.fi/exampleapp/notes)  
server-->browser:HTML-code  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/main.css](https://studies.cs.helsinki.fi/exampleapp/main.css)  
server-->browser:main.css  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/main.js](https://studies.cs.helsinki.fi/exampleapp/main.js)  
server-->browser:main.js  
note right of browser: js-code requests JSON from the server  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/data.json](https://studies.cs.helsinki.fi/exampleapp/data.json)  
server-->browser: [{"content":"42","date":"2020-11-01T13:12:54.825Z"},...]  

![new note](/part0/new%20note.png)

### 0.5 Single page app

title Single page app

browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/spa](https://studies.cs.helsinki.fi/exampleapp/spa)  
server-->browser:HTML-code  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/main.css](https://studies.cs.helsinki.fi/exampleapp/main.css)  
server-->browser:main.css  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/spa.js](https://studies.cs.helsinki.fi/exampleapp/spa.js)  
server-->browser:spa.js  
note right of browser: js-code requests JSON from the server  
browser->server: HTTP GET [https://studies.cs.helsinki.fi/exampleapp/data.json](https://studies.cs.helsinki.fi/exampleapp/data.json)  
server-->browser: [{"content":"llll","date":"2020-11-01T09:45:16.670Z"},...] 

![Single page app](/part0/Single%20page%20app.png)

### 0.6 New note

title New note

browser->server: HTTP POST [https://studies.cs.helsinki.fi/exampleapp/new_note_spa](https://studies.cs.helsinki.fi/exampleapp/new_note_spa)  
note right of browser: The POST request contains the new note as JSON-data containing both the content and the date  
note left of server: The Content-Type header of the request tells the server that the included data is in JSON format  
server-->browser:JSON {content: "42", date: "2020-11-01T17:07:11.424Z"}  

![New note](/part0/New%20note%20(1).png)
