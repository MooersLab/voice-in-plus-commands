# voice-in-plus-commands: Fix annoyances with dictated text and open favorite web pages by voice

## Purpose

I share this library to help others add voice-to-text to their work flows. 
I expect that this library will be used largely to inspire the creation of commands that are more relevant to the reader.

## Disclaimer
This is a programming tool, not an educational tool.

## Voice In vs Voice In Plus
Voice In is a free plugin for Google Chrome that supports dictation in the text areas of web pages.
This is where I draft most of my writing these days before pasting it into a final document.
Voice In provides a Notepad for dictation if you do not already have a favorite alternative like 750words.com.
It also works in Overleaf, Jupyter, and Colab.
The word error is about 2-4 percent, better than most alternative dictation software.
It does not do long hallucinations like chatbots, which I find annoying and a waste of my time.

Voice In Plus requires a modest subscription fee.
It adds support for custom commands.

## Library contents
The full version of my command library includes 

- expansion of spoken contractions in English
- expansions of acronyms
- expansions of name of colleagues
- commands to open favorite web pages
- LaTeX boilerplate

I use contractions in my speech, but I do not want them in my writing.
I mapped all the contractions that I could find to their expansions.
Whenever I say a contraction, it is expanded automatically as the software transcribes the text.

It is easy to expand acronyms from memory into the wrong phrase.
Their inclusion in the library eliminates the need to look them up more than once.
If I say the command `expand XXX`, acronym XXX is expanded immediately after it is spoken.
The expansions of acronyms negate the need of having to look them up again and again to check that they are correct.

I also include expansions of the names of colleagues from their first name to their full name.
This ensures that the spelling of the last name is correct and that I do not have to look up the spelling repeatedly.
These types of commands were removed to protect the identity of my colleagues.

I can imagine mapping voice commands to insert cite keys to standard citations for specific software and methods and to key equations.
This kind of information is very domain specific and not included here.

By using a voice command to navigate to a favorite web page, you can keep your fingers on the keyboard.
It is also faster to use a voice command to navigate to a desired page than to have to use the mouse cursor to navigate to that web page.

Most of my writing is done in LaTeX.
The [overleaf.com](https://www.overleaf.com/about/features-overview) webservice makes writing in LaTeX easy.
Its one weakness of Overleaf is that it lacks support for code snippets.
Voice In Plus offers the opportunity to overcome this limitation.
I have mapped voice commands to several dozen LaTeX code snippets.

Another approach that I have discussed in the past to overcome the absence of code snippets in Overleaf and elsewhere is to send the text area from Overleaf to one of five popular text editors via the GhostText plugin for most web browsers.
The code snippets available in these text editors can be inserted into the text.

Because only the English contraction commands may have more widespread appeal and utility, these have been segregated into a separate file available [here](https://github.com/MooersLab/voice-in-plus-contractions).

## Format of the library
The file format is comma-separated values (csv).
The first column has the voice commands in lowercase.
The second column has the text that is inserted and any action commands that are executed between angular braces.
Multi-line text fragments are possible by putting the entire chunk of text between one set of double quotes.

## Installation
1. Right-click on the plugin icon and select `Options`.
2. This action opens the Voice-in options page. 
3. Click on `bulk add` button. A simple window with a plain text area will open.
4. Open the csv file in a text editor like VS Code. Select all, copy, and then paste them into the text area of the `bulk add` window.
5. Click the `add commands` button below the text area. The new commands will be available for use immediately.
