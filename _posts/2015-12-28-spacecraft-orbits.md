---
layout: post
title: Is there public domain software to calculate the orbit of a spacecraft?
author: Max Parks
categories: planets
thumbnail: http://askanastronomer.org/img/voyager_orb_thumb.jpg
---
<div class="image">
<img src="/img/voyager_orb.jpg">
<div class="caption">Trajectories of the <em>Voyager</em> spacecrafts. Credit: NASA.</div>
</div>

**Is there public domain software that can calculate the trajectory of a spacecraft using a model of the solar system (that includes planets and moons)?**

**Is it feasible for a group of high-school students to develop such a model for a fun (non-school, non-graded) project? The idea is to develop a model that would determine the launch characteristics in order that the spacecraft visits multiple planets/moons.**

<div class="image-40">
<img src="http://ccar.colorado.edu/asen5050/projects/projects_2011/fessenden_proj/index_files/image116.jpg">
<div class="caption">Patched Conic method. <a href="http://ccar.colorado.edu/asen5050/projects/projects_2011/fessenden_proj/">Source</a>.</div>
</div>
I will answer your second question first: Depending on how accurate you wish your trajectory to be, this is a very do-able project! A simple yet accurate simulation of a spacecraft’s trajectory can be constructed using what are called "*Patched Conics*" and the "*Two Body Approximation*". The *Two Body Approximation* assumes that at any given point, one large body (a planet, or the Sun) is dominating the gravitational field that the spacecraft is in. The *Patched Conics* method allows us to stitch together these orbits. Trajectories in the Two Body Approximation take the shape of conics: circles, ellipses, hyperbolas and parabolas. Using this method, we assume that at a certain distance, the gravity of the Earth on the spacecraft is weak, so we switch to the Sun’s reference frame.

With those two terms out of the way, let us discuss the resources you might need for such a project. The first thing to do, I would suggest, would be to pick up a textbook on spacecraft dynamics. The go-to text, as far as I am aware, is “[Fundamentals of Astrodynamics](http://tinyurl.com/pnjbfeq)”, by Bate, Mueller, and White. The book is very approachable, and has gotten many an aerospace engineer through their introductory courses. This book will walk you through how to model the Two Body Approximation, and how to correctly “patch” your conics from one reference frame to another.

<div class="image-40">
<img src="http://www.sv.vt.edu/classes/ESM4714/Student_Proj/class97/mulford/orbit/vectors1.jpg">
<div class="caption">4 of the 6 orbital elements. Pictured are inclination (i), angular momentum (h-bar), longitude of ascending node (Ω), and argument of periapsis (ω) <a href="http://www.sv.vt.edu/classes/ESM4714/Student_Proj/class97/mulford/orbit/orbit.htm">Source</a>.</div>
</div>
Once you have the modelling process down, you will need to create the Solar System as it actually is. To do this, you will need each body’s physical mass, as well as what are called “orbital elements”. These are the variables that you will program in. Every orbiting body will need 6 orbital elements -- with these 6 variables, you can calculate exactly where each planet will be at any given moment. Tables of these elements for the bodies in our Solar System can be found here: [Solar System data](http://ssd.jpl.nasa.gov/?bodies#elem).

Armed with a good textbook and the right tables of elements, you should be able to model the solar system, and introduce your spacecraft into whatever situation you would like! Assuming that you already know how to code, this project should take somewhere between a few weeks and a month or two, depending on how much time you put into it. It would definitely make for a good group project!

The first part of your question was asking if there are any public domain projects like
this already out there. While my investigations did not turn up any public domain trajectory
calculators, there are a number of free models of the planets. I have linked one called “Solar
System Scope” in the section at the bottom, though there are many out there. If projects like
these interest you, and you would like to develop a better intuition for orbits, there are a few
excellent programs I would recommend, despite them not being free. The first piece of
 software I would recommend is [Universe Sandbox](http://universesandbox.com) (or perhaps its more advanced sequel, 2 
Universe Sandbox<sup>2</sup>). Universe Sandbox allows you to simulate any orbital dynamics in space, from galaxies colliding to bowling balls orbiting each other. It uses more advanced models than the Two Body Approximation to better represent the way physics actually works. It also comes packaged with a number of pre-built scenarios, including our solar system, complete with all large bodies and their moons. Universe Sandbox is exactly what it’s name implies: a blank slate to test out different ideas.

The second piece of software I would recommend is a game called [Kerbal Space Program](https://kerbalspaceprogram.com). While it is set in a fictional solar system, it is an excellent tool for familiarizing yourself with the ideas of navigating a solar system. Kerbal Space Program uses Patched Conics and the Two Body Approximation, which may give you some insight into how your own model of the solar system will be constructed. There are ample resources to help you get started in Kerbal, as well as an active Reddit community who are generally willing to help out newcomers, or those seeking educational benefits.

Max Parks
*UT Austin*

### Further Reading ###
* [How to calculate the approximate position of planets](
http://ssd.jpl.nasa.gov/txt/aprx_pos_planets.pdf)
* [Solar System Scope, a simulation of the Solar System](http://www.solarsystemscope.com/)
* [Solar System Dynamics, at NASA JPL](http://ssd.jpl.nasa.gov/)
* [Basics of Space Flight](http://solarsystem.nasa.gov/basics/index.php)
