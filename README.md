# Vote (Plugin) - FORK 

[![Chat](https://img.shields.io/discord/625774284823986183?color=5865f2&label=Discord&logo=discord&logoColor=fff&style=flat-square)](https://azuriom.com/discord)

A vote plugin to reward players when they vote.

## Why this fork

This fork add a way for players to choice on which server the reward should be given. Here is an example
![image](https://user-images.githubusercontent.com/74878280/126628099-58560bf9-a186-4aee-a1c5-f3df7bddbe9c.png)

A pull request has been done and refused [here](https://github.com/Azuriom/Plugin-Vote/pull/22)

## Theme

### Your theme may already support this fork. 
If it don't, you will need to edit it manually or ask to the author of the theme to edit it.
List of themes that already support this fork : 
* [rainbow](https://market.azuriom.com/resources/71) (you will need to edit the theme confguration)

### How to edit your theme
You will need a small adjustment with your theme to use this fork, otherwise
you will get an error `Illuminate\Contracts\Encryption\DecryptException : The payload is invalid.` while voting.

Edit the file `views/plugins/<your_theme>/index.blade.php`. If it doesn't exist, create it and put the content of [this file](https://github.com/magrigry/Plugin-Vote/blob/multi-server/1.x/resources/views/index.blade.php) in it. If the file already exists, edit it and add this piece of code where you want to see the server choice list :
```php
            @if(isset(serversChoice))
                @if (count($serversChoice) > 1)
                    <select id="stepServerIdInput">
                        @foreach($serversChoice as $id => $name)
                            <option value="{{ $id }}">{{ $name }} </option>
                        @endforeach
                    </select>
                @else
                    <input type="hidden" id="stepServerIdInput" value="{{ array_key_first($serversChoice) }}">
                @endif
            @endif    
```

## Installating the fork
* Click the download button to download this fork as a zip. 
* Go to your Azuriom root directory
* If the directory `./plugins/vote` exists, delete it or rename it e.g. `votes.old`. This won't delete any data, plugins are stateless. 
* Create the directory `./plugins/vote` with the right permissions (same as other plugins)
* Extract the content of the zip into `./plugins/vote` 

## Review changes
This fork is safe to use. Changes are simple and easy to read. You can review them [here](https://github.com/Azuriom/Plugin-Vote/compare/master...magrigry:multi-server/1.x?expand=1)

