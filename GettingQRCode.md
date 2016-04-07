# Introduction #

There are currently two ways to get QRDecode:

  * Install it from Installer
  * Compile it yourself.

To get it from installer, add the following repository to your installer (tap on "Sources" in installer, then "Edit", then "Add"):

  * http://www.jerrywong.net/iphone/

To compile it yourself, you will need the following:

  * A working development toolchain (Google around for this if you don't have it)
  * A copy of iphone-qrcode (see the "Source" tab at the top of this page)
  * OpenSSH and BSD Subsystem intalled on your jailbroken iPhone
  * A command line (on OS X, Linux, or Cygwin in Windows)

# Compile Instructions #

Great, you have everything described above. Go to your command line:
  * cd directory\_you\_have\_the\_code
  * make install - the compiler will putter away for a little bit, and then attempt to connect to your iPhone
  * Type in your iPhone's root password when it asks (differs depending on version, Google this, or use Independence or Jailbreaker to change your password)
  * Restart SpringBoard. This is most easily done by rebooting your phone, or installing something from Installer that adds/removes icons from your home screens.

Note:
  * If the process complains about not finding "maxiphone" during the "make install" phase, you will need to edit your hosts file:
  * cd /etc/
  * sudo vim hosts
  * Type in your password when prompted.
  * Add to the bottom of the file "X.X.X.X    maxiphone", where X.X.X.X is your iPhone's IP address. I suggest using your router to give your iPhone the same IP every time, that way you don't have to come back to edit this file.