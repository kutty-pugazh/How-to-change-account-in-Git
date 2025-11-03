## Change GitHub / GitLab / Bitbucket account (authentication)

**If you want to use a different online account (for pushing/pulling):**

**Check which account is stored:**
```sh
git remote -v
```

**→ Example output:**
```sh
origin  https://github.com/olduser/myproject.git
```

**Change the remote URL to your new account:**
```sh
git remote set-url origin https://github.com/newuser/myproject.git
```

**If you’re using HTTPS, clear old credentials:**

## Windows:
```sh
Open Credential Manager → Windows Credentials → Remove GitHub entry
```
## macOS:
```sh
Open Keychain Access → Search “github” → Delete entry
```
## Linux (with credential cache):
```sh
git credential-cache exit
```

Next push, Git will ask you to log in — use your new account’s credentials or personal access token.