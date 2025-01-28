git-authors(1) -- Generate authors report
=================================================

## SYNOPSIS

`git-authors` [-a, --all] [-l, --list] [--no-email]

## DESCRIPTION

  Populates the file matching _authors|contributors -i_ with the authors of commits, according to the number of commits per author.

  See the "MAPPING AUTHORS" section of **git-shortlog**(1) to coalesce together commits by the same person.

## OPTIONS

  -a, --all

  Show all variants of user and email

  -l, --list

  Show authors.

  --no-email

  Don't show authors' email.

  --no-[use-]mailmap

  Don't respect the .mailmap file (this is helpful to validate that your mailmap file is working)

## EXAMPLES

  Updating AUTHORS file:

    $ git authors

  Listing authors:

    $ git authors --list
    TJ Holowaychuk <tj@vision-media.ca>
    hemanth.hm <hemanth.hm@gmail.com>
    Jonhnny Weslley <jw@jonhnnyweslley.net>
    nickl- <github@jigsoft.co.za>
    Leila Muhtasib <muhtasib@gmail.com>

  Listing authors without email:

    $ git authors --list --no-email
    TJ Holowaychuk
    hemanth.hm
    Jonhnny Weslley
    nickl-
    Leila Muhtasib

  * Validate that your .mailmap file is working:

    $ diff <(git authors -l -a --no-mailmap) <(git authors -l -a)

## AUTHOR

Written by Titus Wormer &lt;<tituswormer@gmail.com>&gt;

## REPORTING BUGS

&lt;<https://github.com/tj/git-extras/issues>&gt;

## SEE ALSO

&lt;<https://github.com/tj/git-extras>&gt;
