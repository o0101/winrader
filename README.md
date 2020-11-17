# winrader

Windows 95 in [Grader.JS](https://github.com/c9fe/graderjs). Yep, it's the whole thing. I'm not sorry. 

<img srchttps://github.com/c9fe/winrader/raw/master/.readme-assets/winraderproof.JPG alt="winrader running Windows 95 on Ubuntu" width=768>

## license

Copyright (c) 2020, Dosyago and/or its affiliates. All rights reserved.

This is a release of winrader, demonstrating Windows 95 in a cross-platform executable built using Grader, an cross-platform app builder.

License information can be found in the LICENSE file.

Nothing in the license makes any claim over any part or whole of the Windows 95 images used in releases.

This source-code, excluding any Windows 95 images, is dual-licensed. For information about commercial licensing, see [Dosyago Commercial License for OEMs, ISVs and VARs](https://github.com/dosyago/dual-licensing).

This project is provided for educational purposes only. I do not own any of the Windows related trademarks used herein, and this project is not affiliated with and has not been approved by Microsoft, and has no official connection to or endorsement from Microsoft, or any other trademark holder.

## key stats

- development time: < 2 hours
- lines of code: < 100

## to run this from source

1. you need to glone the repo
2. `npm install`
3. you need a `windows95.img` file. I got mine from [felixrieseberg's releases](https://github.com/felixrieseberg/windows95/releases)
4. `npm test`

## to build the binary

Assuming you've already done the above steps to run from source, then do:

```console
$ ./scripts/compile.sh
```

## nerd warning

**WARNING:** This project uses Google Chrome to display the UI. Running this will download and install Google Chrome if you don't already have it installed. If you are allergic to Google Chrome, please avoid running or ingesting this binary.

## security warning

**WARNING:** Normally, for security, GraderJS will inflate the app contents from the virtual filesystem inside the binary every time you run yer app. But because this project is so massive (it uses a OS image), inflating takes a long time, so I add a "hack" in the `launcher.js` code to only inflate it the first time, to save you time for your convenience. This makes your on-disk code vulnerable to malicious editing. For example someone could overwrite your index.html file because we don't refresh it every time.

## related projects

- [Grader.JS](https://github.com/c9fe/graderjs) - the cross-platform app-builder I used to make this
- [felixrieseberg/windows95](https://github.com/felixrieseberg/windows95) - the original and best windows-in-a-box
- [copy/images](https://github.com/copy/images) - not including the windows 95 image ([which was obtained from felixrieseberg's releases](https://github.com/felixrieseberg/windows95/releases)), a variety of images that in future will also be run in Grader.JS
- [copy/v86](https://github.com/copy/v86/) - x86 virtualization in JS
- [win95.ajf.me](https://win95.ajf.me/) - Windows 95 running in DOSBOX converted to JS via emscripten
- [Archive.org MSDOS games library](https://archive.org/details/softwarelibrary_msdos_games?&sort=-downloads&page=2) - classic DOS games playable in yer browser












