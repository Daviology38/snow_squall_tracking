# snow_squall_tracking
This program takes the files from the kbox_vids or kenx_vids directory (specified by user) and enables the user to plot them one by one. From here you can track the progression of the cells within the radar video files.

The video will continuously loop through the animation, stopping when the user presses the "s" key. The user can then draw a rectangle by clicking and dragging around a cell. Once the desired cell is picked, the "enter" key or "space bar" is pressed and the user will be prompted if they want to pick another cell or not (by entering "y" or "n" and pressing enter). This program can handle a max of 10 tracking cells.

Once "n" is entered by the user, the video loop continues with a green box highlighting each tracked cell. Once either the end frame of the video is reached or if the x and y positions of a green box stop changing (cell has dissipated), then the tracking ends.

The values of the x and y coordinate of the top left position of the box are saved for each frame of movement. After sorting these, an angle of motion is found between the x axis and the line created by the movement of the cell. This angle is then mapped to a compass bearing grid based on the quadrant it was located in on our original x/y cartesian grid. NOTE: In these cases, y is positive going down, so you need to reverse the y coordinate (already done in program).
