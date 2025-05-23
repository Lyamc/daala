# Build instructions on MingW64 (MSYS2)

```
pacman -S automake autoconf git mingw-w64-x86_64-gcc libtool mingw-w64-x86_64-SDL2_gfx mingw-w64-x86_64-libogg mingw-w64-x86_64-libjpeg-turbo mingw-w64-x86_64-libpng mingw-w64-x86_64-check
git clone https://github.com/xiph/daala
cd daala
./autogen.sh
./configure --host=x86_64-w64-mingw32
make
make tools # optional
mv examples/encoder_example.exe daalaenc.exe
mv examples/player_example.exe daaladec.exe
mv examples/dump_video.exe daaladump.exe
```



# Daala next-generation video codec

Daala is the codename for a new video compression technology. The effort is a
collaboration between the Mozilla Foundation, the Xiph.Org Foundation and any
other contributors that wish to help. The goal of the project is to provide a
video format that's free to implement, use and distribute, and a reference
implementation with technical performance superior to H.265.
For more information, see the [Daala wiki][wiki].

To get a sense of how well Daala performs in comparison to other codecs, check
out [Are We Compressed Yet?][awcy]

[awcy]: https://arewecompressedyet.com/
[wiki]: https://wiki.xiph.org/Daala
![Tiger barfing rainbows](https://people.xiph.org/~greg/a.png)

## Hacking on Daala

The wiki has quickstart pages for [Linux/OS X][posix], [Windows][win], and
[Windows MinGW64][mingw].

Daala uses the [GitHub Issue Tracker][issues] and the [Rietveld][code review]
code review tool. [Jenkins][jenkins] is used for continuous integration.

[posix]: https://wiki.xiph.org/Daala_Quickstart
[win]: https://wiki.xiph.org/Daala_Quickstart_Windows
[mingw]: https://wiki.xiph.org/Daala_MinGW64_Environment
[issues]: https://github.com/xiph/daala/issues
[code review]: https://review.xiph.org/
[jenkins]: https://mf4.xiph.org/jenkins/view/daala/

## Getting in Touch

There's an IRC channel #daala on chat.freenode.org. If you don't have IRC set
up you can easily connect from your [web browser][webchat].

You can also subscribe to the [daala mailing list][email].

[webchat]: http://webchat.freenode.net/?channels=%23daala
[email]: http://lists.xiph.org/mailman/listinfo/daala
