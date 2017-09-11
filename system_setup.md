# macOS Setup

## Step 1 - Install apps outside of command line

### Required
- Xcode, Application Loader
- f.lux
- Atom
- Realm Browser
- SourceTree / *GitKraken*
- *Basecamp*
- *Sketch*, *OmniGraffle*
- Fabric
- Postman
- Docker
- Firefox, Chromium / Chrome
- VLC
- iBook Author, Pages, Numbers, Keynotes
- Private Tunnel
- Transmission, FileZilla, Keka / Unarchiver

### Optionals
- XQuartz
- Eclipse
- Skype
- Telegram
- Tor
- Zeplin
- Slack
- Twitch, Discord, Open Broadcaster Studio
- Blender, *Fusion 360*, *Final Cut Pro*

## Step 2 - Install command line tools & packages

1. xcode-select
    - xcode-select is the CLI for xcode. At this point, since Xcode is already installed in [Step 1](#Step 1), xcode-select should be installed already, to double-check:
        - $ ``xcode-select --install`` If it is installed, there will be this error: **command line tools are already installed, use "Software Update" to instlal updates.**; if not, please follow instructions from [Step 1](#Step 1) to setup and then upgrade macOS by **App Store > Updates**.
        - If for now reason, it is needed to setup a development environment without Xcode (not recommended), install xcode-select *before* [Step 1](#Step 1).
2. homebrew
    1. homebrew is a package manager for macOS. Before installing homebrew, make sure to go through **App Store > Updates** to install the Command Line Tools (which contains compilers to build things from source) for Xcode. To install homebrew, run:
        - $ ``/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"``
    2. After installing homebrew successfully, use homebrew to install the following packages:
        - $ ``brew install carthage``
        - $ ``brew install tmux``
        - $ ``brew install cocoapods``
        - $ ``brew install tree``
        - $ ``brew install heroku``
        - $ ``brew install sqlite3``
        - $ ``brew install mongodb``
        - $ ``brew install postgresql``
        - $ ``brew install git``
        - $ ``brew install python``
        - $ ``brew install python3``
        - $ ``brew install pyenv``
        - $ ``brew install ruby-build``
        - $ ``brew install rbenv``
        - $ ``brew install node``
3. rbenv
    1. Now since rbenv is installed, it's time to configure the development environment for ruby by upgrading the system's ruby-lang version to the latest LTS:
        - $ ``rbenv install 2.4.1``
        - $ ``rbenv global 2.4.1``
    2. Next check if the system is on the latest ruby version by:
        - $ ``ruby -v``
    3. If the system's ruby version failed to be upgraded to the latest version, that is because the system shell uses a different path than rbenv's ruby executables in its directory, to redirect the path for the system's bash_profile, run:
        - $ ``export PATH="$HOME/.rbenv/bin:$PATH"``
        - $ ``eval "$(rbenv init -)"``
        - $ ``ruby -v`` to confirm.
4. gem
    1. RubyGems is the package manager for Ruby, all macOS shipped with RubyGems pre-installed because macOS itself is dependent on Ruby, but its version is almost always outdated, to update RubyGems itself:
        - $ ``gem update --system``
    2. Next upgrade the gems that came pre-installed in the system by:
        - $ ``gem outdated``
        - $ ``gem update``
        - $ ``gem cleanup``
    3. Next install the following gems to setup the development environment for ruby:
        - $ ``gem install rails``
        - $ ``gem install sinatra``
        - $ ``gem install carrierwave``
        - $ ``gem install rspec``
5. pip
    1. pip comes installed when python is installed, python also comes with setuptools (package manager for Python). Upgrade both of them by:
        - $ ``pip install --upgrade setuptools``
        - $ ``pip install --upgrade pip``
    2. After the upgrade, install the following things by:
        - $ ``pip install Django``
        - $ ``pip install awscli``
        - $ ``pip install virtualenv``
6. nvm
    - Similar to rbenv, nvm is the version manager for node:
        - $ ``curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.4/install.sh | bash``
7. perl
    - perl comes pre-installed in very macOS, but it is almost always outdated, to upgrade to the latest perl-lang:
        - $ ``curl -L http://xrl.us/installperlosx | bash``
8. fastlane
    1. fastlane is a continous integration tool, to install, run:
        - $ ``gem install -n /usr/local/bin fastlane --verbose``

# iOS Setup

### Required
- *OmniGraffle*, *InVision*
- TestFlight
- *Basecamp* / *JIRA*
- Reddit, Imgur, YouTube, Telegram, Twitch
- Firefox
- Google Maps / Waze
- Protonmail
- PrivateTunnel

### Optionals
- LinkedIn
- WeChat, Skype, Discord, Slack
- Mint
- Chase / HSBC
