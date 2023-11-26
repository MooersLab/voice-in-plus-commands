# voice-in-plus-commands: Fix annoyances with dictated text and open  favorite web pages by voice

## Purpose

To help others trying to add voice-to-text to their work flow.

## Voice In vs Voice In Plus
Voice In is a free plugin for Google Chrome that supports dication in the text areas of web pages.
This is where I draft most of my writing these days before it paste it into a final document.
Voice In provides a Notepad for dication if you do not already have a favorite alternative like 750words.com.
It also works in Overleaf, Jupyter, and Colab.
The word error is about 2-4 percent, better than most of the alternative dictation software.
It does not do long hallucinations like chatbots, which I find to be annoying and a waste of my time.

Voice In Plus requires a modest subscription fee.
It adds support for custom commands.

## Library contents
My full version of the command library includes 

- expansion of spoken contractions in English
- commands to open favorite web pages
- LaTeX boilerplate

I use contractions in my speach, but I do not want them in my writing.
I mapped all of the contractions that I could find to their expansions.
Whenever I say a contraction, it is expanded automatically as the text is transcribed.

By using a voice command to navigate to a different web page, I can keep my fingers on the keyboard.
It is also faster to use a voice command to navigate to a desired page rather than to have to use the mouse cursor to navigate to that web page.

I do most of my writing in \LaTeX.
The overleaf.com website makes writing in \LaTeX so easy.
Its one weakness is that it lacks support for code snippets.
Voice In Plus offers opportunity to overcome this limitation.
I have mapped voice commands to a number of \LaTeX code snippets.

Another approach that I have discussed in the past to overcome the absence of code snippets is to send the text area from Overleaf to one of five popular text editors via the GhostText plugin for most web browsers.
Then the code snippets available in these text editors can be inserted into the text.

Because only the English contraction commmads may have more widespread appeal and utility, these have been seggregated into a separate file so that user can avoid my other commands.

## Format of the library
The file format is comma separated values (csv).
The first column has the voice commands in lowercase.
The second column has the text that is inserted and any action commands that are executed in between angular braces.
Multi-line text fragments are possible via the newline command (`\n`).

## Installation
1. Right click on the plugin icon and select `Options`.
2. This act opens the Voice-in options page. 
3. Click on `bulk add` button. A simple window with a plain text area will open.
4. Open the csv file in a text editor like VS Code. Select all, copy, and paste into the text area of the bulk add window.
5. Click the `add commands` button below the text area. The new commands are available for use.
