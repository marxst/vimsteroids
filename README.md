# vimsteroids: My vim setup for python, puppet, ansible and related...

## What is it good for?

This is my setup for working within a devops group, taking care of a
heavily distributed system, consisting of a lot of python code, namely
openstack components, managed by puppet, orchestrated by ansible, you get
the idea ;-)

## How the thing was born

I started with the hints from [this article](https://realpython.com/blog/python/vim-and-python-a-match-made-in-heaven/)
and was very impressed by the [tagbar feature](http://majutsushi.github.io/tagbar/) 
and found out, that this is easy to adapt to puppet and other languages. I also
found some rudimentary ansible support, so I decided to complement the python 
setup with some vim plugins for puppet and ansible.

I think so far it works pretty well, at least for me, despite being far from
complete. Feel free to fork or contribute ;-)

## How to get started

First of all you should backup your current vim setup, in case you do not like what
 I did.

After that just copy the `.vimrc` file and install the [vundle](https://github.com/VundleVim/Vundle.vim) plugin manager:
```bash
$ git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
If you have done that, open vim and type
```vim
:PluginInstall
```
This will fetch all the needed plugins from github and activate them properly.

Do not forget to read the install procedure for the [YouCompleteMe](https://github.com/Valloric/YouCompleteMe) plugin
and configure it for all the languages you might want it for.

Finally copy the `.ctags` file to your home directory. There is a [list of more 
languages for ctags support](https://github.com/majutsushi/tagbar/wiki) in the wiki of tagbar.

In the `colors` subdirectory you can find my preferred colorscheme, [jelly-beans](https://github.com/nanotech/jellybeans.vim).

## Some Key mappings

`SPACE` folds and unfolds code based on indendation.

`F3` toggles line numbering.

`F4` opens and closes [NERDTree](https://github.com/scrooloose/nerdtree), a file manager.

`F8` opens and closes the tagbar

The keys for movement between different windows splits are remapped from `CTRL``W``direction` to `CTRL``direction`, the directions being the standard vim direction keys `h,j,k,l`.
