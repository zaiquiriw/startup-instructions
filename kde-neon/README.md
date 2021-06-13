# Installing KDE Neon
## First setup the GPU!
  I bricked my last install so now I am setting up the gpu first off before anything else.
  I followed the instructions on this reddit post to install. Time to check if it works!
  https://www.reddit.com/r/kdeneon/comments/jgdw30/best_way_to_install_nvidia_drivers_on_kde_neon/
  I ran the command sudo lshw -C display to do this and.... It works! (You have to restart of course)
  
## Cloning this very Repo!
  Well, I originally had a lot of notes but things crashed and I hadn't saved so now is the time to set this up,
  install GIT! And Emacs while you are at it. We wanna be able to edit this readme whenever we want from a local copy.
    sudo apt-get install emacs
    sudo apt-get install git
    # set up git
    git config --global user.name "<username>"
    git config --global user.email "<email>"

  Now, I also want to add a project folder, prj, that will hold projects and github clones
    mkdir ~/prj
    cd prj
    git clone https://github.com/zaiquiriw/startup-instructions.git

  If you wanna push changes:
    git init
    git status (check the status of the staging before starting)
    git add <filenames and stuff> (-A if you are crazy)
    git commit -m "Message about commit" (This commits a change to head, but not a remote repo)
    git push origin master (Now push the changes to the master branch of the repo)
    
    
  
## Setting up the home Directory
  I don't like capital letter names so...
    mv Desktop desk
    mv Downloads dwn
    rm -r Documents Music Pictures Videos Templates Public
    mkdir doc dwn img med/vid med/music pub tmpl
    
    And then change the default directory names in .config
    XDG_DESKTOP_DIR="$HOME/desk"
    XDG_DOWNLOAD_DIR="$HOME/dwn"
    XDG_TEMPLATES_DIR="$HOME/tmpl"
    XDG_PUBLICSHARE_DIR="$HOME/pub"
    XDG_DOCUMENTS_DIR="$HOME/doc"
    XDG_MUSIC_DIR="$HOME/med/music"
    XDG_PICTURES_DIR="$HOME/img"
    XDG_VIDEOS_DIR="$HOME/med/vid"