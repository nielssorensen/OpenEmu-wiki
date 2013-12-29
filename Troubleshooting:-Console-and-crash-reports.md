When troubleshooting problems with OpenEmu, it is often necessary to inspect logs or crash reports. Both of these can be found in [Console](http://en.wikipedia.org/wiki/Console_%28OS_X%29), OS X's built-in log utility.

### Opening Console

Console is located at /Applications/Utilities/Console, but it is perhaps easiest to open it through Spotlight:

1. Click on the Spotlight icon on the menu bar (the magnifying glass on the far right)
2. Enter `Console` into the search field
3. Console will probably be the top hit, or at least the top 'Application' hit — click it

![Spotlight search for Console](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/troubleshooting/Spotlight%20-%20Console.png)

### Viewing OpenEmu logs

OpenEmu logs to the normal system log, which is visible by default (as part of *All Messages*) when Console opens. Messages at the bottom are newest, and most of those relevant to OpenEmu will contain the text `OpenEmu` or `OpenEmuHelperApp` somewhere.

When possible, it may be preferable to watch the logs as the problem is happening. To do this, open Console and note the last line (you can also insert a marker with the *Insert Marker* tool-bar button). Then, switch to OpenEmu (re-launch it if necessary) and replicate the problem you were having. Any new log entries that appear are probably relevant.

Once you can see the log entries, simply select the lines and copy them like any normal text. You can either click and drag or use Shift+click and/or Cmd+click to select specific lines.

![Console logs](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/troubleshooting/Console%20-%20logs.png)

### Viewing OpenEmu crash report

When OpenEmu (or its helper application) crashes, it usually generates a [crash report](http://en.wikipedia.org/wiki/Crash_reporter), which contains error and debugging information which may be useful to developers. These crash reports appear in Console under the *User Diagnostic Reports* header on the left-hand side, and have names like this:

OpenEmu_2013-12-29-153318_`<computer name>`.crash    
OpenEmuHelperApp_2013-12-29-153318_`<computer name>`.crash

![Console crash reports](https://raw.github.com/okdana/OpenEmu-documentation/master/assets/img/troubleshooting/Console%20-%20crash%20reports.png)

Simply find any files that correspond to the time the crash occurred (often there is just one) and click it. Then you can use Select All (⌘A) and copy the text.

**Note**: There is usually no identifying information in the crash report text — computer names, user names, installed applications, &c., are not included. Your user name may be included if a file path relevant to the crash occurred in your home directory, however. If you are worried about this, feel free to double-check the file before providing it to the developers.

### Providing logs and crash reports to OpenEmu developers

If the log information is brief (a few lines or less), you can simply paste it into an [issue](https://github.com/OpenEmu/OpenEmu/issues?state=open).

Otherwise, for crash reports and large numbers of log entries, it may be best to use a [paste bin](http://en.wikipedia.org/wiki/Pastebin). GitHub has a built-in paste bin called [Gist](https://gist.github.com/), which is quite convenient, but you may use another service (like [Pastie](http://pastie.org/)).

Once you've pasted the log/report contents into the paste bin's text field, click the create/submit button. You will then be given a link to provide to the developers (or often you can simply copy the URL from the address bar in your browser).
