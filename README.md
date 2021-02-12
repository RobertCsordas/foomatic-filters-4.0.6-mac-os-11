# Mac OS 11 pached version of foomatic-rip

Needed for min12xxw, which itself works without issues. Configure it with --prefix=/usr/local.

It works on Apple Silicon.

# How to install

1. brew install ghostscript a2ps
2. ./configure --prefix=/usr/local/
3. make
4. sudo make install (don't worry about the error at the end)
5. add "Sandboxing Relaxed" to the end of /etc/cups/cups-files.conf

# What is changed?

pdf.c is updated to the new version from cups-filters to be compatible with the newest ghostscript. This required some changes in util.h. Removed redefinition of some string functions.
