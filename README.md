# zybookscript
script to destroy zybooks

Copy paste the following script into the f12 console (javascript console) and press run.
from https://www.reddit.com/r/userscripts/comments/vje7b2/does_anybody_know_a_user_script_that_actually/
in the second comment

I've slightly modified the program to fix some bugs


//////////////////////////////////

// CLICK ALL RADIO BUTTONS

//////////////////////////////////

var radioButtons = document.querySelectorAll('input[type="radio"]');

var index = 0;

function clickNextButton() {

if (index < radioButtons.length) {

radioButtons[index].click();

index++;

setTimeout(clickNextButton, 300); // adjust delay as needed

}

}

clickNextButton();

//////////////////////////////////

// CLICK ALL 2X SPEED BOXES

//////////////////////////////////

var x2Buttons = document.querySelectorAll('input[type="checkbox"]');

var index2 = 0;

function clickNextBox() {

if (index2 < x2Buttons.length) {

x2Buttons[index2].click();

index2++;

setTimeout(clickNextBox, 300); // adjust delay as needed

}

}

clickNextBox();

//////////////////////////////////

// CLICK ALL START BUTTONS

//////////////////////////////////

var startButtons = document.querySelectorAll('button[class="zb-button  primary  raised           start-button start-graphic"]');
console.log(startButtons.length)

var index3 = 0;

function clickNextStartButton() {

if (index3 < startButtons.length) {

startButtons[index3].click();

index3++;

setTimeout(clickNextStartButton, 300); // adjust delay as needed

}

}

clickNextStartButton();

//////////////////////////////////

// CLICK ALL PLAY BUTTONS

//////////////////////////////////

function clickNextPlayButton() {

setTimeout(clickNextPlayButton, 100);

let playButtons = document.querySelectorAll('button[aria-label="Play"]');

var index4 = 0;

if (index4 < playButtons.length) {

playButtons[index4].click();

index4++;

setTimeout(clickNextPlayButton, 300); // adjust delay as needed

}

let pauseButtons = document.querySelectorAll('button[aria-label="Pause"]');

if (pauseButtons.length != 0) {

clickNextPlayButton;

}

}

clickNextPlayButton();

//////////////////////////////////

// CLICK ALL SHOW ANSWER BUTTONS

//////////////////////////////////

var index5 = 0;

function clickNextShowAnswerButton() {

setTimeout(clickNextShowAnswerButton, 100);

let showAnswerButtons = document.querySelectorAll('button[class="zb-button secondary show-answer-button"]');

if (index5 < showAnswerButtons.length) {

showAnswerButtons[index5].click();

setTimeout(showAnswerButtons[index5].click(), 100); // adjust delay as needed

index5++;

setTimeout(clickNextShowAnswerButton, 100); // adjust delay as needed

}

}

clickNextShowAnswerButton();
