# dailog
A simple command line tool which helps you to quickly capture what you've done at the end of the day. All points are saved in a monthly markdown file. Points entered during one day are gathered under this day's date.

## Installation
```
TODO
* clone
* chmod
* add to path
```

## Usage

### Gathering items
- Run `dailog` in your terminal
- Enter your points line by line (hit `enter` at the end of each line)
- Exit with `CTRL + d`

### Dumping today's commit messages to dailog
*currently supports only Mercurial*

- Navigate to the project you would like to log
- Run `dailog hg`
- Today's commit messages will be added to dailog

### Preview
Run `dialog preview` to quickly preview current month's log.

### Edit
Run `dialog edit` to edit last or current month's log. Chose from the menu which month's log  you want to edit.

### Export PDF
Run `dialog pdf` to export last or current month's log to pdf. Chose from the menu which month's log  you want to edit. After the pdf is created, the file opens automatically via Mac OS Preview.

__*Warning:*__ pdf export depends on pandoc being correctly installed on your computer.

## Internals

__*dailog*__ creates a folder with its name in root directory of the current user. All markdown and pdf files are being added to this directory.

### File structure
Depending on the current date __*dailog*__ will create a  markdown file for the current month if it does not exit: `yyyy-mm.md`. It will append daily acitivities to the current section for the currenday)

```
# 2016-11

## 2016-11-01 (Tuesday)
- Some task
- Some other task

## 2016-11-02 (Wednesday)
- Some commit message
- Some other commit message
```

## FAQ

__*Why dailog and not daylog?*__

Initialy the script was called *daylog*. After trying it for a couple of days I was consistently mistyping and almost always ended up with *dailog*. Probably the word *daily* which is being typed very often is to blame :)

## Next steps
* Add installation steps
* Add pandoc installation steps
* Add github log feature
* Add configuration, i.e. to store github/mercurial username for filtering
* Add project specific logs



