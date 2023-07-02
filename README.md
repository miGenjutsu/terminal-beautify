# Terminal Beautify

This repo contains all the `settings.json` configurations in order to keep my terminal sync accross all devices. The purpose of this repo is to keep a record and easily setup if ever a new `terminal` will be introduced.

Included in this repository will also be an [Oh-My-Posh Prompt Theme](https://ohmyposh.dev/docs/) that was edited according to personal likes. 

Inspired by the [ohmyposh preset](https://ohmyposh.dev/docs/themes) theme [kushal](https://github.com/JanDeDobbeleer/oh-my-posh/blob/main/themes/kushal.omp.json)

## HOWTO GUIDE:: 
[Scott Hanselman: How to make the ultimate Terminal Prompt on Windows 11](https://www.youtube.com/watch?v%253DVT2L1SXFq9U%2526t%253D1935s)

after following this guided process I've built the confidence to customize my own prompt according to how i would like it to look.

copy the `RAW` content of the `beautifyterminal.omp.json` and create a new `.json` file and paste in newly created file. update the `~/.bashrc` or `$PROFILE` accordinly.

if ever have the desire to create a new prompt them use [oh-my-posh/segemnts](https://ohmyposh.dev/docs/segments/) to do so. just simply build off a preset.

follow naming convention: `beautifyterminal<nameOfInspiredTheme>.omp.json`

## NOTES::

- in powershell ::- insert full path @`./$PROFILE`
  - `windows location` appdata/local/programs/ohmyposh/themes/*name-of-custom-theme*
  - BETTER SUGGESTION::
    - **create a `github/prompt` directory and save the full path that way**
        - windowsLocation:- `c:/.`
        - ubuntuLocation:- `~/.`
  - Remeber: update your `~/.bashrc` and `$PROFILE`
    - `~/.bashrc`:
        ```
        eval "$(oh-my-posh init bash --config "<path-to-file>.omp.json)"
        ```
    - `~/$PROFILE`:
        ```
        oh-my-posh init pwsh --config "<path-to-file>.omp.json" | Invoke-Expression
        ```   
- visual studio code:
	- update font-family
		-- current font using: ShureTechMono Nerd Font Mono


## TODO:
- locate the blueish folder icon
- keep updating accordingly
- configure `~/.bashrc` and `~/$PROFILE` and upload those edits to this repo

## Thoughts::
  - depending on the `segments` move accordingly. i currently moved the AWS to the right but all the others are set to the left. **left open space between `lines 84-85` since this is where i took the AWS Segment from**
    -  if want to move to the right follow instructions:
       - place desired `segments` in the lines after `154`
         - in between:
         ```
         "alignment": "right",
         "segments": [ .... ]
         ```
----


