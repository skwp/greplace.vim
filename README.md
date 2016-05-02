VIM Plugin for doing a search and replace across many files.

## About this plugin

Original plugin by Yegappan Lakshmanan
http://www.vim.org/scripts/script.php?script_id=1813

Modifications by Yan Pritzker:
 * Always grep recursive
 * Silence the search so you don't get a gigantic scroll list

## Usage
1.  Use :Gsearch <search>  to get a buffer window of your search results
2.  then you can make the replacements inside the buffer window using traditional tools (%s/foo/bar/) 
3.  Invoke :Greplace to make your changes across all files. It will ask you interatively y/n/a - you can hit 'a' to do all.
4.  Save changes to all files with `:wall` (write all)

## Customization

To customize command used for `:Gsearch` you can update both the command and
the default options.

_Note_: updating `grepprg` will have consequences on other
commands that rely on `grep` vim command

  * [git grep](https://www.kernel.org/pub/software/scm/git/docs/git-grep.html)

        set grepprg=git\ grep

        let g:grep_cmd_opts = '--line-number'

  * [ag](https://github.com/ggreer/the_silver_searcher)

        set grepprg=ag

        let g:grep_cmd_opts = '--line-numbers --noheading'

  * [ack](http://beyondgrep.com/)

        set grepprg=ack

        let g:grep_cmd_opts = '--noheading'

