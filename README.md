# Setup Development Environment


## macOS
### git & bash-completion
1. Check if `git-completion.bash` is installed
```
sudo find / -type f -name "git-completion.bash"
```
2. Add `bash-completion` to ``~/.bash_profile` or ``~/.profile`
```
# bash-completion
if [ -f /opt/local/etc/profile.d/bash_completion.sh ]; then
  . /opt/local/etc/profile.d/bash_completion.sh
fi
```
#### References:
* [https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
