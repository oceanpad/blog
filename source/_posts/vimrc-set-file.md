---
title: vimrc set file
date: 2016-05-10 00:10:04
tags:
---
*This is my .vimrc set file:

*start from here

runtime! debian.vim
if has("syntax")
  syntax on 
endif

colo slate
set tabstop=2
set softtabstop=2
set shiftwidth=2
set autoindent
set nu
set clipboard=unnamedplus
set hlsearch
set wildmenu
set background=dark
set laststatus=2
set runtimepath^=~/.vim/bundle/ctrlp.vim	"crtl+p
set showcmd		" Show (partial) command in status line.
set showmatch		" Show matching brackets.
set ignorecase		" Do case insensitive matching
set smartcase		" Do smart case matching
set cursorline          " highlight current line
set incsearch		" Incremental search
"set autowrite		" Automatically save before commands like :next and :make
"set hidden		" Hide buffers when they are abandoned
"set mouse=a		" Enable mouse usage (all modes)

" Source a global configuration file if available
if filereadable("/etc/vim/vimrc.local")
  source /etc/vim/vimrc.local
endif

set nocompatible              " be iMproved, required
filetype on                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'VundleVim/Vundle.vim'
Plugin 'tpope/vim-fugitive'
Plugin 'elzr/vim-json'
Plugin 'lokaltog/vim-powerline'
Plugin 'scrooloose/nerdtree'
"Plugin 'vim-airline/vim-airline'
"Plugin 'vim-airline/vim-airline-themes'

call vundle#end()            " required
filetype plugin indent on    " required
* end at here 
