" Turn on syntax highlight
syntax on


" Line number 
set number
highlight LineNr term=bold cterm=NONE ctermfg=DarkGrey ctermbg=NONE gui=NONE guifg=DarkGrey guibg=NONE
 
" Encoding
set encoding=utf-8

" Whitespace
set wrap
set textwidth=80
set formatoptions=tcqrn1
set tabstop=2
set softtabstop=2
set expandtab
set noshiftround

" Plugins

" Status Line
set laststatus=2
set t_Co=256
let g:lightline = {
      \ 'colorscheme': 'deus',
      \ }

" NERDTree
autocmd StdinReadPre * let s:std_in=1
autocmd VimEnter * if argc() == 0 && !exists('s:std_in') | NERDTree | endif


if (empty($TMUX))
  if (has("termguicolors"))
    set termguicolors
  endif
endif

" Dracula colorscheme
packadd! dracula
syntax enable
colorscheme dracula
