# install_linux_lab


# install opencv 3.2 
# maybe can be installed directly
conda install --channel https://conda.anaconda.org/menpo opencv3


# open multiple terminals
Perhaps this could help: screen

It is not installed by default on Ubuntu, but is provided in the repositories.

It is very useful: ssh to a remote host and type screen to enter a screen session.

Start whatever time consuming task you like, and then press Ctrl+A followed by Ctrl+C to create a new window in the screen session.

This will spawn a new shell where you can do what you want. Create even more windows using the same command.

To switch between two windows quickly, use Ctrl+A followed by Ctrl+A again. As you can see, Ctrl+A puts screen in command mode.

Ctrl+A Ctrl+D will detach from the screen session. You can then disconnect from the host and log in again later and use screen -dr to resume your session.

To go to a specific screen window, type Ctrl+A followed by a number.

Screen will exit when all active windows are closed (or the shells within have exited).
