![Version](https://img.shields.io/static/v1?label=voice-in-plus-commands&message=0.2&color=brightcolor)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)


# voice-in-plus-commands: Fix annoyances with dictated text and open favorite web pages by voice

## Purpose

I share this library to help others add voice-to-text to their workflows. 
This library will be used largely to inspire the creation of commands that are more relevant to the reader.

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
- open specific websites in browser (e.g., `open PubMed`, `open Google Scholar`, `open PDB`, `open LBSF`, `open OCSB`, `open weather forecast`)

I use contractions in my speech but do not want them in my writing.
I mapped all the contractions that I could find to their expansions.
Whenever I say a contraction, it is expanded automatically as the software transcribes the text.

It is easy to expand acronyms from memory into the wrong phrase.
Their inclusion in the library eliminates the need to look them up more than once.
If I say the command `expand XXX`, acronym XXX is expanded immediately after it is spoken.
The expansions of acronyms negate the need to look them up again and again to ensure that they are correct.

I also include expansions of the names of colleagues from their first name to their full name.
This ensures that the spelling of the last name is correct and that I do not have to look it up repeatedly.
These types of commands were removed to protect the identity of my colleagues.

I can imagine mapping voice commands to insert cite keys to standard citations for standard methods and to key equations.
This kind of information is domain-specific and not included here.
Instead, I have set up several domain-specific libraries in separate repositories so that users can download only those collections of voice snippets relevant to their work.
See [Voice Computing](https://github.com/MooersLab/MooersLab?tab=readme-ov-file#voice-computing) section of the MooersLab landing page for hyperlinks to these repositories.

By using a voice command to navigate to a favorite web page, you can keep your fingers on the keyboard.
It is also faster to use a voice command to navigate to a desired page than to use the mouse cursor to navigate to that web page.

Most of my writing is done in LaTeX.
The [overleaf.com](https://www.overleaf.com/about/features-overview) web service makes writing in LaTeX easy.
Its one weakness of Overleaf is that it lacks support for code snippets.
Voice In Plus offers the opportunity to overcome this limitation.
I have mapped voice commands to several dozen LaTeX code snippets.

Another approach I have discussed to overcome the absence of code snippets in Overleaf and elsewhere is to send the text area from Overleaf to one of five popular text editors via the GhostText plugin for most web browsers.
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

## Related repositories
See [Voice Computing](https://github.com/MooersLab/MooersLab?tab=readme-ov-file#voice-computing) section of the MooersLab landing page.

## Rules for developing voice commands

### Pick word combinations rarely used in ordinary prose
The basic rule for developing a voice command is to pick a word combination that is very unlikely to be used in one's prose.
This choice can avoid the accidental insertion of an unintended set of words.
For example, using the voice command "to do" to insert an org-mode TODO is pointless because this phrase is used frequently in my prose.
Instead, I came up with the command ''priority'' and then the associated alphanumeric code for the priority. 
It is pretty unlikely that I will say the command "priority A1" in my usual prose.

### Pick word combinations that do not contain other commands
If you pick a word combination with a subset of words already assigned to another command, the commands will collide, and you will not get the intended effect.
It is better to pick a synonym for the new command than include the old one.

### Use verbs are prefaces
I use the verb "insert" in front of the computer code that I want to insert.
I use the verb "expand" to expand a person's first name into their full name and to expand acronyms into their full term.

### Test the commands
Like other forms of computer code, test the Voice In commands to ensure you get the intended effect.
The speed with which you vocalize a command has a significant impact.
You may find that you have to verbalize the command at high speed to avoid inserting just the first word of the command rather than the entire command.

|Version      | Changes                                                                                                                                    | Date                 |
|:-----------:|:------------------------------------------------------------------------------------------------------------------------------------------:|:--------------------:|
| Version 0.2 |  Added badges and update table. Fixed all.csv so that it shows up as a table on GitHub.                                                    | 2024 April 13        |

