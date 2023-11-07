## Abra el archivo ~/.bashrc y busqueif [ "$color_prompt" = yes ]; then

```bash
#show git branch
show_git_branch() {
   git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

if [ "$color_prompt" = yes ]; then
    PS1="${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\] \[\033[31m\]\$(show_git_branch)\[\033[00m\]$ "
else
    PS1="${debian_chroot:+($debian_chroot)}\u@\h:\w \$(show_git_branch)\$ "
fi
```
