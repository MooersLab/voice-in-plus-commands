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
My full version of the command library includes expansion of spoken contractions, commands to open favorite web pages, and LaTeX boilerplate.
Because only the first may have widespread appeal and utility, these have been seggregated into a separate file.

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