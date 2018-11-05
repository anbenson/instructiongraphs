# Instruction Graphs

This is a 15-400 research project based off the work on instruction graphs
described in https://www.cs.cmu.edu/~mmv/papers/14aamas-MericliEtAl.pdf.

## Dependencies
- python2
- ply (installable via `pip install ply`)
- ros-indigo-turtlebot-simulator (try `sudo apt-get install ros-indigo-turtlebot-simulator` on Ubuntu)

## Running the interpreter
- `git clone https://github.com/anbenson/instructiongraphs`
- `cd instructiongraphs/IGinterpreter`
- `roslaunch turtlebot_stage turtlebot_in_stage.launch &`
- `./main.py getcoffee.ig`

## Notes about Implementation
- The interpreter by default requires a running instance of the turtlebot
  simulator, which is very slow and will cause your computer to become slow to
  respond. You have been warned. Alternatively, you could edit the code pretty
  easily in `dynamics.py` to disable calls to the simulator and merely print
  things instead.
- The `move` command takes two arguments. The first refers to distance, and the
  second to angular rotation.
- In order to detect obstacles, the interpreter relies on user input. Enter 'y',
  'yes', or an empty string to respond with 'yes', else 'no'.

## Demo
A short video demonstrating the 'getcoffee.ig' program in action is included in
the file `ig_turtlebot_demo.mp4`. You might wonder why I filmed it with a phone
camera. This was mostly due to the fact that the turtlebot simulator bogged down
my VM so badly that I was worried what a screencast program might do to it.

## Report
The final report for 15-400 is in the `report` subdirectory. The paper itself is
`paper.tex`, but the report also contains several appendices which are the other
tex files in the directory.
