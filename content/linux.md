---
title: Very Basic Vim and Command-line Stuff desu
sub_title: Plus some keyboard shortcuts
Date: 2020-06-01
LastMod: 2020-06-11
---

[Back to catalog](https://otaking.xyz/index.html)

Useful Vim editor stuff and some linux mint mate command line stuff to copy and paste. The main purpose for this just as with everything else on this site is for my own benefit and reference so that in case I lose my setup or forget stuff then I can set this to set it up again somewhat. All of the stuff here I just got it from different parts of the internet and the documentation in programs and I have collected it for my benefit so I am not going to bother with bloating this page with sources. I am a n00b so remember that there are better/different ways to do stuff than I do here but this is just what worked for me desu desu desu desu desu desu.

## Command line stuff

- sudo /etc/init.d/bluetooth restart: to restart bluetooth in linux mint
- pulseaudio -k: to restart audio in linux mint
- sudo apt update && sudo apt upgrade -y: update packages in linux mint
- reboot: reboot linux mint
- control+z: to send a document to the background
- fg doc-name.html: to bring the document back to the foreground
- date: tells me the date
- shutdown: shutsdown computer
- exit: closes terminal
- man program-name: shows manual for a program. Super Useful.
- cal: shows calendar.
- cal -3: shows calendar for previous, current and next month.
- cal june 546: shows calendar for the month of june in 546.
- df -h: shows free space in the hard drive. The "h" stands for human readable or something.
- du -h directory-name: will show file sizes of subdirectories and the size of the directory.
- du -ah directory-name: will show file sizes of all files within a directoru
- du -h filename : shows space used by a file.
- ls -lh: lists directories with file sizes in a human readable format.
- ls -lah: shows the hidden files as well in a directory... Jusr ls does not show hidden .dotfiles as such.
- file filename: Gives information about filename. E.g. file rss.png gives info about rss.png.
- file -b filename: Same as file but does not write filename in order to be brief
- cd directory-name : change directory to directory name.
- cd ~/ : Change directory to home directory.
- ps ax: lists all programs currently running. "ps" probably means programs idk.
- pidof program-name: shows "process id of" program-name provide it is running.
- top: windows task manager like thing in the terminal. To leave top press "q".
- htop: top but with pretty coloured text. If it is not installed already you may be prompted to install it with sudo apt-install htop or something.
- uname: will remind you which operating system you are running in case you forgot.
- ip addr: shows your ip address and some other stuff.
- ping website-address :shows ip address of a website.
- cd - : Go back to previous directory you were on.
- less textfie: less lets you view textfiles in your terminal and to scroll up and down using vim keybings. To leave use q.
- cat textfile: vomits the contents of a text file in the terminal. You can specify more than one textfile like "cat textfile1 textfile2"
- "sudo updatedb" and then "locate": sudo updatedb makes a little index of all the files on your computer and then locate filename lists any files with filename in their filename.
- locate filename | less : you may have to updatedb first. Shows the results of a search in "less" a scrollable form. This is called piping apparently.
- locate filename | grep searchterm : searches for searchterm in the output of locate search. Search in your search.
- df -h | grep media : lists the mounted drives with the term media in them and the amount/percentage of space that is free in them
- "cp dirname/subdir/filename"+".": This will copy filename in the directory you are on. Make sure to add the full stop at the end.
- "cp -iv dirname/subdir/filename"+".": Will do the same as just cp but the -iv means that you will get a confirmation about the copying instead of it just happening in silence.
- cut -d, -f 2,3 : print something in filename which uses the delimeter comma (it is seperated by commas not spaces or brackets or something) and is in the second and the third columns.
- cat textfile | grep Jesus : Is going to print the lines in textfile which have Jesus in them. Don't do this just "grep Jesus textfile".
- cat textfile | grep Jesus | less: Is gonna print out the lines in textfile which have Jesus in a scrollable way. Don't do this just "Grep Jesus textfiel | less".
- cat textfile | tr W J : Prints out textfile but replaces every W with a J. tr means translate or so I am told.
- cat textfile | tr "[:lower]" "[:upper]" : Prints textfile but it is all in uppercase.
- grep Jesus textfile : grep finds Jesus in textfile and prints lines with Jesus in them.
- grep Jesus textfile > jesus.log : Grep finds Jesus in textfile and writes it in jesus.log. Now jesus.log has lines with Jesus in them.
- echo "Jesus" > jesus.log : replaces everything that was in Jesus log with just Jesus.
- ls >> jesus.log: Writes the contents of ls into jesus.log but only after Jesus.
- echo $0: Will tell you which lang your terminal is running on. Probably bash.
- sleep 5 && echo lmao: waits for five seconds and prints lmao.
- Ctrl+C: Will stop whatever process the terminal is running.
- PS1 ="Lol:" : Will set your command prompt to lol. The command prompt is that little bit of text that comes up for you type text afterwards in the terminal.
- diff textfile1 textfile2: Will print out all the lines which are different in textfile1 and textfile2.
- alias r: will check if r is aliased to anything.
- alias r=ranger: Will alias r to ranger, a file manager which you need to install on linux mint.
- rm file: removes file. Deletes it.
- rm file file2: Removes file and file2
- rm -rf directory: Removes a directory without asking you whether to remove it.

## Vim stuff

Vim is God's own true text-editor which runs on windoze 9+1 too. As all tools that God uses it is keyboard driven. That bloated thing called emacs is not a text-editor but rather is a set of tools including a text-editor. It has so many tools it might as well be an operating system running on top of your operating system. Also unless you want to break and deform your hands out of all recognition you are going to use Evil mode on emacs which uses many of vim's good keybindings anyhoo.

- u: undo
- ctrl-r: Redo stuff in Vim
- G: go to the bottom of a document in vim
- gg: go to the top of a document in vim
- shift ZZ: Save and exit in vim
- Shift ZQ: Exit without saving in vim
- vimtutor: Vim Tutorial in Vim
- hjkl: direction keys
- Ctrl+d: Go down half a page.
- Ctrl+u: Go up half a page.
- dd: delete line of text.
- x: backspace in normal mode.
- zz: focus line you are on in the middle of the page
- zt: focus the line you are on to the top of the page
- zb: focus line you are on to the bottom of the page
- i: insert mode, normal typing
- Esc: normal mode, turns keyboard to a kind of control console with keybindings to shortcuts to do stuff.
- swap capslock key in linux mint mate: keyboard->Layout->Options->Capslock behaviour->Swap capslock and esc keys.
- Increase key repeat rate when key is held down (so that you can hjkl fast and furious): keyboard preferences->General->Double the speed slider (it is a pity it doesn't show actual numbers but whatever).
- {,}: Curly brackets to skip between paragraphs.
- A: Puts you in insert mode at the end of the line on the far right.
- i: insert stuff to the left of the cursor
- a: puts you on insert mode on the right of the cursor
- I: Puts you on insert mode on the far left end of the line.
- :x Saves and quits
- :q! Does not save and "force" quits like if you are idiotically editing the same file in two places. It happens to the best of us.
- :w Save but don't exit. w stands for write.
- ggVG: Go to the top and then select everything.
- :sort Sorts every line in alphabetical order
- dw: delete a word. You need to be at the very beggining of a word.
- d$, D: delete the rest of the line to right from the cursor. Just use D like a normal human being. d$ is too many key-preses which reduces maximum comfy.
- $: to go the far right end of the line. I have never used this tbh.
- 0, ^: to go to the far left start of the line. Never used these tbh.
- de: delete to the end of the word. Difference with dw? de will leave two spaces whereas dw will leave only one space. Basically de will leave the spaces at the back and the front of the word whereas dw will delete the space at the back too leaving only one space.
- w,e: move forward between words. w will move the cursor to the start of the word and e will focus it to the end of the word.
- b: move back a word
- db: delete backwards a word.
- d{, d}: delete paragraphs.
- 2w: move you two words forward
- 3e: will move the cursor three words forward with the cursor at the end of the third word.
- d5w: will delete five words forward from where your cursor is.
- d4{: Gonna delete previous 7 number curly bracket paras.
- 4dd: deletes next 4 paragraphs.
- daw: deletes a word and the space around it. The "a" stands for sort of "around" the word in this case desu. Difference with dw?ddw cannot be used when in the middle of a word to delete a word if you try it will just do some wierd shit.
- diw: deletes just the word, not the spaces around it. "i" is sort of for inside.
- dap: Deletes a paragraph
- 5dap: Deletetes 5 paragraphs and the space around them
- dip: Deletes a paragraph but leaves the space around them
- di(, dib: Deletes inside brackets/parenthesis. Useful.
- dab, da(: Deletes inside brackets and the brackets themselves.
- U: to undo a whole line
- Ctrl r: redo
- :earlier5m: Allows you to time travel 5 minutes to the past in vim
- :later5m: Returns back 5 minutes forward in time in vim
- di": Delete inside next quote. Unlike with brakets (di( and dib) you don't need to be in the quote.
- p: paste a line that has been deleted with dd. It will paste stuff after the first letter.
- P: paste stuff before the first letter. Useful.
- V: select a whole line. If you move it, it will select line by line.
- V"ay: Select a whole a whole line and copy it in the "a" register
- "ap: Paste the text saved in the "a" register
- V"+y: Copy text into the "+" register to paste stuff from vim into other applications/vim windows. You need to have gVim (vim-gnome) installed.
- "+p or "+P: To paste text from the "+" register. "P" will paste it infront whereas "p" next to the second character.
- re: replaces the character the cursor is on with "e".
- c: deletes stuff and puts you back in insert mode. How you actually replace stuff.i c is supposed to mean "change" or something.
- cw: deletes word and puts you back into insert mode.
- ci(: deletes inside brackets and puts you back into insert mode
- C, c$: Delet everything to the end of the line from where you are.
- Ctrt+g: in normal mode it will show you your location as in what line number you are on and the % of the document you are on.
- 25%: To go to 25% of the document.
- ' ': To go back to where you were before 25%.
- / : Search. Press "n" to go to the next instance the search term occurs and "N" to go back to the previous instance.
- ? : is search as well except by default it searches backward. "n" will go further up and "N" will go further down.
- o : Start a new paragraph below and go to insert mode. Super Useful.
- O : Add a new paragraph above and go into insert mode.
- % : If you are on "(" and it has a matching ")" it will move you to ")". If you press % again it will move you back to "(".
- :s/old/new/g : Replaces "old" text with "new" text on one line. Without the "g" at the end it will only replace the first occurance of "old" with "new".
- :%s/old/new/g: to change every occurance of "old" with "new" in a file.
- :%s/old/new/gc: to find every occurrence of "old" in the whole file with a promt whether to substitute it or not with "new".
- v: select text visually in visual mode which highlights the text you select visually.
- vap: Select the paragraph you are on visually.
- yap: Copy the whole paragraph you are on without needing to visually select it.
- Ctrl+v: selects inline blocks of text. You will understand what I mean when you try it.
- . : The Full Stop repeats the last command you did. Very Useful.
- y: yank, copy
- yy: copy a whole line
- :norm.: runs the last command on all the lines you have selected.
- R: replace more than one character. Puts you in replace mode. Only useful when replacing stuff with stuff with the same number of characters.
- :setlocal spell spelllang=en_gb: English Language Spell checker. Hilights words with wrong spelling. If you some weirdo who only uses vim for prose and no code then use ":set spell spelllang=en_gb"
- z=: provides suggestions for wrongly spelled words. Use numbers to select which word to replace it with.
- ]s, [s: Go from misspelled word to misspelled word. ]s goes to nnext and [s goes to previous.
- :set nospell: turns spell checking highlighting off.
- y2w: yank 2 words. Copy two words.
- yi(:copy inside brackets
- ya(:yank around brackets. Copies brackets and what's inside them too.
- set ic: makes the search function case insensitive. Very Useful.You can put it into your vimrc file to have it do this by default.
- set noic: Make Search Case-Sensitive Again.
- set hlsearch: highlights search results.
- set nohlsearch: Turn off highlight for search.

## Keyboard Shortcuts/Hotkeys/Keybindings I use

To change keyboard shortcuts on linux mint mate go to the start menu and search for keyboard shortcuts then double click on what you want to change and then enter the keys you wanna use. You can also add new keybindings by clicking add obv.

- Close Window: Super+Shift+c. By "super" I mean the windows key if you are a normal pc user. Also for some reason I am not bothered to find out it will show shift+super+c but it works so whatever.
- Open Terminal: Super+Enter.
- Opens Web Browser: Super+B
- Logs Out: Super+Shift+Q
- Zoom in/out in terminal: This is there by default. Ctrl plus + to zoom and Ctrl - to zoom out. For some reason the + and - in the numpad didn't work with this but the normal ones get the job done so desu.
- Super+P: To open a program with rofi. You will need to sudo apt install rofi. Then go to keyboard shortcuts and add a shortcut named and with the command "rofi -show run" and add the keybinding to Super+P. Hit escape to leave if you don't wanna open anything desu.
- Alt-Tab: To change windows with rofi. Follow the instructions for Super+P but with the name/command "rofi -show window" and reassign the Alt-Tab shortcut to rofi to show all open windows. Hit escape to leave it.
- Super+r: To open ranger, a terminal based file editor. You will need to have ranger installed obv. Go to keyboard shortcuts and add a custom shortcut name/command: "mate-terminal -e ranger".
- Super+n: To open Newsboat, a terminal based RSS feed reade. Add a custom shortcut with name/command: "mate-terminal -e newsboat"

## Other Basic Stuff.

- Remove the menu: Make sure you have the stuff you need the most like settings pinned before this. Right click on it and get rid of it. You can right click on the panel to get the menu back.

- Change rofi theme: You will need to have rofi installed for this. Run rofi -show run or (or the Super+P shortcut if you have added that). Then go to rofi-theme-selector and select your theme with Alt-a desu. The monokai theme looks alright.

- Increase initial terminal size: Go to "Edit" in the menu bar and then to "Profile Preferences." Tick "Use custom default terminal size."Increse the columns to 120 and the rows to 40.

- Install a terminal based file manager like ranger or lf: Ranger is easier to install on linux mint with "sudo install ranger" whereas lf you need to compile it and I am too small-brained for that. If an arch based distro you can get it off the aur or so I am told. To view hidden files in ranger type zh. zh again to hide hidden files. q to quit. jk to go down/up etc... type man ranger in the terminal for the rest.

- Basic system info with os logo in ascii art at terminal startup with neofetch: sudo apt install neofetch then go to your home directory. Show your hidden files through the "view" submenu then go open bashrc with a text editor of your choice. Go to the very bottom, of bashrc and write "neofetch" without the "s. Save and close then open your terminal. At first I was a bit iffy about installing it as it seemed prettier than useful but it is not useless as it shows some useful info I guess. It is certainly pretty though.

- Set up newsboat terminal rss reader: sudo apt install newsboat, then mkdir ~/.newsboat, then cd ~/.newsboat, then vim urls, then paste a url on every line save and exit. To edit rss urls you can always vim ~/.newsboat/urls. To add a custom name to a feed write "~Custom Feed Name" to the end of the URL. You can also add tags by adding "tag name" after the url. When you are in news boat you can press "t" and it will show you a list of tags with the number of unread articles just in those tags. Next to add vim keybindings, autoreload feeds when you startup newsboat, pretty colours, the ability to play youtube/bitchute videos in mpv, limit feeds per feed to 50 then you must go to vim ~/.newsboat/config then paste the stuff below and save and exit. Note: I am using the Brave Browser if you are using some other browser change "brave-browser" as appropiate. To play videos in mpv you will have to type ",m" while your cursor is focused on the vid you wanna play. To find the rss feeds for the youtube channels you can get them by copying "https://www.youtube.com/feeds/videos.xml?channel_id=UCyawG3aTE7RmNQcFQskDWcw" and changing "UCyawG3aTE7RmNQcFQskDWcw" to the youtube's channel id. For bitchute vids copy "https://www.bitchute.com/feeds/rss/channel/veemonro/" and then change "veemonro" to the channel id there. Another easy way to get youtube channel rss feeds is to go to https://invidio.us and click the rss icon. To get rss feeds for twitter users/search-terms go to nitter.net and it's the same story. For a list of my own RSS feeds visit my

   

  RSS Feeds

   

  page.

  ```
  # general settings
  auto-reload yes
  max-items 50
  
  # externel browser
  browser "brave-browser"
  macro m set browser "mpv %u"; open-in-browser ; set browser "brave-browser %u"
   
  # unbind keys
  unbind-key ENTER
  unbind-key j
  unbind-key k
  unbind-key J
  unbind-key K
  
  # bind keys - vim style
  bind-key j down
  bind-key k up
  bind-key j next articlelist
  bind-key k prev articlelist
  bind-key J next-feed articlelist
  bind-key K prev-feed articlelist
  bind-key G end
  bind-key g home
  bind-key d pagedown
  bind-key u pageup
  bind-key l open
  bind-key h quit
  bind-key a toggle-article-read
  bind-key n next-unread
  bind-key N prev-unread
  bind-key D pb-download
  bind-key U show-urls
  bind-key x pb-delete
  
  
  
  # pretty colours
  color background default default
  color listnormal cyan default
  color listnormal_unread blue default
  color listfocus black yellow standout bold
  color listfocus_unread yellow default bold
  color info red black bold
  color article cyan default
  
  # highlights
  highlight article "^(Title):.*$" blue default
  highlight article "https?://[^ ]+" red default
  highlight article "\\[image\\ [0-9]+\\]" green default
  		
  ```

- Increase font size in the mate terminal: Go to edit>Profile Preferences and untick "use system width font".

- Open linux mint software manager from terminal/rofi: mintinstall.

- To install Luke Smith's st terminal build then "cd ~/", "git clone https://github.com/LukeSmithxyz/st", "cd st" and "sudo make install"

- Instructions to install dwm tiling window manager on linux mint :[Link](https://cannibalcandy.wordpress.com/2012/04/26/installing-and-configuring-dwm-under-ubuntu/)[Archived Link](https://archive.is/nq6pU). The version they are installing is 6.0 which is an older one so make sure to get get the latest version instead. Just visit the link they are trying to get you to download and go a directory backwards. You may run into "no such directory" errors but in that case do not despair. Just search the web a little bit for what the hell those missing directories are and install them. Make sure you sudo apt install suckless-tools first so that you can use alt-p to open programs. Also install st terminal. Luke's st terminal is alright so you could install that I guess.

  Also make sure not to disable password login because if you skip the login screen you won't be able to change the desktop enivoronment/window manager and if you don't even have a terminal or dmenu installed then you will be stuck with a black screen and will have to go into recovery mode and restore a previous back up of the system. This happened to me.

  If everything fails then go into the linux text-only console with CtCtrl+Alt+F2 or Ctrl+Alt+F3... You will need to know your profile username rather than just your password. This console thing is called the tty and you can switch from one tty to another with alt-left/right. If you alt left to when you are in tty2 then you will return to where you were before. Try to undo the changes by doing stuff like sudo apt remove dwm or dwm kill all you have made and then alt-left until you reach where you were before or better yet type "reboot" which will restart your computer hopefully in an unfucked state.

  To swap the Capslock and Esc Keys go to home with ~/ then vim ~/.Xmodmap and paste the stuff below here. The reson that this is necessary is because the previous fix in linux mint mate keyboard shortcut settings didn't work when I switched to dwm:

  ```
  ! keycode   9 = Escape NoSymbol Escape
  ! keycode  66 = Caps_Lock NoSymbol Caps_Lock
  
  clear Lock
  keycode 66 = Escape NoSymbol Escape
  
  keycode 9 = Caps_Lock NoSymbol Caps_Lock
  		
  ```

  Then save and exit vim. Then vim .xinitrc and paste "xmodmap .xmodmap" and save and exit. Reboot your computer and then your keyboard is corrected.

  Start Dropbox at startup: For some reason dropbox stopped autostarting when I moved from mate to dwm so I found this little fix: type crontab -e in your terminal. Then paste "@reboot ~/.dropbox-dist/dropboxd" at the bottom of the file and save and exit. Next time you reboot dropbox should start automatically. If it doesn't you can always type start dropbox which will start dropbox just for that terminal just for that session.

- Alias cp to cp -iv then vim ~/.bashrc and type alias cp='cp -iv' and save. The v means be verbose or something.

- Alias r to ranger with vim ~/.bashrc and type alias'r=ranger' and save.

- Alias n to newsboat with vim ~/.bashrc and type alias 'n=newsboat' and save obv.

- Install neocities cli: The neocities cli will allow you to update your neocities website from the terminal. To install the cli tool first sudo apt-get install ruby then sudo then sudo gem install rake and finally sudo gem install neocities. I also git cloned the github repo cd-ied into it and then sudo gem installed neocities but I don't know whether that makes a difference nor am I bothered to find out right now. You can start playing with neocities by typing neocities in your terminal.

- Uninstall Blueberry and install Blueman: I had all sorts of annoying issues with blueberry. I still can't get blueman to autoconnect to my bluetooth speakers but at least I don't need to restart bluetooth and kill pulseaudio because of some broadcom driver bullshit.

- Create a alias to change directory and list files in Dropbox by just typing d: ~/ then vim .bashrc then add "alias d='cd ~/Dropbox && ls'" then save and exit. Finally you can reload .bashrc with "source ~/.bashrc" or you can reboot your computer.

- Alias h to cd ~/: vim .bashrc then add alias h='cd ~/' then save exit and then finally ". ~/bashrc" which is the same as "source ~/.bashrc".
