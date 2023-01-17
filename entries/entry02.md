# Entry 2
##### 1/9/23

During the past two months, I started tinker deeper in firebase by choosing a section which I choose the [authentication](https://firebase.google.com/docs/auth) section. At first, I followed the creating email [guide](https://firebase.google.com/docs/auth/web/password-auth) and I started off with this beginner code:

```js
createUserWithEmailAndPassword(auth, email, password)
  .then((userCredential) => {
    // Signed in
    const user = userCredential.user;
    // ...
  })
  .catch((error) => {
    const errorCode = error.code;
    const errorMessage = error.message;
    // ..
  });
```
But after I tried to go to the next step by going to [manage users](https://firebase.google.com/docs/auth/web/manage-users) to try to fill in the `.then()` and `.catch()` statements, it got confusing to puzzle things together. So I watched this authentication [video](https://www.youtube.com/watch?v=b1ULt_No3IY&ab_channel=%7BRhymBil%7D) and I took the html page and a snippet of the js page where you only create a user and the conponents I needed so I can take it step by step and not do an entire log in page. 

```js
function register() {

  email = document.getElementById('email').value
  password = document.getElementById('password').value
  
  auth.createUserWithEmailAndPassword(email, password)
  .then(function() {
  
    var user = auth.currentUser
    var database_ref = database.ref()
    var user_data = {
      email : email,
      full_name : full_name,
      last_login : Date.now()
    }

    database_ref.child('users/' + user.uid).set(user_data)

    alert('User Created!!')
  })
  .catch(function(error) {
    var error_code = error.code
    var error_message = error.message

    alert(error_message)
  })
}
```
I realized it doesn't follow the code that the offical document gave; so I tried to alter it a bit by merging them both to see if it still worked or if it was outdated. I switched the first function into `(userCredential)`, switch both functions into arrows, and remove the `.auth`.
```js
function register() {

  email = document.getElementById('email').value
  password = document.getElementById('password').value

  createUserWithEmailAndPassword(email, password)
  .then((userCredential) =>{

    var user = auth.currentUser
    var database_ref = database.ref()
    var user_data = {
      email : email,
      last_login : Date.now()
    }

    database_ref.child('users/' + user.uid).set(user_data)

    alert('User Created!!')
  })
  .catch((error) => {
    var error_code = error.code
    var error_message = error.message

    alert(error_message)
  })
}
```
When I tried to run it, I ran into an issue where in the console, it said:
```diff
- Uncaught SyntaxError: Cannot use import statement outside a module
```
I tried going to [stackoverflow](https://stackoverflow.com/questions/59761839/syntaxerror-cannot-use-import-statement-outside-a-module-firebase-functions) to see if there was a solution to this problem and it still didn't solve the issue for me since it still appeared. I tried typing in this:
```js
const initializeApp = require('firebase/app');
const getAuth = require('firebase/auth');
const signInWithEmailAndPassword = require('firebase/auth');
const createUserWithEmailAndPassword = require('firebase/auth');
const onAuthStateChanged = require('firebase/auth');
```
# Goals for the future

To solve the uncaught syntax error.<br>
Look at [Net Ninja Youtube Playlist](https://www.youtube.com/playlist?list=PL4cUxeGkcC9jERUGvbudErNCeSZHWUVlb) to see their way of firebase auth and see if I can add on to what I currently have.<br>
Look at Mr. Mueller's [example](https://github.com/brianmueller/mfa-pds/blob/main/y2122/firebase/like.html) to see if I can absorb anything to help with building my firebase.<br>

We are currently in the second step of our EDP (Engineering Design Process) where we are suppose to research our problem and I was researching how to use firebase more in the authentication part. My next step is to brainstorm possible solutions and see what I can use with firebase to connect it with my project.

The two skills I used was how to google and how to read. I used how to google by googling firebase authentication javascript tutorial instead of just googling firebase to get what I specifically wanted; like the language and section I wanted to learn from firebase. I also use how to read to read the document once I got on the website and dissected the specific beginner code I wanted out of all the other beginner codes.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
