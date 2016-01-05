Connect it.

Find the id and name of the mouse in the output of:

    xinput list


Run:

    xinput --test THE_ID_OF_THE_MOUSE


Try each button, and write down the button number for later use. On my last test with my rat 7, they were:

* 1 = left click
* 2 = wheel click 
* 3 = right click
* 4 = wheel up
* 5 = wheel down
* 6 = ??
* 7 = ??
* 8 = backward thumb
* 9 = foward thumb
* 10 = thumb wheel right 
* 11 = thumb wheel left
* 12 = thumb dpi
* 13, 14, 15 = mode changes
* 16 = dpi up
* 17 = dpi down

On this line, you must update the mouse name with the name you got from ``xinput list``:

    MatchProduct "Mad Catz Mad Catz R.A.T.7 Mouse"


On this line, you must put the biggest button number you got:

    Option "Buttons" "17"


On this line, you must put 0s on the mode buttons (which break X):

    Option "ButtonMapping" "1 2 3 4 5 6 7 8 9 10 11 12 0 0 0 16 17"


On this line, you must list the mode buttons:

    Option "AutoReleaseButtons" "13 14 15"


On this line, you must put the 4 wheel buttons:

    Option "ZAxisMapping" "4 5 11 10"


Finally, copy the 10-rat.conf file to /etc/X11/xorg.conf.d/ (create the folder if needed).
