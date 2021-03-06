# Lab 4: Faraday&rsquo;s Law, Speed of Light

:::::::::row
::::::col l5
### Faraday&rsquo;s Law Section
::: Materials
- [c] Wire Leads
- [c] Breadboard 
- [c] Magnet Wire
- Option 1:
    - [c] Multimeter
    - [c] Magnets
- Option 2:
    - [c] Power Block
    - [c] Transistor (kit)
    - [c] LED
    - [c] 10 $\Omega$ resistor
    - [c] 2000 $\Omega$ resistor 
- [c] A multimeter
:::
::::::
::::::col l7
### Speed of Light Section
::: Materials
- [c] Microwave
- [c] Pasta, Chocolate, or Melting Cheese 
- [c] Ruler
- [c] Microwave-safe plate
:::
::::::
:::::::::

# Induction and the Electromotive Force

We previously completed two projects focusing on the physics of moving charges -- their behavior in external magnetic fields, and the magnetic fields they themselves generate. We now move on to talk about moving *magnets*.

As you may have learned by now, similarly to the way a moving charge (and, hence, a changing electric field) can generate a magnetic field, a changing magnetic field also induces an electric field. This electric field, like any, has the ability to do *work* [fn] Magnetic fields themselves cannot do work, but when energy is expended (e.g. by pushing a magnet) to cause a change of magnetic field or flux in some region, the resulting electric field can do work.[/fn] . Specifically, we will be interested in how it can do work to generate current in a wire. In this lab, we will investigate the current induced in a loop of wire in the vicinity of a moving magnetic source.


The equation that describes the creation of an electric field by a changing magnetic field is Faraday’s Law. It states that if any open surface experiences a time-varying magnetic *flux*, then a net voltage (or emf) exists around the perimeter of that surface. Here, flux refers to the net magnitude and direction of magnetic field lines penetrating the area enclosed by a loop of wire, or 

::: Equation
$$
\Phi_B= \vec B \cdot \vec A
$$
:::

For a coil with a loop of area $A$, Faraday’s Law predicts that the emf measured around the perimeter is

::: Figure:Equation
$$
V_{coil} =  V_{loop} = - \frac{d \Phi_B}{dt}
$$
:::

Note that the cause of Faraday’s Law is some **time-varying** external magnetic field. 

:::Simulation
<iframe src="https://kapawlak.github.io/PhDemoJS/Apps/Faradays_Law/Faradays_Law.html" width= "100%" height="850px" style="border:none;"></iframe>
:::
In which direction does the current flow in such a situation? The question is addressed by Lenz&rsquo;s law, which states that the magnetic field generated by the current flow (recall the previous lab experiment) will point in the direction *opposite* to the change  in the magnetic flux  from the external field -- the electron motion attempts to generate a $B$ field that "cancels out"; the change in flux, so that the total field in the region is $\vec B =0$.

:::Question
Try to describe what would happen if, instead, the current generated a magnetic field that aligned with the external flux, recalling that a current itself generates a magnetic field. Which laws of physics would might this ultimately break? 
:::

For a coil with $N$ loops in series, the area increases to $NA$, so Faraday’s Law predicts that the emf measured around the perimeter is:

::: Equation
$$
V_{coil} = N V_{loop} = - N\frac{d \Phi_B}{dt}
$$
:::
The effect of these loops is essentially to amplify the emf by a factor of $N$. 

This part of the lab will involve the study of Faraday’s Law and Lenz’s Law acting upon a coil. For Option 1, We will measure Lenz’s Law by moving a magnet suddenly toward or away from the coil, and observing the direction of current. For option 2, we will create a wireless power transmitter by creating a magnetic field that oscillates very quickly, and capturing it with another coil connected to an LED. 

# Faraday&rsquo;s Law Experiments

## Option 1: Lenz&rsquo;s Law


:::Materials
- [c] Wire Leads
- [c] Breadboard 
- [c] Magnet Wire
- [c] Multimeter
- [c] Magnets
:::

