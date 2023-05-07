Download Link: https://assignmentchef.com/product/solved-ence361-project-personal-fitness-monitor-project
<br>
The goal of this project is to program a personal fitness monitor to record a user’s steps and estimate the distance travelled by the user.

<h1>Program Specification</h1>

The developed program will be assessed against the following specifications:

<ol>

 <li>The program should estimate the number of steps taken by a user based on data from the accelerometer on the Orbit board.</li>

 <li>The program should estimate the distance travelled by the user.</li>

 <li><span style="text-decoration: line-through;">The program should allow the user to set step- and distance-goals and should display</span> <span style="text-decoration: line-through;">progress towards these goals.</span></li>

 <li><span style="text-decoration: line-through;">The program should notify the user when a goal is completed.</span></li>

 <li>The RESET button on the TIVA board should restart the program and clear any stored step, distance and goal values.</li>

 <li>In addition to the requirements above, the display, buttons, switches and potentiometer on the TIVA and Orbit boards should function according to the requirements given <span style="text-decoration: line-through;">in Milestone 2</span> <u>below</u>:</li>

</ol>

6.1.<u>At startup the OLED board should display the number of steps counted since the</u> <u>last reset.</u>

6.2.<u>Pushing the LEFT or RIGHT buttons on the Orbit board should toggle the display</u> <u>between total distance travelled since last reset and number of steps counted</u> <u>since last reset.</u>

6.3.<u>The total distance travelled should be calculated from the number of steps</u> <u>multiplied by 0.9 metres.</u>

6.4.<u>When the distance travelled is displayed, pushing the UP button on the TIVA board</u> <u>should toggle the units between kilometres and miles.</u>

6.5.<u>A long press on the DOWN button when the number of steps are displayed should</u> <u>reset steps to zero; similarly a long press on the DOWN button when the distance</u> <u>travelled is displayed should reset the distance travelled to zero.</u>

6.6.<u>Power cycling the board should reset step count and distance travelled to zero.</u>

6.7.<u>Setting SW1 to the UP position should put the fitness monitor in a test mode,</u> <u>where the functionality of the GUI can be verified. In this test mode each push of</u> <u>the UP button should increment the step count by 100 and the distance by 0.09</u> <u>km. Likewise, pushing the DOWN button should decrement the step count by 500</u> <u>and the distance by 0.45 km. Note that the other functions of the UP and DOWN</u> <u>buttons, namely toggling units and resetting counts, should be disabled while SW1</u> <u>is UP. The functionality of the LEFT and RIGHT buttons should not be affected by</u> <u>SW1. Setting SW1 to DOWN should restore the normal functionality of the UP and</u> <u>DOWN buttons.</u>

<ol start="7">

 <li>When the program starts, which may happen after a ‘reset’ operation or after reprogramming, the step and distance values should be zero<span style="text-decoration: line-through;"> and the goals should be</span> <span style="text-decoration: line-through;">returned to default values, namely 1,000 steps and 100 m</span>.</li>

 <li>The program should have a real-time foreground/background kernel operating on a round-robin basis for background tasks. Robust behaviour should be maintained at all times.</li>

</ol>

<h1>Source Code</h1>

Source code from labs and lectures are available on Learn. TivaWare examples are also available from TI. You are welcome to reuse this or other code in your project on <strong>two</strong> conditions:

<ol>

 <li>You explicitly acknowledge the provenance of any code you use, typically by way of comment in your source files.</li>

 <li>You take responsibility for any code you use: this responsibility includes changing the comments to reflect your use of the code.</li>

</ol>

You will lose marks if you do not meet these conditions.

<h1>Serial Port</h1>

During development groups may choose to output debugging information over the serial port. This debugging information <strong>should not</strong> be included in the final version of the code. You are strongly encouraged to use compiler directives to control the transmission of such debug information. For example, a section of code which should not be compiled can be bracketed as follows:

<strong>#ifdef DEBUG_ONLY</strong>

<strong>// Code for debugging here; only compiled if DEBUG_ONLY is TRUE.</strong>

<strong>#endif.</strong>