# Yoda

[![Join the chat at https://gitter.im/kcmerrill/yoda](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/kcmerrill/yoda?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Let the little green guy do the tedious docker work for you!

## What is it? 
Yoda is a command line tool used to interact with docker projects/containers based on Yaml configuration files. There are however some features that yoda does not have that Fig does have, and vice versa.

## Features
- Ability to pull, build and run containers and _all_ of their dependencies. 
- A repository of .yoda files that yoda can grab(and contribute to too!) to get you up and running even quicker!
- Wraps the CLI interface and relies more heavily on shell, thus making it more customizable. 
- Functionality for different environments built in(no need for additional config files based on env)
- A few more!!!

## Installation ##
1. Clone the yoda project from github
2. Run composer to install the php dependencies
3. Add yoda to your $PATH
```bash
git clone git@github.com:kcmerrill/yoda.git
cd yoda/ && ./composer install
sudo ln -s $PWD/yoda /usr/bin/yoda
```

Yoda should now be ready to go. Give it a try
```bash
yoda
```

## Screencast (Video) ##
I suppose it's a little long for a "brief" overview, but a brief overview of what Yoda is. How you might be able to leverage it in certain ways and going over a few of it's key features.

[![Yoda Overview](https://raw.githubusercontent.com/kcmerrill/yoda/master/screenshots/yoda_lift_config.png)](https://www.youtube.com/watch?v=jBvG8wOmAdU)

## Screenshots ##

#### Example of a `$ yoda lift`
Use `yoda lift` to build and run a yoda project and all its dependencies.

Compare the command output to that project's `.yoda` config file.

![Yoda Screenshot #1](https://raw.githubusercontent.com/kcmerrill/yoda/master/screenshots/yoda_lift_config.png)

#### Example of a `$ yoda kill`
If you're looking for a clean start, use `yoda kill` to stop all running docker containers.

![Yoda Screenshot #2](https://raw.githubusercontent.com/kcmerrill/yoda/master/screenshots/3__tmux.png)

#### Example of a `$ yoda control`
Once Yoda has lifted a project's docker container you can use `yoda control` to shell into that container.

The functionality of `yoda control` can be extended by adding a `control:` section to the `.yoda` file.

![Yoda Screenshot #3](https://raw.githubusercontent.com/kcmerrill/yoda/master/screenshots/3__tmux_and_screenshots.png)

