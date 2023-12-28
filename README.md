<h3>Java Steam Locomotive Simulator </h3>

<img src=Jsim.PNG align=right width=500>

<i>Backend</i> is a PC based Java applications
that runs a steam locomotive simulation
as if the operator were in the locomotive cab.

<p>
Gauges report pressures of both cylinders, tractive effort (TE)
speed (mph) and air, independent and brake line pressure.
The app has controls for throttle, reverser, air and independent brakes.
There are also inputs for the number of cars, (tonnage) and grade.
Gauges for train and grade resistance may be added.

<p>
The app models a steam engine as well as brakes.
The steam engine models the pressure in each cylinders
to determine the tractive effort of the wheels on the rails.
Similarly, air brakes model brake line pressure and
the affect on brake piston as brake line pressure changes.

<p>
The simulation attempts realistic behavior and
requires proper operation of controls.
The physics model accounts for the forces and mass of the train
to determine acceleration.
Code for the cylinders determine tractive force based on cylinder pressure and
brake code determines braking force based on engine brake cylinder and
brake line pressures

<p>
The forces are

<img src=https://www.coalstonewcastle.com.au/images/physics/brakes_a7_valve.png width=400 align=right>

 <li> tractive effort
 <li> air brakes
 <li> independent brakes
 <li> train resistance (bearing and aerodynamic)
 <li> grade

<applet code="Backend.class"
        archive="Backend.jar"
        width=600 height=400>
</applet>

<!-- ----------------------------------------------------  ----------------- -->
<hr>
<h4> Operation </h4>

Without experience, operating a steam locomotive is non-intuitive,
especially brakes, which there are two of.
There are separate brakes for the engine and the train.

The following two sections
provide a checklist of steps to move a locomotive by itself and
then a train, once the locomotive is coupled to one or more cars.

While the keyboard arrow keys can be used to affect the throttle and reverser,
there are keyboard commands for everything.
<ul>
 <li> q/w change the position of the air brake handle
 <li> a/s change the position of the engine (direct) brake handle
 <li> # t set the throttle as a %
 <li> # r set the reverser as a %
 <li> # c sets the number of cars and tonnage
 <li> # g sets the grade  (- key works after a value is entered)
 <li> y   reset
</ul>

<!-- ----------------------------------------------------  ----------------- -->
<hr>
<h4> Brake Usage </h4>

Moving a loco (no cars) using engine (direct) brakes:
<ul>
 <li> Not sure what holds the brakes in place with a cold locomotive
        (wheel chocks?)
 <li> Engine brakes should be set to (slow) application and
        air brakes set to LAP
 <li> Presumably once the engine starts making steam,
        the engine brakes can be Applied until the engine brake pressure
        is adequate and then set to LAP
 <li> The engine brakes would be set to Release or Running
        when the locomotive is ready to start moving,
        the reverser is pushed forward (or backwards if reversing) and
        the throttle opened.
 <li> Throttle might be closed once the locomotive is moving and
        the locomotive allowed to coast
 <li> Brakes would be Applied, bringing the locomotive to stop and
        the engine brakes set to LAP
</ul>

Moving a train:
<ul>
 <li> The locomotive is coupled to a train as it is brought to a stop
        by applying the engine brakes and then setting then to LAP
 <li> After brakes hoses are attached, air brakes are set to RELEASE
 <li> Once brake line pressure reaches max (90 PSI),
        engine (Direct) brakes are set to LAP (?)
 <li> Air brakes would be Applied/released as necessary as the train travels
 <li> Air brakes are applied to come to a stop at the destination
 <li> Engine brakes are Applied and air brakes set to LAP
        prior to disconnecting air hose.
 <li> The engine brake are be set to Release or Running
        when the locomotive is ready to start moving,
        the reverser is pushed forward (or backwards if reversing) and
        the throttle opened.
</ul>

<!-- ----------------------------------------------------  ----------------- -->
<hr>
<h4> Throttle & Reverser Usage </h4>

<ul>
 <li> With the pistons in some unknown position,
        the reverser must be set all the way forward
        (or all the way backwards if reversing)
        to allow steam into both cylinders.
 <li> The throttle is opened to allow steam into the cylinders
 <li> The throttle is opened just a crack if pulling a train to avoid slip.
 <li> Quickly close the throttle when slip occurs.
 <li> The reverser should be pulled back to the half forward/reverse position
        once the train picks up speed (mph ?)
        to used steam a bit more efficiently
        by allowing it into one cylinder or the other and
        taking advantage of steam expansion once the valve is closed
 <li> The throttle can be partially closed once the desired speed is reached
        to maintain speed
 <li> While maintaining speed, the reverser can be reduced (?)
        to reduce the consumption of steam and
        take advantage of Expansion.
</ul>

<!-- ----------------------------------------------------  ----------------- -->
<hr>
<h4> Running the App </h4>

The app can be invoked from a DOS <i>cmd</i> window
with the
<a href=https://docs.oracle.com/goldengate/1212/gg-winux/GDRAD/java.htm#BGBFJHAB>
Java  RunTime Environment</a> installed.
<pre>
java -jar Backend.jar
</pre>

The app source code can be compiled and invoked
using the following commands.
The compiler requires the
<a href=https://www.oracle.com/java/technologies/downloads>
Java Development Kit (JDK)</a>
<pre>
javac Backend.java
java Backend
</pre>

Use Windows explorer to navigate to the directory
where the Backend app is installed,
press <i>Alt-D</i> and enter <i>cmd</i>
to open a command prompt window
and enter the above commands.
