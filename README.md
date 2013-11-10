bcpaste
=======

A bash and curl script for pastebin. 
This script implements all paste functions specified in the official api
documented at http://pastebin.com/api


Usage: bcpaste [options] title [filename]

  title           set the title of your paste
  filename        filename of the file to paste, if not given
                  /home/telemin/bin/bcpaste will read from stdin

Options:
  
  -u,--unlisted   default: make unlisted paste (conflicts with -p,-r)
  -p,--public     make public paste (conflicts with -u,-r)
  -r,--private    make private paste (conflicts with -u,-p,-g)

  -e,--expiry=    set expiry time [10M,1H,1D,1W,2W,1M,N]
                  (default N(ever))

  -f,--format=    set format for syntax highlighting, see the 
                  man page, script or pastebin for list, by

  -g,--guest      paste as a guest, does not require an auth
                  token to be generated

  -h,--help       show this help

  -F,--formats    list available syntax highlighting formats

  -a,--auth       authenticate with pastebin.com to generate
                  your user api key, stored at ~/.bcpaste_auth
                  once done, pastes will be made as that user

===============================================================================

TODO:

SSL support for pro users
support for listing of user pastes
support for downloading a specified paste

