Run this once your launchd file is ready: `(sudo) cp com.kolonial.tech.updatedb.plist /Library/LaunchDaemons`

To have the task run at a specific time (cron-esque):
`<key>StartCalendarInterval</key>
<dict>
    <key>Hour</key>
    <integer>10</integer>
    <key>Minute</key>
    <integer>37</integer>
</dict>`

To load the task:
`launchctl load -w /Library/LaunchDaemons/com.kolonial.tech.updatedb.plist`

To unload the task:
`launchctl unload -w /Library/LaunchDaemons/com.kolonial.tech.updatedb.plist`

To start the task:
`launchctl start com.kolonial.tech.updatedb`

To stop the task:
`launchctl stop com.kolonial.tech.updatedb`

To determine if the task loaded:
`launchctl list | grep kolonial`

To debug a task:
Look at `/tmp/test.stdout` and `/tmp/test.stderr`