::::::Exercise
We will wind the coil around and insert the two ends into the breadboard. The multimeter measurement leads should be inserted so that if the current in the loop moves counterclockwise, it will generate a positive voltage, and vice versa.
:::RFigure coil m
![Example of a wrapped coil with the final loop tucked to keep it tidy](imgs/Lab4/coil.jpg)
:::
Setup:
1. Ensure that you have removed as much enamel as possible from the tips of your Magnet wire.
2. Coil the wire around something round, creating 10-15 loops. 
3. To keep the coil in place, you can wrap the final loop of wire around itself.  
4. Insert the wire ends into the breadboard and connect the multimeter.
5. Move the south pole of the magnet toward the coil very quickly.
6. Note the sign of the voltage. 




:::Question
1. In which direction does the voltage jump? 

2. A positive voltage jump means that current is flowing from the negative lead to the positive lead. Based on the direction of your wire winding, is the current flowing clockwise or counter-clockwise?

3. Now consider the orientation of your magnet, where the south pole should have been facing your loop. Does your observation of the current direction match Lenz&rsquo;s law?
:::
::::::



## Option 2: Wireless Power Transmission


:::Materials
- [c] Wire Leads
- [c] Breadboard 
- [c] Power Block
- [c] Transistor (kit)
- [c] LED
- [c] 10 $\Omega$ resistor
- [c] 1000 $\Omega$ resistor 
:::

:::RFigure osc l
![Example of a wrapped coil with the final loop tucked to keep it tidy](imgs/Lab4/transistoroscillator.png)
:::

In this experiment, we will use a transistor to create a high-frequency oscillating magnetic field. While the behavior of transistors is a topic beyond the scope of this class, we will briefly present a cartoon of their function so you can understand how they are generating an oscillating field.

Transistors have three leads: The collector which "collects" current, the emitter which "emits" current, and the base which determines when current in the collector can flow to the emitter.

In general, transistors can be used in a variety of modes. In this lab, we will use them in the *charge collector* mode, which allows them to operate like a switch. In charge collector mode, current is blocked between the collector and emitter terminals *unless* there is a sufficient voltage between the base and the emitter, often called a *bias* voltage. We can use this by creating a situation that causes voltage on the base terminal to rise and fall very quickly, leading to the collector-emitter current being turned on and off at a high frequency.

:::Figure trans xl
![](imgs/Lab4/trans.png)
:::

When the current from the emitter runs through a coil, the result is that a pulsed magnetic field is created from the very fast switching on and off of the current. If we connect the base terminal to a secondary coil in the same orientation, the result is a magnetic field that oscillates between the maxima.



::::::Exercise

**Construction of the Transmitter Coil:**

:::RFigure tcoil m
![Example of a transmitter coil with the final loop tucked to keep it tidy](imgs/Lab4/Tcoil.jpg)
:::

