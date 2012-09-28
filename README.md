#CodeRunner-Syntax-Files

##About
This repo is a collection of extra syntax files for [CodeRunner](http://krillapps.com/coderunner/). CodeRunner is an app for Mac OS X. CodeRunner itself is limited on the number of languages it has [syntax highlighting](http://en.wikipedia.org/wiki/Syntax_highlighting) for.

##Install
First of all, clone this repo somewhere via the terminal.
```bash
git clone git@github.com:lukevers/CodeRunner-Syntax-Files.git
```
Now, there are two things you have to do. First, place the plist syntax files into the Syntax folder where CodeRunner keeps them. That can be located here:
```bash
/Applications/CodeRunner.app/Contents/Resources/Syntax
```
Next, you need to edit the `Syntax.plist` file that tells CodeRunner what plist files to use. That can be located here:
```bash
/Applications/CodeRunner.app/Contents/Resources/Syntax.plist
```
If you're editing `Syntax.plist` with Xcode or another plist editor, just add a new `String` to the `Dictionary`. If you're not using a plist editor then just simply add these two lines. For example, pretend we're adding Go as a language:
```xml
<key>Go</key>
<string>go.plist</string>
```
The `key` is the name that you'll see in CodeRunner under `Syntax Mode` under `Languages` in preferences. The `string` is the location and name of the plist file within the Syntax folder where the plist files are kept.

When editing/replacing any of the files, you may have to authenticate yourself. If it still does not work, copy the file to a new location, edit it, and then copy the file back to the original location.