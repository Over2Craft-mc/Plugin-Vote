# Vote (Plugin) - FORK 

[![Style](https://github.styleci.io/repos/237491397/shield)](https://github.styleci.io/repos/237491397)
[![Chat](https://img.shields.io/discord/625774284823986183?color=5865f2&label=Discord&logo=discord&logoColor=fff&style=flat-square)](https://azuriom.com/discord)

A vote plugin to reward players when they vote.

## Why this fork

This fork add a way for players to choice on which server the reward should be given. 

A pull request has been done and refused [here](https://github.com/Azuriom/Plugin-Vote/pull/22)

Here is an example
![image](https://user-images.githubusercontent.com/74878280/126628099-58560bf9-a186-4aee-a1c5-f3df7bddbe9c.png)

## Theme

You will need a small adjustment with your theme to use this fork, otherwise
you will get an error `Illuminate\Contracts\Encryption\DecryptException : The payload is invalid.` while voting.

See [here](https://github.com/Azuriom/Plugin-Vote/compare/master...magrigry:multi-server/1.x?expand=1#diff-e6a72274bd2be1ba8cf26cb930f07d9c65cf4329bfc5f832779d8be3129ea3c6) 
an example that show to modify your theme for it to work with this fork.

## Review changes
Changes are simple and easy to read. You can review them [here](https://github.com/Azuriom/Plugin-Vote/compare/master...magrigry:multi-server/1.x?expand=1)

## Installation

Download this fork as a zip. Go to your Azuriom root directory, extract the content into `./plugins/vote` 
