# bash-config

```bash
parse_git_branch() {
  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

export PS1="\u@local \[\e[32m\]\w \[\e[91m\]\$(parse_git_branch)\[\e[00m\]$ "

bind 'set show-all-if-ambiguous on'
bind 'TAB:menu-complete'
```
