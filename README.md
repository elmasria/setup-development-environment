# Setup Development Environment


## macOS
### git & bash-completion
1. Check if `git-completion.bash` is installed
```
sudo find / -type f -name "git-completion.bash"
```
2. Add `bash-completion` to `~/.bash_profile` or `~/.profile`
```
# bash-completion
if [ -f /opt/local/etc/profile.d/bash_completion.sh ]; then
  . /opt/local/etc/profile.d/bash_completion.sh
fi
```

3. Add `git` branch to terminal prompt by adding the below section to `~/.bash_profile` or `~/.profile`
```
# Git branch in prompt.
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}

export PS1="\u \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "
```

#### References:
* [https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
* [https://www.mfitzp.com/article/add-git-branch-name-to-terminal-prompt-mac/](https://www.mfitzp.com/article/add-git-branch-name-to-terminal-prompt-mac/)

## Helpers
* [Git Style Guide](https://udacity.github.io/git-styleguide/)
