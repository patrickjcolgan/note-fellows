Project Title:
Note Fellows

Contributors:
Adam
Jared
Chris
Kevin
Connor

Version 1.0 release date:
11/20/15

known bugs:
none

# CF301 - Patrick & Serina


1. changed returnUser and newUserForm
  + Instead of two document.getElementById commands, replaced with one of these in both returnUser and newUserForm: `$('#loginForm').append('<form name="....`

2. In the following function, attempted to change to just _one_ eventListener using jQuery, but it broke everything.
``` javascript
function newUserForm (event) {
  $('#loginForm').append('<form name="loginform" class="whiteText" id="newUser"><fieldset><legend>New User</legend><label>Username</label><input class="labelColor" type="text" name="usr" placeholder="username" required="required"><label>Password</label><input class="labelColor" type="password" name="pword" placeholder="password" required="required"><p id="msg"></p><input class="button-primary" type="submit" value="Create New User"></fieldset></form><input class="button-primary" type="submit" value="Switch to Login Page" id="existingButton">');
    var newUserEl = document.getElementById('newUser');
    newUserEl.addEventListener('submit', function(e) {newUser(e);},false);
    var existingButton = document.getElementById('existingButton');
    existingButton.addEventListener('click', function(e) {returnUserForm(e);},false);
  };
  ```

3. Attempted to change the following to jQuery, but could not figure out whey it would not work.
``` javascript
clearNoteBrowser: function () {
  document.getElementById('noteList').innerHTML = '';
  // $('#noteList').append('');
},
clearForm: function () {
  document.getElementById('displayWindow').innerHTML = '';
  // $('#displayWindow').append('');
},
clearNoteWrapper: function (){
  document.getElementById('noteWrapper').innerHTML = '';
  // $('#noteWrapper').append('');
},
```

4. SMACSS
 + added a base.css, layout.css, and module.css
 + moved some content from style.css to these three files.

5. Mobile-first principles
 + Changed base.css code for mobile-first
 + This hides the "welcome to note fellows" text
 + centers the Note Fellows icon
 + Adjusts padding
 + Add 750px, module.css media query adjusts to desktop view

6. localStorage does not appear to need adjusting (at least, not without significant changes to other functions that may be beyond the scope of this assignment)
