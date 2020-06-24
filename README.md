# Create script to clone repos in directory
"Back up" repos in directory by creating a script to clone them (output file is `git_clone_script.sh`):
```
find . -name .git -type d -prune 2>/dev/null -exec git --git-dir={} config --get remote.origin.url \; | sed 's/^/git clone /' > git_clone_script.sh
```
