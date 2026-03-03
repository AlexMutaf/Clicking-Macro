    Follow the steps below to set up the program.
    Below is also listed what each function does and how to use them (this includes only the user functions)!

    1. How to create the virtual mouse?
       Start by making an integer and giving it the value of the function "open_virtual_mouse()".
       This integer will be what the program uses to communicate with the OS. Below is an example:

       # uint64_t communicator = open_virtual_mouse();

    2. How to set up the virtual mouse?
       Call the function "setup_virtual_mouse(*communicator_var*)" to set up the mouse.
       The function takes the communicator as a parameter. Below is an example:

       # setup_virtual_mouse(communicator);

    3. How to move the mouse?
       Call the function "move_mouse_to(*communicator_var*, *pos_x*, *pos_y*)" to move it to a specific pixel on
       the screen. In the example below I will move the cursor to (100, 100) on the screen:

       # move_mouse_to(communicator, 100, 100);

    4. How to click?
       Use both of the functions below to left and right click.
       Below is an example:

       # left_click(communicator);
       # right_click(communicator);

    5. How to close the virtual mouse?
       Run the function below to close the mouse. Add the communicator as a parameter.

       # close_virtual_mouse(communicator);


    Now that you know how the program works complete the steps below to finish setting it up:

    -----
    * Please change your display resolution to match your monitor in the "mouse_control.cpp" file.
    * EXAMPLE: my resolution is 2560x1440p, so these would be the values:
      const uint64_t MAX_RES_X = 2560 - 1;
      const uint64_t MAX_RES_Y = 1440 - 1;

    -----
    * To get the co-ordinates of a pixel on the screen I recommend using slurp.
    * Install it with either of the commands below:

    > sudo pacman -S slurp      # Arch
    > sudo apt install slurp    # Debian/Ubuntu
    > sudo dnf install slurp    # Fedora

    * Then run the command below and click somewhere on the screen:

    > slurp -p

    -----
    * If the program is too fast/too slow for the UI you are macro-ing, go in the "mouse_control.cpp" file, and change the variable "delay" to
      account for your needs.
    * DEFAULT VALUE:
      const uint64_t delay = 150'000;