1. Leaving a 5-10 cm of tail, wrap the wire 15 times around something round.
2. Skip a 10- to 15-cm section of wire, and resume winding the wire in the same direction for another 15 turns. For the final loop, you can wrap the wire around itself to keep the loop stable.
3. Cut the wire to leave another 5-10 cm of tail.
4. The skipped wire from step 2 should create another &ldquo;tail&rdquo; in the center of your coil. Twist this section to secure it, and use scissors to cut it, leaving four wire ends in total as in [Fi](#Fi-tcoil).

####

**Construction of the Receiver Coil:**

:::RFigure coil2 xs
![Example of a wrapped coil with the final loop tucked to keep it tidy](imgs/Lab4/coil.jpg)
:::

1. Coil the wire around something round 15 times, leaving 5-10 cm of tail on each side. 
2. To keep the coil in place, you can wrap the final loop of wire around itself
3. Twist the enamel-free ends of the coil with the leads of an LED.

:::Figure transmitter xl
![After wrapping your first 15 loops, create the central lead in the coil by pulling some extra wire down and twisting before wrapping the last 15 loops.](imgs/Lab4/transmitter.gif)
After wrapping your first 15 loops, create the central lead in the coil by pulling some extra wire down and twisting before wrapping the last 15 loops.
:::


With the two DIY components built, we are now ready to assemble the circuit.



####

**Construction of the Circuit:**



1. Insert your transistor into the board so that each of the three leads is in a different row. 
2. With the flat edge of your transistor facing the right side, connect the bottom lead to ground through a 10-$\Omega$ resistor.
3. The middle lead of the resistor should be connected to one of the **outer** wire ends of your transmitter coil through a-1k $\Omega$ resistor.
4. The remaining **outer** wire end should be connected to the final lead of the transistor.
5. The two center wire ends created by cutting the tail should be plugged into the 3.3-V positive rail. 

:::Figure oscpic l
![The full circuit](imgs/Lab4/coil1.jpg)
The full transmitter circuit
:::

**Testing the Transmission:**
1. Turn on your circuit by pressing the button on your power block. 
2. Bring your receiver coil with the LED attached to the transmitter coil. 

:::Figure light m
![](imgs/Lab4/light.gif)
:::

:::Question
1. Try lighting the LED by holding the receiver coil up to the transmitter coil in both directions. What do you observe? 

2. LEDs have a definite polarity, and light up only if the current is flowing into the positive terminal and out of the negative terminal. Why does this agree with your observations above?

3. The transistor causes a roughly sinusoidal magnetic field oscillation at a frequency of about $\omega \approx 6$ MHz, or a peak-to-peak time of \~ 166 ns. The magnetic field at any point around the transmitter loop can then be written
    $$
    \vec B(\vec r, t) = \vec B_{max}(r) \sin(\omega t)
    $$
If it takes 1.5 V to turn on your LED, estimate the **minimum** value of the maximum magnetic flux through your receiver, $\Phi_{max}$, induced during the oscillation. 

:::
::::::



# Light 
In this section, we will use the wave nature of light to measure the speed of light indirectly. Microwave ovens use microwaves, which -- you guessed it -- are simply ordinary light with a relatively large wavelength (compared to &ldquo;visible&rdquo; light, that is). Most microwaves operate in the 2.45 GHz frequency band, as this band is the most efficient at exciting rotations of water molecules in food.

Since we know the frequency, $\nu = 2.45$ GHz, if we are able to determine the *wavelength*, $\lambda$, of the signal, we can find the speed of light by using the fundamental relationship:

::: Equation
$$
c =  \nu \lambda 
$$
:::


When a microwave is powered, it produces standing waves across the cooking chamber. We can use the resulting pattern to measure the wavelength of the light by placing a medium in the microwave, with the rotating platform removed, and noticing how it heats up unevenly.

The question we have to ask now is: How can we infer the wavelength of the microwaves by using household objects? The answer is quite simple, actually! Since the microwaves deposit *energy* into water molecules, and that energy depends on the amplitude of the wave at that point, we can look for the first signs of "cooking" in the medium -- places where the wave amplitude is highest will heat faster than the surrounding region. Hence, the cooked regions represent the *antinodes* of the microwaves, and raw regions are near *nodes*. 


:::::::::Figure micro
### How Microwaves Work
::::::col l4
![](imgs/Lab4/m1.png)
A microwave oven works by producing microwaves in a device called a magnetron, that leave from a hole adjacent to it (typically on the the right). The microwaves will reflect back and forth from the two sides of the metal oven.
::::::
::::::col l4
![](imgs/Lab4/m2.png)
 The wavelength of the microwaves is tuned to produce a standing wave. This is where you get two waves, one going in each direction, which interact to make some areas where there is a huge vibration and others where there is none.
::::::
::::::col l4
![](imgs/Lab4/m3.png)
This means that there are places where the microwaves are very intense, where the molecules will be vibrated very powerfully, and so heated strongly, and others where the microwaves are weak.  These areas are separated by half a wavelength.
::::::
:::row
Because of the standing waves, modern microwave ovens contain turntables. Otherwise parts of your food would be overcooked and others would still be raw.
:::
:::::::::


Since we are finding distance between the locations of the antinodes, $d$, our measured distances will represent *half* of our wavelength, $\lambda$.



::: Question
Why is the distance between the food medium and the magnetron not important to the determination of $c$ in this experiment?
:::

::: Question
 Write the equation to calculate $c$ in terms of $d$ rather than $\lambda$.
:::



# Measuring the Speed of Light
::: Materials
- [c] Microwave
- [c] Pasta, Chocolate, or Melting Cheese 
- [c] Ruler
- [c] Microwave-safe plate
:::

:::::: Exercise


:::Figure tested xl
![](imgs/Lab4/choc.jpg)

 We tested a number of possible food items to use, and found that using dry pasta that was briefly put under running water to moisten it worked best.
:::
1. Remove the rotating table from your microwave. You may need to place a microwave-safe cup or bowl upside down over the turning gear.
2. Place your medium on the microwave-safe plate.
3. Set the plate in the microwave and turn it on for 10- to 30-second intervals, until you see at least two spots that are melting/cooked
4. Measure the distance between the centers of these two spots.


:::Figure pasta xl
![](imgs/Lab4/pasta.jpg)

Do your best to measure from the center of the cooked region. Be sure to estimate your measurement error, so that you will be able to determine the precision of your result!
:::

:::Question
1. What is the distance between the centers of your cooked regions, $d$? 
2. Estimate the uncertainty in this measurement, e.g. what are the largest and smallest values you'd expect to get if you were to measure this distance multiple times? Write your final answer as $(d \pm \delta d)$ as usual.
3. Calculate the measured value and error of the speed of light using your results. Write your final answer as $(c \pm \delta c)$ as usual Recall that for a product $A =XY$, the formula for error is given by:
$$
\frac{\delta A}{A} =  \sqrt{ \Big(\frac{\delta X}{X}\Big)^2 + \Big(\frac{\delta Y}{Y}\Big)^2}
$$
:::
::::::

:::Question
1. What is the *discrepancy* between your result and the accepted value of $c$?
2. Is the discrepancy within the error bounds, $\delta c$ you calculated?
3. Based on your answer to the above, do you think your measurement agrees with the accepted value of $c$? Why or why not?
4. Are there any sources of systematic error (e.g. irregularities in food moisture, dirty microwave walls, other things that may affect microwave amplitude distribution) that may have affected your results? Give details about these possible sources and how they might affect your result.
:::


::: Question
1. Roughly measure the length of the inside your microwave in cm. 
2. Is it close to a multiple of $d$?
3. Give an argument as to why microwaves typically come in only a few standard sizes. 
4. What do you think the function of the mesh on the viewing screen of your microwave is?
:::

# Write Up

###  **@fa-hand-o-right@  Instructions :**
 #### **1. Answer all questions clearly, showing your work where appropriate.**
 #### **2. Starting on a seperate page:** 
  - Write a short summary (~0.5 page, single spaced) describing Faradays Law, how you tested it, and any important observations.
  - Write a short summary (~0.5 page, single spaced) describing how you can infer the speed of light using the wavelength, how you tested it, and any important observations. 
  - In these summaries, be sure to **summarize your results** and **reasons why you believe your data are precise and accurate**. If you do not think your data are accurate, explain why, and how this could be fixed in a future lab.

 #### **3. Additional Information:**
 - You should attach images of your plots,  data, and setup.  Doing so may allow you to regain partial or full credit even if your experiment fails.


::::::Summary
  :::Hider Lab Submission
  <iframe id="contentframe" width="100%" src="https://gauchospace.ucsb.edu/courses/mod/lti/launch.php?id=6236577&triggerview=0" allow="microphone https://coursekit.google.com; camera https://coursekit.google.com; geolocation https://coursekit.google.com; midi https://coursekit.google.com; encrypted-media https://coursekit.google.com;" allowfullscreen="1" style="height: 500px;"></iframe>
 :::
::::::

# Feedback

Any feedback you choose to give will be used to improve labs this quarter! Feedback is not required on all questions. If you&rsquo;d like just to leave some comments, scroll to the bottom of the form.
::: Hider Open Feedback Form
<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScs2N7niGtq0X3r9blr-wdvoqgGCb1_AR2fqgQCn8YyLawIQg/viewform?embedded=true" width="100%" height="1000" frameborder="0" marginheight="0" marginwidth="0">Loading…</iframe>
:::


