Put scripts and config file in `/home/evgeni/.config/rofi`

Need to `npm install -g chrome-remote-interface` and check issue with permissions/ownership or something
For reference, the script permissions:
```
-rwxrwxr-x 1 evgeni evgeni 466 Jun 24 00:15 chrome-switch-tabs.sh
```

Need to run Chrome with `--remote-debugging-port=9222`. Edit `/usr/share/applications/google-chrome.desktop` or whatever:
```
...
Exec=/usr/bin/google-chrome-stable %U --remote-debugging-port=9222
...
Exec=/usr/bin/google-chrome-stable --remote-debugging-port=9222
...

```

Use the command in `rofi-command.sh` as a keyboard shortcut.