# Text-Editor

## Technology Used 

| Technology Used         | Resource URL           | 
| ------------- |:-------------:| 
|  Git | [https://git-scm.com/](https://git-scm.com/)     |    
| JavaScript    | [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) | 
| IndexedDB   | [https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) |
| Heroku    | [https://devcenter.heroku.com/categories/reference](https://devcenter.heroku.com/categories/reference) |
| npm    | [https://docs.npmjs.com/](https://docs.npmjs.com/) | 

## Description 
[The Deployed Site.](https://fa-texteditor.herokuapp.com/).

This text editor is a PWA aaplication that, retrieves data from, and stores data to an IndexedDB. 

Some code from an exisiting application was provided. However, I added scripts to the package.json, implmented asset caching to the src-sw.js, and additinal code to the src/js files.

![Text Editor](/client/src/images/Screen%20Shot%202023-03-03%20at%2010.47.23%20PM.png)

## Portfolio Example

An integral component of creating this application was including scripts in the package.json. Doing so allows for specific actions to be called upon. For example, "start:dev" will start both the client and server folders at the same time, whereas "start" will run and build only the server.

```
  "scripts": {
    "start:dev": """,
    "start": """,
    "server": """,
    "build": """,
    "install": """,
    "client": """
  },

```

These are the scripts I added.

```
  "scripts": {
    "start:dev": "concurrently \"cd server && npm run server\" \"cd client && npm run dev\"",
    "start": "npm run build && cd server && node server.js",
    "server": "cd server nodemon server.js --ignore client",
    "build": "cd client && npm run build",
    "install": "cd server && npm i && cd ../client && npm i",
    "client": "cd client && npm start"
  },

```


## Usage 

Use Insomnia to view and interact with information using the routes.


## Learning Points 

Adding the scripts to the package.json helped me to reflect on the commands I run through the terminal. 


## Author Info

### Fayven Amelga 


* [Portfolio](https://famelga.github.io/Portfolio/)
* [LinkedIn](https://www.linkedin.com/in/fayven-amelga-b09b17b6/)
* [Github](https://github.com/famelga)



## Credits

Fayven Amelga




## License

MIT License

Copyright (c) 2023 Fayven Amelga

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Badges

![MIT Badge](https://img.shields.io/badge/license-MIT-blue)

---

© 2023 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.