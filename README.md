# Sublime Development Settings for python development

>A guide on how to match my full sublime setup in an easy to follow process.

Welcome! Please find around my specific sublime setup that allows you to match
This setup is not only extremely useful, It is also *extremely pretty.*
<!-- markdownlint-disable MD013 -->
![Sublime Setup Preview](https://packagecontrol.io/readmes/img/0d63060a39000f2691d757a8a448e071ba534579.jpg)
<!-- markdownlint-enable MD013 -->

---

## What to do with this repository

If you are lazy you could just find your installation of Sublime and copy the contents
of the folders in this repository to the respective `Packages` & `Installed Packages`
to their respective folders on your local machine. With the exception of the
Markdown & Python specific packages, everything would work without issues.

---

## Installed Packages

These are all the specific packages that I use with descriptions on why they
were included.

### Stand alone packages

These packages have no dependencies. They are mainly for making things efficient
or pretty.

#### [Package Control](https://packagecontrol.io/installation)

The sublime text package manager that just makes it simple to keep everything
working as it should be. This is critical to installing all the rest of the
packages outlined below. Installation instructions are located on the link above.
From this point on every package can be installed by bringing up the
package control prompts:

* On Windows:  `Control`+`Shift`+`P`
* On Mac: `Command`+`Shift`+`P`

And then typing: `Package Control:Install Package`

#### [Theme - Gravity one](https://packagecontrol.io/packages/Theme%20-%20Gravity)

Let's start by making sublime prettier. This is by far one of the best themes
out there. I run my entire machine on Dark Mode so the black bar is a welcomed
addition.

#### [GitGutter](https://packagecontrol.io/packages/GitGutter)

A Sublime plug-in that shows information about your file status within a git
repository. Has status bar text telling you everything happening as well as
inline popups if you so wish. I couldn't do without it.

![GitGutter in Action](https://packagecontrol.io/readmes/img/3f3140ad6c5c6269f71c23233bf47b7d17350cfc.gif)

#### [SideBarEnhancements](https://packagecontrol.io/packages/SideBarEnhancements)

The normal sidebar menu has NOTHING and is generally not useful. SideBarEnhancements
solves that cleanly allowing you to create folders, add new files etc with a
single right click.

#### [Pretty JSON](https://packagecontrol.io/packages/Pretty%20JSON)

I seriously dislike having to clean up JSON files. This package does most of the
grunt work with a single command.

* On Windows: `Control`+`Alt`+`J`
* On Mac: `Command`+`Control`+`J`

#### [SublimeLinter](https://packagecontrol.io/packages/SublimeLinter)

This is my linter of choice. Supports tons of different linters and all the
packages I use for python, markdown & json linting are through this linter.
Useful commands:

* On Windows:
  * Lint the current document: `Control`+`K`, `L`
  * Show all Lint errors: `Control`+`K`, `A`
  * Go to next Lint error: `Control`+`K`, `N`
  * Go to previous Lint error: `Control`+`K`, `P`
* On Mac:
  * Lint the current document: `Command`+`Control`+`L`
  * Show all Lint errors: `Command`+`Control`+`A`
  * Go to next Lint error: `Command`+`Control`+`E`
  * Go to previous Lint error: `Command`+`Control`+`Shift`+`E`

#### [MarkdownPreview](https://packagecontrol.io/packages/MarkdownPreview)

Allows you to open a markdown file on a browser window so you can preview it
against the most popular formats.

### Python Development Packages

These packages require you install Python on your local machine and set it up
correctly. I will include how to install the pre-requisites for each.

**Notes:**

* Mac OS:
  * 10.10+ Has python 2.7 by default bound to the `python` command. You have to
  custom install python 3.+ and use`python3` to trigger commands to that version.
  * You can no longer mess with anything in `/usr/bin`, you have and instead
  have to rely on `/usr/local/bin/`.
  * If you use `pip` it will fail *most* times due to System Protections. use
  `pip3` instead you should be trying to develop against python 3+ anyways as
  python 2 is being deprecated in 2020.
* Windows:
  * Ensure you bind your python install to your PATH variable.

#### [Sublimelinter-pylint](https://packagecontrol.io/packages/SublimeLinter-pylint)

Interface to pylint. Pylint can seriously help improve the way you code python
catching a lot of the noob errors people make. **Depends on pylint being installed**
To install: `pip install pylint`

#### [Sublimelinter-pyflakes](https://packagecontrol.io/packages/SublimeLinter-pyflakes)

Interface to pyflakes. Optional really. I prefer pylint. But I like doubling up
on my code linters if it helps me even more to avoid stupid errors. **Depends on
pyflakes being installed**
To install: `pip install pyflakes`

#### [Sublimelinter-pycodestyle](https://packagecontrol.io/packages/SublimeLinter-pycodestyle)

Lints python to conform to PEP8 standards. **Depends on pycodestyle being installed**
To install: `pip install pycodestyle`

#### [Sublimelinter-pydocstyle](https://packagecontrol.io/packages/SublimeLinter-pydocstyle)

Lints python to conform to PEP257 documentation standards. **Depends on pydocstyle
being installed**
To install: `pip install pydocstyle`

#### [AutoDocString](https://packagecontrol.io/packages/AutoDocstring)

Because I am lazy and I prefer stubs for code are generated for me to save me
the seconds I waste copy-pasting around doc strings and instead I generate it
with a single command:

* On Windows: `Control`+`Alt`+`'`
* On Mac: `Command`+`Alt`+`'`

#### [PyYapf Python Formatter](https://packagecontrol.io/packages/PyYapf%20Python%20Formatter)

Another addition because I am lazy. Runs yapf to autoformat the script. **Depends
on yapf being installed**
To install: `pip install yapf`

### Other Linter Packages

#### [Sublimelinter-json](https://packagecontrol.io/packages/SublimeLinter-json)

Extremely useful for linting JSON networking data. Uses the Sublime Console parser
so no dependencies.

#### [Sublimelinter-contrib-markdownlint](https://packagecontrol.io/packages/SublimeLinter-contrib-markdownlint)

What I use to lint these files! Requires Node.js installed. And then for you to
install the markdownlint-cli pacakge.

After installing Node.js run the following command: `npm install -g markdownlint-cli`
