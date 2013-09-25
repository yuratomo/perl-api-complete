perl-api-complete
=================
Vim omnifunc for perl api.

Install
-------
Set your .vimrc as follows.

    " Vundle
    Bundle 'git://github.com:yuratomo/perl-api-complete.git'

Settings
--------
Set your .vimrc as follows.
### autoload perl-api-complete
    au BufNewFile,BufRead *.pl   setl omnifunc=perlapi#complete
    
### show status refarence
    au CompleteDone *.pl         call perlapi#showRef()
    au BufNewFile,BufRead *.pl   inoremap <expr> <c-down> perlapi#nextRef()
    au BufNewFile,BufRead *.pl   inoremap <expr> <c-up>   perlapi#prevRef()

### balloon help
    if has("balloon_eval") && has("balloon_multiline") 
      au BufNewFile,BufRead *.pl setl bexpr=perlapi#balloon()
      au BufNewFile,BufRead *.pl setl ballooneval
    endif
    
ScreenShots
----------

