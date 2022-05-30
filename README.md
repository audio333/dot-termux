# Termux

### PKG
* `$ pkg install nodejs-lts wget curl python2 transmission`
* `$ pkg install screenfetch ffmpeg tealdeer gitui`
* `$ pkg install openssh nmap iproute2`
* [ytfzf](https://github.com/pystardust/ytfzf/wiki/Termux-How-To)
  * `$ pkg install ncurses-utils fzf chafa`
  * Install a patched version of [mpv-android](https://kitsunemimi.pw/tmp/mpv-android-2022-03-24.apk)
    * Make sure the regular version of mpv-android is not installed
    * Open mpv, go to three dots top right->Settings->Advanced->Install/Update youtube-dl and 
    * select Install and choose yt-dlp
* [ani-cli](https://github.com/pystardust/ani-cli#android)
  * [mpv-android script](https://www.reddit.com/r/termux/comments/schy01/anicli_on_termux/humuou4/)
  * Make sure to add the referrer in mpv by opening mpv (playstore version), going into Settings -> Advanced -> Edit mpv.conf and adding:
    > referrer="https://gogoanime.fi/"

### Fresh Install Info
    sudo apt install git stow

    # clone dotfiles
    cd ~
    git clone https://github.com/audio333/dot-termux.git

    # backup current dotfiles
    mkdir -p ~/Downloads/stowbackup
    mv ~/.bashrc ~/Downloads/stowbackup

    # symlink all files in dotfiles dir to home dir
    cd ~/dot-termux

    # link only folders (trailing slash)
    stow -v -t ~ */

        # delete (-D flag)
        stow -v -D -t ~ */
        stow -v -D -t ~ newsboat

        # redo link (-R)
        stow -v -R -t ~ */
        stow -v -R -t ~ newsboat


    src: https://github.com/gotbletu

