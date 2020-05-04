COMP580 Final Report


Members: Blythe King, David Chang, Jordan Van Glish


Description

This project is a typing game that presents words to type and locations of keys audibly instead of visibly. Instead of showing a diagram of the keyboard, or relying on the user’s ability to look at the labels on the keyboard, the program describes key locations, and instead of presenting a paragraph of text for the user to type, it will read aloud letters, words, and phrases to give the user content to practice. Furthermore, the entire program can be navigated using keys instead of having to move the cursor to click on objects on the screen.

The program has three main modes - tutorial, practice, and test – that the user can select from, with a fourth “further instruction” mode that does not provide typing content but gives additional instructions after the initial explanation. The tutorial mode will read aloud letters and numbers (A-Z, [Space], 0-9) to help the user familiarize him- or herself with the keyboard. If the user types the character incorrectly, then the program will describe the row and location of the correct key. The practice mode will read aloud words and short phrases for the user to practice what he or she learned from the tutorial, as well as help the user learn how to spell words if the user reads on an elementary-level. If the user mistypes one letter, the program will read aloud the location of the mistake (index of mistake and what number of word – e.g., second – the mistake was in). If the user makes more than one mistake, then the program will spell the word for the user to type. The test mode will read aloud longer sentences for the user to type. Like the practice mode, if the user makes one mistake, then the program will read aloud the index and word index of the mistake as well as the correct letter, and if the user makes more than one mistake, then the program will spell out the entire phrase for the user to type.

As the user types their answers, the program will read aloud each letter typed to help the user identify what he or she is typing. If the user hits backspace, then the program will read “backspace” and then the last letter of the new character array. For example, if the user typed “apple” and then hit backspace, the program would say “a,” “p,” “p,” “l,” “e,” “backspace,” and “l” as the user types each respective letter. The mode can be changed at any time during the tutorial, practice, and test modes by hitting the up arrow and typing the corresponding number (1-4) of the desired mode. The cursor is programmed to move to whichever textbox without having the user move the mouse.
 

Intended Audience

The intended audience is visually-impaired elementary and middle school students. The words are largely elementary-level, hence the younger audience, but any visually-impaired person could use this program to learn the location of the keys, just potentially without the benefit of learning how to spell new words. As such, the game is entirely based on audio descriptions and using the keyboard to navigate rather than the cursor. Furthermore, the colors used (Carollina blue background and blue text) were tested for a high contrast using webaim.org’s contrast checker, which helps web developers pick color schemes for low-visibility users. As a positive side effect of being developed for those that are visually impaired, the game may also be used by any person learning to type on the keyboard, as long as they cover their hands with something so they don’t “cheat” and look at the keys.
 

Technologies, Frameworks, Libraries

This game was coded using CSS, HTML5, and JavaScript, with the base of the game not being based off of pre-existing code (aside from using tutorials and in-class code – such as the Runner game example by Professor Gary Bishop to see how SpeechSynthesis works - to learn how to use certain JavaScript functions). Most of the game is based off of the use of SpeechSynthesis in JavaScript, as audio descriptions are essential to let visually-impaired users know how to play the game. However, we also designed the page to have visual descriptions for parents and friends of visually-impaired users who want to see what the user is doing in the game. The program is posted on blyking.github.io, so GitHub and GitHub Desktop were also essential in designing this game.
 
 
How to Build and Deploy It

The most straight-forward way for users to deploy the game is to visit blyking.github.io, as the game is posted there. However, if a user wants to have the game locally on their computer, they could download the .css, .html, and .js files onto their computer into the same folder and click on the .html file in their file explorer. 

If an educator, parent, or student would like to inject their own words, phrases, or sentences into the game, here are the steps needed to do so:
1. Download the entire repo into a folder on your computer
2. Open Intro.js in a code editor, such as Visual Studio Code
3. Add, edit, or replace any of the following:
        i. Words: line 78 (var words = [...])
        ii. Phrases: line 79 (var phrases = [...])
        ii. Sentences: line 91 (var sentences = [...])
4. Save the .js file and close the editor
5. Open the index.html file in a browser (Preferably Google Chrome)


Issues, Shortcomings, and Future Work

The main issue/”bug” of the game is how the program corrects typos involving the space bar in the practice and test modes. For example, if a user is prompted to type “once in a blue moon” but instead types “oncebin a blue moon,” the program will correct the user by saying, “Incorrect! You typed b instead of space between two words of the phrase.” This differs from how the program corrects the user if he or she had typed “once en a blue moon,” as the program will give the word index (second) and the letter index within the word (first). The correction for space typos is not as illuminating as it could be since it does not give the exact location of the error. However, the space bar bug was found very late in the project development and would have been given a more advanced fix had it been found earlier.

Any other known shortcomings of the game are largely from “not being sure” what game design would be most useful for visually-impaired users. One complaint the game got from peer evaluations was that the text took too long to go through. We alleviated this issue by making general instructional text (i.e., any audio instructions said while the cursor is in the mode select text box) skippable by selecting a mode, but we were hesitant to make the audio describing the mode, reading aloud what the user has typed, or describing typos skippable. As of now, the audio reads aloud exactly what the user has typed into the answer text box by reading aloud any event.key aside from “Enter” (submits the answer) and the up arrow (switches to the mode select text box) to allow visually-impaired users to get the best idea possible of what their current answer is without having to see the screen. We did not want to make it skippable in case the user accidentally typed a letter; we want the user to be able to hear any mistakes he or she makes. Furthermore, the program needs to be able to describe where errors are fully; if this audio is accidentally skipped, then the user could become very confused about how to proceed to the next prompt.

Another shortcoming that could lead into future work involving 3D-printing is the inefficiency of describing the location of keys. For example, enter is described as being “far right, fourth from top” on the keyboard, as when we closed our eyes, that was the only way for the program to accurately direct us to the correct key. A peer evaluation suggested that we figure out another way to describe the locations of keys, but we could not figure another way to audibly describe the location. However, if we were able to 3D-print a keyboard cover with braille letters, then this issue would be mitigated entirely. Unfortunately, not being on campus has rendered that idea impossible but would be an interesting future extension to this project.

In terms of adding on to the game itself in the future, more “modes” can be added. Right now, the game only teaches lowercase letters, the space bar, and numbers, but future versions could teach punctuation and capitalization. In addition, a timed mode could be added to test how many words per minute the user can type. The game is adequate for beginner typists, but future work can make it useful for typists of all levels.
