# Ruby

Notes for installation or update of Ruby Gems on Mac OS.  Additional notes , featuring the installation of Jekyll.

#### Local

List installed Gems  

    gem list  

## Ruby

Upgrade to the latest [RubyGems](https://rubygems.org/pages/download)

    sudo gem update --system  

#### Outdated
List outdated gems:

    gem outdated --local  

#### Updating
Update all installed rubygems:

    gem update --user-install  

#### Clean
Remove outdated versions of installed gems, leaving the newest updated version installed:

    gem clean  


## Jekyll

Local [installation](http://guides.rubygems.org/command-reference/#gem-install) to a regular account

    gem install --user-install jekyll  

Global installation via an administrator account

    sudo gem install jekyll  

Usage

    jekyll serve  


### Local installation & usage of the So Simple Theme

Installation

    bundle install --path .vendor/bundle

Usage

    bundle exec jekyll serve


## Miscellaneous Gem Commands

    gem environment
    gem list --local
    gem uninstall
    gem dependency nameOfGem --reverse-dependencies


#### References
<https://rubygems.org/pages/download>  
<http://guides.rubygems.org/rubygems-basics/>  
