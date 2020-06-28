# :sunglasses:	 vimconfig 
My personal .vimrc file with many useful plugins. <br>
 * I'm using _**macOS its version : Catalina 10.15.5**_ <br>
 * I uploaded it to backup my config. _Do not ever use my .vimrc file, it is chaotic_ :exploding_head:	

Check these out to get better results : https://github.com/amix/vimrc, https://devhints.io/vimscript <br>
Make your own or try to get it from the link above.

![Alt text](pngs/macOS/main/Screen%20Shot%20Unity%20C%23%20at%20Latest%20.png
"vim-unity-c#-main")


### Color Cheatsheet (Xterm)
[List of 256 colors](https://jonasjacek.github.io/colors/) <br>

###  Plugins 

* [YouCompleteMe](https://github.com/ycm-core/YouCompleteMe) <br> 
* [delimitMate](https://github.com/Raimondi/delimitMate) <br>
* [indentLine](https://github.com/Yggdroot/indentLine) <br>
* [Vundle.vim](https://github.com/VundleVim/Vundle.vim) <br>
* [Dracula](https://github.com/dracula/vim)
* [OpenGL](https://github.com/beyondmarc/opengl.vim)
* [Zenburn](https://github.com/jnurmine/Zenburn)
* [lua-support](https://github.com/wolfgangmehner/lua-support)
* [vim-lua-ftplugin](https://github.com/xolox/vim-lua-ftplugin)
* [vim-misc](https://github.com/xolox/vim-misc)
* [vim-airline-themes](https://github.com/vim-airline/vim-airline-themes)
* [indentpython.vim](https://github.com/vim-scripts/indentpython.vim)
* [ctrlp](https://github.com/kien/ctrlp.vim)
* [vim-codefmt](https://github.com/google/vim-codefmt) <br>
* [vim-glaive](https://github.com/google/vim-glaive) <br>
* [vim-maktaba](https://github.com/google/vim-maktaba) <br>
* [nerdtree](https://github.com/preservim/nerdtree) <br>
* [tagbar](https://github.com/majutsushi/tagbar) <br>
* [vim-airline](https://github.com/vim-airline/vim-airline) <br>
* [syntastic](https://github.com/vim-airline/vim-airline) <br>
* [SimpylFold](https://github.com/tmhedberg/SimpylFold) <br>
* [vim-flake8](https://github.com/nvie/vim-flake8) <br>
* [gruvbox](https://github.com/morhetz/gruvbox) <br>
* [vim-glsl](https://github.com/tikhomirov/vim-glsl) <br>
* [vim-fugitive](https://github.com/tpope/vim-fugitive) <br>
* [vim-todo-lists](https://github.com/aserebryakov/vim-todo-lists) <br>
  
## Key Mappings
**Leader** key is backslash ("\\")

map <leader>g  :YcmCompleter GoToDefinitionElseDeclaration `<CR>`
<br>
map <F2> :NERDTreeToggle<CR> <br> 
map <buffer> <F9> :w<CR>:exec '!python3' shellescape(@%, 1)`<CR>`<br>
<buffer> <F9> <esc>:w<CR>:exec '!python3' shellescape(@%, 1)`<CR>`

# Love2d (Löve) support
Biggest advantage is my config is that to launch love in vim by single keyboard stroke.
There is a [plugin](https://gist.github.com/davisdude/0f46c9c00917fc5c53bb) with 105 LOC
and it is probably better solution but i didn't get the code well (i am newbie) 
and tried to make my own and it took only 2 lines of code. 

Do not forget to set $PATH variable for love2d.

Press F5 to launch love and pass your current buffer's path as arg
Let's say, your buffer's path is ~/Desktop/game/main.lua
F5 will run love ~/Desktop/game/ 
that's it.
`au Filetype lua nmap <buffer> <F5> :call RunLove() <CR>` 

This function does the job.
`function RunLove()
    :lcd %:p:h
    :!love `pwd`
endfunction`

Lua scripts remember love functions by a dictionary
[Dictionary Link](https://raw.githubusercontent.com/josefnpat/dotfiles/master/config/vim/vim/love-dictionary/love.dict)
Put dictionary file under the .vim/love-dictionary/ directory.
<b> :!lua % <b>

## ScreenShots

There are screenshots of environments with different colorschemes. I've installed same vim plugins on macOS and ubuntu. <br>
<br> *Here is the results of my .vimrc configuration on two different OS.*

<br> **Color Schemes** <br>
* Onedark
* Gruvbox
* Koehler
* Zenburn
* Dracula

# macOS

### Gruvbox

 ![Alt text](pngs/macOS/Screen%20Shot%20Gruvbox%20Single%202020-06-27%20at%20Latest.png
 "vim-gruvbox-single")

 ![Alt text](pngs/macOS/Screen%20Shot%20Gruvbox%20Split%20Windows%202020-06-27%20at%20Latest.png 
 "vim-gruvbox-splitw")

### Onedark

![Alt text](pngs/macOS/Screen%20Shot%20OneDark%20Single(VISUAL)%202020%20at%20Latest.png
 "vim-onedark-single")

### Koehler
 
 ![Alt text](pngs/macOS/Screen%20Shot%20Koehler%20Single%20Latest%20at%20Latest.png
 "vim-koehler-single")

### Zenburn

![Alt text](pngs/macOS/Screen%20Shot%20Zenburn%20Single%202020-06-27%20at%20Latest.png
"vim-zenburn-single")

# Ubuntu

## Gruvbox

![Alt text](pngs/ubuntu/Screenshot%20from%20linux(0).png
"linux0")

## Koehler

![Alt text](pngs/ubuntu/Screenshot%20from%20linux(1).png
"linux0")

## Zenburn

![Alt text](pngs/ubuntu/Screenshot%20from%20linux(2).png
"linux0")

## Onedark
![Alt text](pngs/ubuntu/Screenshot%20from%20linux(3).png
"linux0")

## Dracula
![Alt text](pngs/ubuntu/Screenshot%20from%20linux(4).png
"linux0")


# *STRONGLY* recommended plugin 
##  [vim-todo-lists is a Vim plugin for TODO lists management.](https://github.com/aserebryakov/vim-todo-lists)
Create a file with .todo extension, leave the rest to plugin. <br>
<br>I added those lines to .vimrc to insert date automatically when a task is created:<br>
`let g:VimTodoListsDatesEnabled = 1` <br>
`let g:VimTodoListsDatesFormat = "%a %d, %Y"`

![Alt text](pngs/macOS/main/Screen%20Shot%20todo%20at%20Latest.png
"vim-todo-main")

***Baddest text editor on the planet!***

