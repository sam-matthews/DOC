# Sublime Text 2

Sublime Text 2 is a text editor. Possibly not just any text editor, but still just a text editor. This document will work through my setup.

So first things first, lets install the software and make the app look just a little bit nicer:

1.	Get the software from [here](http://c758482.r82.cf2.rackcdn.com/Sublime%20Text%202.0.2.dmg)
2.	Open the user settings file, via settings and make these changes:

{
	"font_size": 				18,
	"highlight_line": 			true,
	"file_exclude_patterns":	[],
	"folder_exclude_patterns":	[],
	"ignored_packages":			[],	
}

Next . . . Install the license. This is quite important as it makes life with much easier without the annoying messages. So grab the license, currently in 1Password and add it into the license window. All things going well you should have a working version of Sublime Text.

So now we have an editor which looks reasonably OK and a working copy, that is we have installed the license. Now some more basic setup. Add the package installer and install some themes.

To install go [here](https://sublime.wbond.net/installation) for instructions on how to install the package installer.


There is quite a bit of information out there. So lets start with the following site.

There is [this](http://blog.alexmaccaw.com/sublime-text) website which goes over some ways on how to make SUblime Text 2 look nice. It actually goes into changing the icon as well !

Then there is [this](http://drewbarontini.com/setup/sublime-text/) which goes through quite a few ways to improve the look and feel of Sublime Text 2.

# SODA Theme
The Soda theme is installed from the package installer, but the code etc can be found [here](https://github.com/buymeasoda/soda-theme/).

## The theme is installed - what next

In the user preference file, add the following:
{
	...
	"theme": "Soda Light.sublime-theme",
	...
}

Adding the above to the user preference file - the theme is loaded once the preference file has been saved. Some things I have noted about this theme - 

 - The tabs are not readable.
 - The status bar (at the bottom of the screen) is white (or maybe an off white, or even a spanish white !). I like this change very much.

 note: Restarting Sublime Text fixes the tab issue somewhat, however the tabs are square. I woulds prefer a rounded option for the tabs. Helpfully, there is a solution for this. Make the following changes to the user preference file to make these changes.

## Turn the tabs into something a little nicer

{
	...
	"soda_classic_tabs": true
	...
}

So after saving these changes, the tabs are now a much nicer rounded look.

## Folder icons
Add the following line to add folders to the sidebar.

{
	"soda_folder_icons": true	
}

This change makes the look of the sidebar that little bit nicer.

## Theme Customizations

Looks as though there are some methods on updating these themes. [This](https://github.com/buymeasoda/soda-theme/wiki/Theme-customisation) walks through how to customize these themes. This is something I would like to touch on later.

## Color Schemes

The Soda theme is related to the look and feel of Subloime Text. Below are some instructions or links to some instructions on how to do this. More instructions on the website listed above, but essentially you copy the theme files into the Sublime Text user folder. Then do the following:

PREFERENCES --> COLOR SCHEME --> USERS --> Choose the theme.

# More changes to user preference file

I made some more changes to the user preference file, namely to remove the lione counter and gutter. This gives me a little more space particulary when dealing with text.

The user preference file now looks like this - 

{
	"color_scheme": "Packages/User/Espresso Soda.tmTheme",
	"caret_style": "solid",
	"font_size": 18,
	"highlight_line": true,
	"ignored_packages":
	[
		"Vintage"
	],
	"soda_classic_tabs": true,
	"soda_folder_icons": true,
	"theme": "Soda Light.sublime-theme",
	"wide_caret": true,
	"word_wrap": true,
	"line_numbers": false,
	"gutter": false
}

# Markdown 

Markdown is what I prefer to use when writing text. Why ? Well because someday I'll add the text to a website and using markdown just makes this process that little bit easier.

This first markdown editing package was created by Brett Terpstra and nodoubt is pretty good. He just seems to come out with really good stuff. The github location is [here](http://ttscoff.github.io/MarkdownEditing/).

## Install
Download via Package Installer.

Now the package has been installed, there are some usefull bits that have changed (or introduced).

Under Prefrences --> Package Settings --> Markdown Editing, there are a number of preference files used. As previously there are user settings and default settings. Under user settings there are a number of changes which can be made for the different templates - there are three.

So this means the changes you make in the respective user prefence files for markdown only apply when the type of file is markdown. This is really usefull and makes Sublime Text just so so so useful.

Below is a sample of the changes I have made to the user preference file.

{
	"tab_size": 2,
	// "color_scheme": "Packages/MarkdownEditing/MarkdownEditor-Dark.tmTheme",
	"color_scheme": "Packages/User/Monokai Soda.tmTheme",
	"font_size": 20
}

As you can imagine you can have a user preference file for every type of file you are interested in. As we go on it will be interesting to see how the different code templates work.

As an aside, it will also be interesting to see if Sublime Text will work as some type of dynamic webpage modifier. That is I make changes to documents on Sublime Text and send them through to the webserver, whereever that may be.

# Markdown - A closer look

The first thing to note about Sublime Text is the configuration files are using the JSON format. This file type is very similar to XML, but looks much easier to read. The JSON format is what is used for the preference files and examples can be seen throughout this document.

The user preferences are a fairly simple example of JSON files. However JSON files can be a little more complex. In the MARKDOWNEDITING project mainmenu JSON file looks something like this -

[
    {
        "caption": "Preferences",
        "mnemonic": "n",
        "id": "preferences",
        "children":
        [
            {
                "caption": "Package Settings",
                "mnemonic": "P",
                "id": "package-settings",
                "children":
                [
                    {
                        "caption": "Markdown Editing",
                        "children":
                        [
                            {
                                "command": "open_file",
                                "args": {"file": "${packages}/MarkdownEditing/README.md"},
                                "caption": "README"
                            },
                            { "caption": "-" },
                            {

As you can see there are many layers and the files can become complex. I would imagine there is a good way of managing JSON files in Sublime Text (as so much of Sublime Text is based on JSON files).

## XML

XML files are also used. XML files look a tad more complex and hard to read. Again, hopefully there are some good plugins to use with Sublime Text.  


