# VimConfig
```vim
" 修改leader键
let mapleader = ','
let g:mapleader = ','

set nu
syntax on
set autoindent
set encoding=utf-8

" 设置文内智能搜索提示
" 高亮search命中的文本
set hlsearch
" 打开增量搜索模式,随着键入即时搜索
set incsearch
" 搜索时忽略大小写
set ignorecase
" 有一个或以上大写字母时仍大小写敏感
set smartcase

" 检测文件类型
filetype on
" 针对不同的文件类型采用不同的缩进格式
filetype indent on
" 允许插件
filetype plugin on
" 启动自动补全
filetype plugin indent on

" 取消备份。 视情况自己改
set nobackup
" 关闭交换文件
set noswapfile

" 鼠标暂不启用, 键盘党....
set mouse-=a

" Quickly close the current window
nnoremap <leader>q :q<CR>

" Quickly save the current file
nnoremap <leader>w :w<CR>

call plug#begin('~/.vim/plugged')
Plug 'scrooloose/nerdtree'
call plug#end()

map <F10> :NERDTreeToggle<CR>
au VimEnter * NERDTree
```
