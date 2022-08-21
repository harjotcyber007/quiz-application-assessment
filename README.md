Quiz app using HTML, CSS, and Javascript from harjot singh for assessment

Arcitecture :

Index file 
 |     |
 |     |
game  highscore

 we create game.html and game.css.

- Display Hard Coded Questions
- Create `game.js` file 
- Create functions that load questions, identify selected answers

Need to figure out how to query each of the `.choice-text` elements, so using `data-number="X"`.
We then change that to an array using `const choices = Array.from(document.getElementsByClassName("choice-text"));` 

JavaScript Spread syntax to bring the `questions` array into the `availableQuestions` array

Then I also uses the [splice] method which adds/removes items to/from an array. 

Display Feedback for Correct/Incorrect Answers

- Apply a class to the question element based on correct/incorrect answer selection 
- use setTimeout to display the correct/incorrect answer for 1000ms before calling getNewQuestion(); 
- Add the HTML/CSS elements to create a header (Question and Score)
- Created function to increment score if answer is correct.
- Create a Progress Bar
- The progress bar is filled in by adjusting the width of inner div using rogressBarFull.style.width = `${(questionCounter / MAX_QUESTIONS) * 100}%`



At end I did :
- Created `end.html` and `end.js` files 
- Added CSS for forms 
- Added function to `end.js` that checks for a value in the username field to disable to the save button


Score saving : 

- Save High Scores in Local Storage
- Saves player's score to local storage `localStorage.setItem("mostRecentScore", score);`
- Application tab > Local Storage

- sort high scores, limit scores to top 5, and write them to local storage
- Load and Display High Scores from Local Storage
- Creates `highscores.html`, `highscores.css`, and `highscores.js` pages
- Pulls in high scores from local storage using `const highScores = JSON.parse(localStorage.getItem('highscores')) || [];`
- Use JS [array map()](https://www.w3schools.com/jsref/jsref_map.asp) to convert the returned array from local storage to elements for an HTML list 

Fetch API to Load Local Questions:

- Move hard coded questions from `game.js` to `questions.json`
- questions from `questions.json` and display them in the console: 


Fetch API to Load Questions API:

Uses [Open Trivia DB API](https://opentdb.com/api_config.php) to pull questions.
Side note: I installed [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa/related?hl=en) into Chrome to be able to view the returned JSON in a cleaner format. 

The format in which questions are returned from Open Trivia DB is not the format we use in our app. So we're going to use a map function to clean it up. 

This is end