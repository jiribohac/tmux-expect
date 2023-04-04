# tmux-expect
select a tmux pane and automatically respond to input using expect

# Use cases:

## Entering BIOS over serial console

Imagine you're connected to a serial console of a server that takes 5 minutes to boot. You want to enter the
BIOS setup by pressing Delete when prompted. But you don't want to spend 5 minutes by staring at the screen.

1. run the serial console (ipmitool, screen, or such) inside tmux
2. run tmux-expect
3. select the tmux pane
4. enter "Press DEL" when asked for the prompt
5. Press DELETE when asked for the response

tmux-expect will monitor the serial console and press DELETE when a "Press DEL to enter BIOS SETUP" appears

## Selecting another kernel when booting grub over serial console

Again, booting a machine with serial console. You want to boot other than the default GRUB entry and the timeout is short!

1. see above
2. see above
3. see above
4. enter "GRUB" for the promp
5. press DOWN for the response

grub will be interrupted and you can select an entry manually.

## x3270

Have you ever worked withan s390 console using x3270 and got IRRITATED by having to clear the screen
manually each time it fills up? Say no "MORE..."!

1. run c3270 instead of x3270, inside tmux
2. run tmux-expect
3. select the c3270 pane
4. type "MORE..."
5. type Ctrl+A C

Voilà, you just brought 3270 50 years forward and made it usable!

