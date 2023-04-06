
 
Installation: 

$git clone https://github.com/Gamekiller17/crunch
$cd crunch
$sudo make && make install


Usage: $crunch <minimum-length> <maximum-length> [<characters>] [options]

[characters]
    abcd... = Lowercase letters, ABCD... = Uppercase letters, 0123... = Numbers, @!#$... = Symbols, \ = Space, " " = Space

Options: [-b <number><sizetype>] [-c <number>] [-d <number><pattern>] [-e <string>] [-f <file>] [-i] [-l] [-o <file>] [-p <charset>] [-q <file>] [-r] [-s] [-t <pattern>] [-u] [-z <method>]

[Options]
    -b <number><sizetype>          : maximum bytes to write to output file. depending on the blocksize
                                     files may be some bytes smaller than specified but never bigger.
    -c <number>                    : Specifies the number of lines in output file. Required: [-o START]
    -d <number><pattern>           : Limits character duplicate limit
    -e <string>                    : String to end at
    -f <file>                      : Specifies character set from a charset.lst file
    -i                             : Inverts the output from left to right to right to left
    -l                             : Specifies pattern symbols as literals. Required: [-t]
    -o <file>                      : Specifies output file
    -p <charset>                   : Generate characters that don't have repeating characters
    -p <word1> <word2> <word3> ... : Generate words that don't have repeating characters
    -q <file>                      : Same as [-p] but words/characters are taken from a file
    -r                             : Resume from a specified output file. Required: [-o]
    -s <string>                    : String to start from
    -t <pattern>                   : Specifies pattern
        [Patterns]
        @ = Lowercase letters
        , = Uppercase letters
        % = Numbers
        ^ = Symbols
    -u                             : Disables the printpercentage thread
    -z <method>                    : Compress output file
        [Methods]
        gzip    => Speed = Fast,     Compresstion = Low
        bzip2   => Speed = Moderate, Compresstion = Medium
        7z      => Speed = Slow,     Compresstion = High


Compiles on: Should compile in any x86 or x64 Linux machine if needed compilers are installed (gcc, make)
