##  Pi Setup - sh: can&#39;t access tty

At startup:

    sh: can't acces tty

Add `disablesafemode` to /recovery.cmdline:

    runinstaller quiet vt.cur_default=1 elevator=deadline disablesafemode

note:
- Attach peripherals, insert SD card, then attach power.
- First Pro Tip that is hard to find a solution for.
