COMP580 Final Report

Members: Blythe King, David Chang, Jordan Van Glish

Description

This project is a typing game that presents words to type and locations of keys audibly instead of visibly. Instead of showing a diagram of the keyboard, or relying on the user’s ability to look at the labels on the keyboard, the program describes key locations, and instead of presenting a paragraph of text for the user to type, it will read aloud letters, words, and phrases to give the user content to practice. Furthermore, the entire program can be navigated using keys instead of having to move the cursor to click on objects on the screen. 

The program has three main modes - tutorial, practice, and test – that the user can select from, with a fourth “further instruction” mode that does not provide typing content but gives additional instructions after the initial explanation. The tutorial mode will read aloud letters and numbers (A-Z, [Space], 0-9) to help the user familiarize him- or herself with the keyboard. If the user types the character incorrectly, then the program will describe the row and location of the correct key. The practice mode will read aloud words and short phrases for the user to practice what he or she learned from the tutorial, as well as help the user learn how to spell words if the user reads on an elementary-level. If the user mistypes one letter, the program will read aloud the location of the mistake (index of mistake and what number of word – e.g., second – the mistake was in). If the user makes more than one mistake, then the program will spell the word for the user to type. The test mode will read aloud longer sentences for the user to type. Like the practice mode, if the user makes one mistake, then the program will read aloud the index and word index of the mistake as well as the correct letter, and if the user makes more than one mistake, then the program will spell out the entire phrase for the user to type.

As the user types their answers, the program will read aloud each letter typed to help the user identify what he or she is typing. If the user hits backspace, then the program will read “backspace” and then the last letter of the new character array. For example, if the user typed “apple” and then hit backspace, the program would say “a,” “p,” “p,” “l,” “e,” “backspace,” and “l” as the user types each respective letter. The mode can be changed at any time during the tutorial, practice, and test modes by hitting the up arrow and typing the corresponding number (1-4) of the desired mode. The cursor is programmed to move to whichever textbox without having the user move the mouse.


Intended Audience

The intended audience is visually-impaired elementary and middle school students. The words are largely elementary-level, hence the younger audience, but any visually-impaired person could use this program to learn the location of the keys, just potentially without the benefit of learning how to spell new words. As such, the game is entirely based on audio descriptions and using the keyboard to navigate rather than the cursor.


Technologies, Frameworks, Libraries

This game was coded using CSS, HTML5, and JavaScript, with the base of the game not being based off of pre-existing code (aside from using tutorials and in-class code – such as the Runner game example by Professor Gary Bishop to see how SpeechSynthesis works - to learn how to use certain JavaScript functions). Most of the game is based off of the use of SpeechSynthesis in JavaScript, as audio descriptions are essential to let visually-impaired users know how to play the game. However, we also designed the page to have visual descriptions for parents and friends of visually-impaired users who want to see what the user is doing in the game. The program is posted on blyking.github.io, so GitHub and GitHub desktop were also essential in designing this game.


How to Build and Deploy It

The most straight-forward way for users to deploy the game is to visit blyking.github.io, as the game is posted there. However, if a user wants to have the game locally on their computer, they could download the .css, .html, and .js files onto their computer into the same folder and click on the .html file.
