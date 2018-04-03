# Windows for developers

> Small notes from an ex-Mac user about developing on Windows.

Hello everyone. In [January '18 I switched to a Surface Book 2 (13 inch)](https://twitter.com/PipoPeperoni/status/953267367899025409) after using a MacBook Pro (13 inch) for eight years or so. I only had "soft reasons" to do that:

- the Surface line allways interested me - especially trying the Surface pen (I loved taking notes and drawing as a student)
- recent changes on the MacBook line seemed to be more problematic for me (e.g. touch bar)
- I always used a 13 inch laptop and the MacBooks have no dedicated graphics card in this size
- the MicroSoft culture in the last years seemed to be more attractive to me (more focus on developers, designers and open source)
- I only heard good things about the WSL
- I like to try new things!

The macOS High Sierra update actually bricked my MacBook Pro at the end of 2017, so I decided to switch to Windows 10 completely - as an "experiment". Maybe an expensive experiment, but I was supported by [Mercateo](https://github.com/Mercateo) to get some more diversity in our setup. (I was the first Windows developer after years with just Mac and Linux systems.) I used my system for three months now and here is a short review.

> **tl;dr**: Yes, you can use a Windows system as your every day system for development. But the switch will not be easy and I can't recommend it to everyone. It really depends on your requirements.

## Windows OS

The Windows OS seems to came a long way since the last time I checked it. I think I haven't found a new feature I dislike - I only miss some features. Here is a break down:

- I miss tabs in the Explorer. But there is a similar feature called ["Sets"](https://arstechnica.com/gadgets/2017/11/tabs-come-to-every-window-in-windows-10-sets/) which comes soon.
- I want to calibrate my gestures. Scrolling with two fingers on Mac OS always worked flawlessly, but there is a slight chance that my scrolling is interpreted as pinch-to-zoom on Windows (maybe a 10% chance).
- I _really_ miss good system-wide _and_ customizable hotkeys like "Close other tabs".
- I miss some system-wide text correction/text expanding feature.

## WSL

Installing and using the WSL was _really_ easy and 99% of our Node scripts worked without changing them. _That_ is really impressive. I had no problems using Node or Java or something else. (I used Docker on the Windows side however.) But there are downsides.

- **The WSL is slow.** Yarn/npm installations take forever.
- **Be prepared to use Windows Insiders.** (Because of fixed issues like [this one](https://github.com/Microsoft/WSL/issues/2898).) It would be _so_ good, if updates to the WSL wouldn't be tied to OS updates.
- **Be prepared to use a Linux VM.** (Because of not yet fixed issues like [this one](https://github.com/Microsoft/WSL/issues/2780).) I always hoped I could just use WSL and be productive from day 1, but sadly this is _not yet_ the case. Interestingly Windows offers a native way to install a VM without additional software. In some weeks it should be possible to get a [full featured Ubuntu VM in _three clicks_](https://blogs.technet.microsoft.com/virtualization/2018/02/28/sneak-peek-taking-a-spin-with-enhanced-linux-vms/). Currently it needs some more clicks, but works. Performance could be better and I would like to resize the window for the VM.
- `nvm` has a known problem with [slow startup](https://github.com/creationix/nvm/issues/1277) times, but it was unbearable on the WSL. I use [`n`](https://github.com/mklement0/n-install) now.
- It would be nice if Windows apps (like VS Code and SourceTree) could use WSL apps (like Git) without problems, so I don't need to maintain two Git installations. (At least VS Code has an open issue to try to support the WSL Git as well.)

## Apps

I don't need a lot of apps, but sadly I still have some troubles with them.

- VS Code could perform a little bit better. There is only a [partially fix for that for now](https://github.com/Microsoft/vscode/issues/13612).
- Hyper.js is _really_ slow and buggy for me. So much that it is not useable for me. The VS Code terminal however works _really_ great. There is an open issue to make it a [standalone application](https://github.com/Microsoft/vscode/issues/34442). That would be so nice.
- I always used Monosnap for screenshots and short screen recordings. It has a Windows version as well, but this one is _very_ slow on high resolution screens. (But the developers are quite nice.)

Other apps worked really well without problems (Enpass, all browsers, Telegram, WhatsApp...).

## Surface Book 2

**A Surface product without a pen is a half-hearted attempt** in my opinion. Sadly the pen isn't included in the Surface Book 2 and it was sold out, when we bought the Book. Because of some unfortunate events I still don't have a pen. If I'd be responsible for the Surface hardware I'd make sure to include a pen to show my product as a complete solution.

- Nice display, keyboard and touchpad.
- Nearly silent during the whole day.
- Battery life (or stand-by behaviour?) could be better. IMHO the MacBook was more responsive after waking up and had lost less energy.
- In some rare moments I hear coil whine. (After a full reboot...?)
- HDMI would be nice.
- Opening the book with 180° would be nice.

## Windows culture

The _new_ Windows culture is a main selling point for the Windows platform.

- You can get in touch with Windows developers _really_ easily. I had great success contacting and getting help from Windows developers via Twitter or GitHub issues. (E.g. you can report WSL bugs on [a dedicated GitHub repository](https://github.com/Microsoft/WSL).) The developers and project managers were responsive, helpful _and_ friendly.
- Windows even has a dedicated app to get in touch with developers called Feedback-Hub. I like the idea, but the app could have a better UX and I got mroe answers via Twitter or GitHub. The Feedback-Hub is more a one-way communication channel than a dialogue. (How nice would it be to have an app called "Dialogue" as the Feedback-Hub.)
