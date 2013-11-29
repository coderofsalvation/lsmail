lsmail
======

deadsimple console imapclient (think: ls my@gmail.com ) written in bash &amp; php

### Usage ###

    $ lsmail my@email.com 
    
    id    date                     from             subject 
    ----  ----                     ----             ---- 
    7331  2013-11-29 Fri 10:11:15  flopse@foobars. [issue165] flopedia flopjes api 
    7330  2013-11-29 Fri 09:11:18  Babce@bflaoer   Freedom 
    7329  2013-11-28 Thu 18:11:58  flopse@foobars. [issue954] flop XML Integration 
    7328  2013-11-28 Thu 17:11:38  flopse@foobars. [issue165] flopedia flopjes api 
    7327  2013-11-28 Thu 15:11:35  Babce@bflaoer   FW: flop rates 
    7326  2013-11-28 Thu 14:11:54  flopse@foobars. [issue165] flopedia flopjes api 
    7325  2013-11-28 Thu 14:11:15  flopse@foobars. [issue165] flopedia flopjes api 
    7324  2013-11-28 Thu 10:11:31  flopse@foobars. [issue954] flop XML Integration 
    7323  2013-11-27 Wed 16:11:41  fg@foobars.com  Fwd: RE: Skype new account 
    7322  2013-11-27 Wed 16:11:16  fg@foobars.com  Re: lorem ipsum 

    lsmail> 7331

    subject        : [issue165] flopedia flopjes api 
    fromaddress    : "Matt Jown" <matt@gmail.com>
    toaddress      : you@gmail.com 
    ccaddress      : 
    date           : Fri, 29 Nov 2013 09:05:14 +0000

    If chuck norris is really that good, then he would be able to come down 
    my house and bash my brains out while I'm typing this amas;ldkfjaksjdlkfjsldf...
    ;lksjfkjs;df....sdfjahldifuayreiwhtkwjejer.....asdjfio8ewlilkhgtwlkert....lakjshdfk..
    alsdfjhalksdjhfalksjdhf..i   asd.faerfhwhlewiauhfiuhaelirufh....

    $ lsmail
    
    [my@email.com]
    
    id    date                     from             subject 
    ----  ----                     ----             ---- 
    7331  2013-11-29 Fri 10:11:15  flopse@foobars. [issue165] flopedia flopjes api 
    7330  2013-11-29 Fri 09:11:18  Babce@bflaoer   Freedom 
    7329  2013-11-28 Thu 18:11:58  flopse@foobars. [issue954] flop XML Integration 
    7328  2013-11-28 Thu 17:11:38  flopse@foobars. [issue165] flopedia flopjes api 

    [other@foo.com]

    id    date                     from             subject 
    ----  ----                     ----             ---- 
    7331  2013-11-29 Fri 10:11:15  flopse@foobars. [issue165] flopedia flopjes api 
    7330  2013-11-29 Fri 09:11:18  Babce@bflaoer   Freedom 
    7329  2013-11-28 Thu 18:11:58  flopse@foobars. [issue954] flop XML Integration 
    7328  2013-11-28 Thu 17:11:38  flopse@foobars. [issue165] flopedia flopjes api 

### why ###

* sometimes we need to keep things deadsimple 
* bash automation / monitoring / notification
* easily checking multiple emailboxes

CREDITS: [imapmunch](https://gist.github.com/coderofsalvation/4604003)

### requirements ###

* bash 
* php 

### Installation ###

    mkdir ~/bin 
    cd /tmp
    git clone https://github.com/coderofsalvation/lsmail.git
    cd lsmail 
    cp imapmunch lsmail ~/bin/.
    cp ~/.lsmail.my@example.com ~/.lsmail.my@gmail.com 
    # now modify ~/.lsmail.my@gmail.com 
    (..)
    # set permissions
    chmod 600 ~/.lsmail.*

### Note ###

Put this in ~/.profile so you always have handson-access to your personal bashscripts in ~/bin:

     PATH="$HOME/bin:$PATH"

### Planned features ###

* easily download attachments (already implemented, not finished)
* hastag/price/currency/scanning in subject
* csv/json output
