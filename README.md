# opendoom

opendoom aims to accurately reproduce the original DOS version of
Doom and other games based on the Doom engine in a form that can be
run on modern computers. We are open to supporting any execution
environment.

Originally, opendoom was only a Doom source port. The project
now includes ports of Heretic and Hexen, and Strife.

opendoom’s aims are:

 * To always be 100% Free and Open Source software.
 * Portability to as many different operating systems as possible.
 * Accurate reproduction of the original DOS versions of the games,
   including bugs.
 * Compatibility with the DOS demo, configuration and savegame files.
 * To provide an accurate retro “feel” (display and input should
   behave the same).

More information about the philosophy and design behind opendoom
can be found in the PHILOSOPHY file distributed with the source code.

## Setting up gameplay

For instructions on how to set up opendoom for play, see the
INSTALL file.

## Configuration File

opendoom is compatible with the DOS Doom configuration file
(normally named `default.cfg`). Existing configuration files for DOS
Doom should therefore simply work out of the box. However, opendoom
also provides some extra settings. These are stored in a separate
file named `opendoom.cfg`.

The configuration can be edited using the opendoom-setup tool.

## Command line options

opendoom supports a number of command line parameters, including
some extras that were not originally suported by the DOS versions. For
binary distributions, see the CMDLINE file included with your
download; more information is also available on the opendoom
website.

## Playing TCs

With Vanilla Doom there is no way to include sprites in PWAD files.
opendoom’s ‘-file’ command line option behaves exactly the same
as Vanilla Doom, and trying to play TCs by adding the WAD files using
‘-file’ will not work.

Many Total Conversions (TCs) are distributed as a PWAD file which must
be merged into the main IWAD. Typically a copy of DEUSF.EXE is
included which performs this merge. opendoom includes a new
option, ‘-merge’, which will simulate this merge. Essentially, the
WAD directory is merged in memory, removing the need to modify the
IWAD on disk.

To play TCs using opendoom, run like this:

```
opendoom -merge thetc.wad
```

Here are some examples:

```
opendoom -merge batman.wad -deh batman.deh vbatman.deh  (Batman Doom)
opendoom -merge aoddoom1.wad -deh aoddoom1.deh  (Army of Darkness Doom)
```

## Other information

 * opendoom includes a number of different options for music
   playback. See the README.Music file for more details.

 * More information, including information about how to play various
   classic TCs, is available on the opendoom website:

     https://www.opendoom.org/

   You are encouraged to sign up and contribute any useful information
   you may have regarding the port!

 * opendoom is not perfect. Although it aims to accurately
   emulate and reproduce the DOS executables, some behavior can be very
   difficult to reproduce. Because of the nature of the project, you
   may also encounter Vanilla Doom bugs; these are intentionally
   present; see the NOT-BUGS file for more information.

   New bug reports can be submitted to the issue tracker on Github:

     https://github.com/opendoom/opendoom/issues

 * Source code patches are welcome, but please follow the style
   guidelines - see the file named HACKING included with the source
   distribution.

 * opendoom is distributed under the GNU GPL. See the COPYING
   file for more information.

 * Please send any feedback, questions or suggestions to
   opendoom-dev-list@opendoom.org. Thanks!
