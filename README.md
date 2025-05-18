## Fearless Geek Session Manager

**fgsm** is an application or session launcher, written in pure bash with no
ncurses or dialog dependencies. It does have soft dependencies on gum and figlet.
It is inspired by cdm, tdm, in some way by krunner and related.

### Dependencies
* Gum
* figlet

This project was originally based on tbsm, but all of the tbsm code has now been removed and has been re-written from scratch.

Details about **tbsm** can be found in the doc directory and on
the [tbsm home page](https://loh-tar.github.io/tbsm/) with some
screenshots.

### Installation
1. Place `src/fgsm` into your path. - example: `sudo cp src/fgsm /usr/local/bin`
2. Copy `src/xinitrc` to $HOME/.xinitrc - `cp src/xinitrc $HOME/.xinitrc`
3. Place the following code into your `.zshrc` or `.bashrc` if you're using ZSH or Bash:
```

# Start FGSM on tty1
if [[ "$(tty)" == "/dev/tty1" ]]; then
  command -v fgsm >/dev/null && fgsm
fi
  
```
Other shells will have a different process for this.
4. Disable any display/session manager you may have currently set up. If on a systemd Linux system, `sudo systemctl disable [whatever the manager name]`

### To-Do
Add other options to the menu

### License

GNU General Public License (GPL), Version 2.0
