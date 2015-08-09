Title: The Current State of Accessibility in Linux Distributions

Most distributions have the packages needed for accessibility in their
repositories.  If they don't, it is likely that they can be added with
little trouble.  The major difference among distributions is not the
packages used, but rather the strategy employed when installing the distro.

There are two major strategies for installation media.
Some distros are accessible out of the box, just like a system running Mac OS X.
In other words, accessibility is at most a few keystrokes away.
Ubuntu is a fine example of this.
But some distros let third parties handle the problem.
For example, Arch Linux does not have an official accessibility project,
but it does have a thriving blind community built around the third-party Talking Arch project.
Both strategies have their merits,
but the first is by far the most popular.

In either case, I will assume that you want a system that starts speaking at some point during the boot process.
Typically, the text-to-speech system is software-based, and you should hear the speech from your default sound card.
Braille is also an option, but the process for making it available at bootup is not as well documented.
In some cases, simply having a USB braille display plugged into your machine
will cause brltty to start and be properly configured at boot.
Likewise, we need more docs on magnification.

# Distributions with Out-of-the-box Accessibility

## Ubuntu

Boot the live media.  Wait until you hear a bongo sound, and then press
alt+super+s to start Orca, the Gnome screen reader.
Note that the super key is also the windows key.
Can it be any easier than that?
From here, you can either play around in the live environment or install Ubuntu to a hard disk.
If you choose to install Ubuntu, you can enable Orca permanently so that
it will always start at boot.
Presumably, you should be able to do the same for screen magnification.
[Visit the Ubuntu accessibility page](https://help.ubuntu.com/community/Accessibility) for more details.

## Debian

If you have the Debian netinst CD, try pressing s and then enter at the
isolinux prompt.  That didn't work when I tried it just now.  What
did work was hitting the escape key, and then typing `installspk` (to install
on i386) or `amd64-installspk` (for AMD64), followed by pressing enter.
This brings up the installer with speech.
But see below for an alternative method of installing Debian.

## Grml

Grml is a live Linux system tailored to system administrators.
It can also be installed to the hard disk, or you can run debootstrap from Grml
to install Debian to a hard disk.  Grml has been very popular within the blind community
over the years.  Simply type grml swspeak at the Isolinux prompt, and the system
will come up in console mode with a text-to-speech system speaking via your sound card.

Its home page is [grml.org](https://grml.org).

## Gentoo

The Gentoo installation media can be used with speech in console mode.
Enter the following incantation at the isolinux prompt:
`gentoo speakup.synth=soft`.
Also note that it is pretty straightforward to install Gentoo using
non-Gentoo media, so this is an option for those who need it.

## Fedora and RHEL

TODO.  Need to talk to a friend who has experience with RH.
At one time, if you wanted to install Fedora, you used third-party
media from the [speakupmodified site](http://speakupmodified.org).
They aren't distributing anything these days, and apparently even
Fedora's graphical installer has become accessible.

# Customized Distros and Third-party Media

## TalkingArch

TalkingArch is an unofficial modification of the Arch Linux install media,
providing text-to-speech or braille output during the installation process.
The philosophy behind TalkingArch is that in the common case, the
user shouldn't have to type anything at a boot prompt.  It should be
"plug and play", rather than "blindly mash keys and pray".
You can find the TalkingArch homepage at [talkingarch.tk](http://talkingarch.tk/).
Follow the links to the Arch Linux wiki for a detailed article describing
how to do an eyes-free installation of Arch Linux.
TalkingArch is also useful on rescue media, in case you need to repair
an existing installation.

(Probably some overly strong wording there ... TalkingArch was my baby after all).

## Vinux

Vinux is a full-fledged Linux distribution derived from Ubuntu.
Its home page is [vinuxproject.org](http://vinuxproject.org),
and this is what its creaters have to say about it:

> Vinux is a Ubuntu derived distribution optimised for the needs of blind and
> partially sighted users. By default Vinux provides two screen-readers,
> Braille display support and a friendly community.
> When you boot the live Vinux image, you will be greeted by the Orca screen
> reader enabling you to navigate the graphical Gnome desktop using keyboard commands.

