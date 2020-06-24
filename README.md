# Create script to clone repos in directory
```
find . -name .git -type d -prune 2>/dev/null -exec git --git-dir={} config --get remote.origin.url \; | sed 's/^/git clone /' > git_clone_script.sh
```
