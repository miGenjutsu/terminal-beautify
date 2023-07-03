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
    	- current font using: ShureTechMono Nerd Font Mono


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

## Documentation:

file path `/mnt/c/Users/domhe/`

after consulting with `chatgpt` it helped resolve the issue i was experincing when attempting to load customize `oh-my-posh theme` heres that conversation:
Locate Your Windows User's Home Folder: In WSL, your Windows user's home folder can be accessed at the following path: /mnt/c/Users/<WINDOWSUSERNAME>. Replace <WINDOWSUSERNAME> with your actual Windows username.

Copy Your Oh My Posh Theme to Windows Home Folder: Copy your beautifyterminalkusha.omp.json theme file from your WSL's home folder (e.g., ~/github/prompt/) to your Windows user's home folder. You can do this by running the following command in your WSL terminal:

bash

cp ~/github/prompt/beautifyterminalkusha.omp.json /mnt/c/Users/<WINDOWSUSERNAME>/

Update the ~/.bashrc Configuration: Modify the line in your ~/.bashrc file to point to the theme file in your Windows user's home folder. Update the path accordingly:

bash

    eval "$(oh-my-posh init bash --config '/mnt/c/Users/<WINDOWSUSERNAME>/beautifyterminalkusha.omp.json')"

By copying your theme file to your Windows user's home folder and updating the path in the ~/.bashrc file, you should be able to use the shared theme between Windows and WSL. Remember to save the changes to your ~/.bashrc file and restart your terminal for the modifications to take effect.

This approach allows you to maintain a single copy of your theme file that can be used in both Windows and WSL environments without the need for separate copies or complex path configurations.  


**Updating Theme**

If you've updated your Oh My Posh theme in Windows and want to reflect those changes in your WSL2 environment, you can follow these steps to update the theme:

    Open a Windows File Explorer window.

    Navigate to your Windows user's home folder, which is typically located at C:\Users\<WINDOWSUSERNAME>. Replace <WINDOWSUSERNAME> with your actual Windows username.

    Locate the updated beautifyterminalkusha.omp.json theme file in your Windows user's home folder.

    Copy the updated theme file.

    Open a WSL2 terminal.

    In your WSL2 terminal, navigate to your WSL2 user's home folder using the path /mnt/c/Users/<WINDOWSUSERNAME>. Replace <WINDOWSUSERNAME> with your actual Windows username.

    bash

cd /mnt/c/Users/<WINDOWSUSERNAME>

Paste the updated theme file into your WSL2 user's home folder.

Once the file is copied, you can update the path in your ~/.bashrc file to point to the updated theme file in WSL2.

bash

eval "$(oh-my-posh init bash --config '/mnt/c/Users/<WINDOWSUSERNAME>/beautifyterminalkusha.omp.json')"

Save the changes to your ~/.bashrc file.

Restart your WSL2 terminal or run the following command to apply the changes:

bash

    source ~/.bashrc

After following these steps, your updated Oh My Posh theme should be applied in your WSL2 environment.