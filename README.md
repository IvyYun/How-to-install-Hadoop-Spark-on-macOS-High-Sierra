# How to install Hadoop/Spark on macOS High Sierra

1. Something need to be done before setup Hadoop:

- Error: `Since I've already installed Hadoop in my Mac, I need to link it with my Brew`, while it threw me error when I tried to do __brew link hadoop__ (Could not symlink sbin/FederationStateStore /usr/local/sbin is not writable.)

  - How to resolve it:
    cd /usr/local
    sudo mkdir sbin
    sudo chown -R $(whoami) $(brew --prefix)/*
    brew link hadoop (yourPackageName)
