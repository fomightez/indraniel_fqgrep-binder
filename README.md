
# indraniel_fqgrep-binder
Analysis of sequencing data via if indraniel/fqgrep (An approximate sequence pattern matcher for FASTQ/FASTA files) in Jupyter sessions provided via MyBinder.org. Adapt the demonstrations to analyze your data and create reports.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/indraniel_fqgrep-binder/master?urlpath=%2Flab%2Ftree%2Fdemo.ipynb)


*tl;dr:*  
Click any `launch binder` badge on this page to use the demonstrations inside your browser.


**Note if you are interested in , see [my fqgrep-binder repo](https://github.com/fomightez/fqgrep-binder) where I demonstrate that. I also mention Patmatch which belongs in discussions of this sort of software; however, Patmatch only works with FASTA files.


--------

SYNOPSIS
========

'fqgrep' is an approximate sequence pattern matcher for FASTQ/FASTA files.  
One can think of it as being a grep (http://en.wikipedia.org/wiki/Grep)  
and agrep (http://en.wikipedia.org/wiki/Agrep) like tool optimized  
for FASTQ (http://en.wikipedia.org/wiki/FASTQ_format) and FASTA  
(http://en.wikipedia.org/wiki/FASTA_format) files. It can work directly  
on both compressed and uncompressed file types.  

Below is the help message via ('fqgrep -h') describing its usage:  

Usage: fqgrep [options] -p <pattern> <fastq_or_fasta_files>  
        -h                  This help message  
        -V                  Program and version information  
        -p <STRING>         Pattern of interest to grep [REQUIRED]  
        -v                  Invert match - show only sequences that  
                            DO NOT match the pattern  
        -a                  Show all records irregardless of match status  
                            Useful in conjunction with the -r option;  
                            when one would like to do further post-processing  
                            of the match data  
        -c                  Highlight matching string with color  
        -f                  Output matches in FASTA format  
        -r                  Output matches in detailed stats report format  
        -b <STRING>         Delimiter string to separate columns  
                            in detailed stats report [Default: '\t']  
        -m <INT>            Total number of mismatches to at most allow for  
                            in search pattern [Default: 0]  
        -s <INT>            Max threshold of substitution mismatches to allow  
                            for in search pattern [Default: unlimited]  
        -i <INT>            Max threshold of insertion mismatches to allow for  
                            in search pattern [Default: unlimited]  
        -d <INT>            Max threshold of deletion mismatches to allow for  
                            in search pattern [Default: unlimited]  
        -S <INT>            Cost of base substitutions in obtaining  
                            approximate match [Default: 1]  
        -I <INT>            Cost of base insertions in obtaining  
                            approximate match [Default: 1]  
        -D <INT>            Cost of base deletions in obtaining  
                            approximate match [Default: 1]  
        -e                  Force tre regexp engine usage  
        -C                  Display only a total count of matches  
                            (per input FASTQ/FASTA file)  
        -o <out_file>       Desired output file.  
                            If not specified, defaults to stdout  

PREREQUISITES  
============= 

"fqgrep" depends upon the following libraries:  

  * TRE Regular Expression Library (TRE)  
    [http://laurikari.net/tre/] version 0.8.0.  
  * zlib  
    [http://www.zlib.net]  

They will need to be available on your system before fqgrep can be
installed.

    TRE
    ===

        On Ubuntu (or any other Debian-based Linux distribution):
        ---------------------------------------------------------
        
            sudo apt-get install libtre-dev libtre5

        On Mac OS X 
        -----------
    
        via macports [http://www.macports.org/] :
    
            sudo port install tre
    
        or via homebrew [http://brew.sh] :
    
            brew install tre
    
        or via compiling direct source code:
    
            wget http://laurikari.net/tre/tre-0.8.0.tar.gz
            tar -zxvf tre-0.8.0.tar.gz
            cd tre-0.8.0
            ./configure
            make
            sudo make install
    
        Other Alternative Operating Systems
        -----------------------------------
        
        For other installation alternatives please visit the following web site:
    
            http://laurikari.net/tre/download/
    
    zlib
    ====

    On Ubuntu (or any other Debian-based Linux distribution):

        sudo apt-get install zlib1g zlib1g-dev
        
    On Mac OS X the zlib library comes pre-installed. 

Usage of the example trimmer, fqgrep-trim.pl, provided in the scripts
subdirectory of this git repository, may require the installation of the
'Path::Class' perl module (found on CPAN) onto your system.

As the root user, please try the following terminal command for
"Path::Class" installation:

     cpan Path::Class

INSTALLATION
============

The installation process currently consists of a very simple Makefile.

Just do the following:

git clone git://github.com/indraniel/fqgrep.git;
cd fqgrep;
make; # try 'make genome'   if at the Genome Center at Washington University
      #                     or would like to create an executable with all the
      #                     relevant libraries statically compiled into it
      #
      # try 'make macports' if installing on Mac OS X and you installed the
      #                     TRE library via macports (http://www.macports.org/)

The 'fqgrep' executable should be in the working directory.
Afterwards, you can move the executable to wherever you wish.
Usually, this is the directory "/usr/local/bin" .

USAGE & DETAILS
===============

For more information about fqgrep and its associated scripts, please
visit the following documentation page:

https://github.com/indraniel/fqgrep/wiki


AUTHOR
======

Indraniel Das (indraniel at gmail dot com)

ACKNOWLEDGEMENTS
================

This software was developed at the Genome Center at Washington
University, St. Louis, MO.

Thanks to the Genome Center's Technology Development Informatics
Group (Jasreet Hundal, Jason Walker, and Todd Wylie) for insightful
discussions and feedback.

DISCLAIMER
==========

This software is provided "as is" without warranty of any kind.

DOI INFO
========

https://zenodo.org/badge/latestdoi/20108/indraniel/fqgrep


Created: March 15, 2011
