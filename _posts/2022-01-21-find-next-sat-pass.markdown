---
layout: single
title:  "Find Next Sat Pass"
date:   2022-01-21 14:00:00 +1100
categories: jekyll update
---

Okay, babies first piece of code is to:

* Find a library to deal with orbital mechanics (so I don't have to)
* Find the next useful pass of the Sentinel-2A satellite (ignoring 2B for now)
* Find the azimuth/elevation of the satellite when my ground station is under it's nadir.

I'm making the assumption that the camera is indeed pointing directly down. I actually haven't been able to find anything in the docs that explicitly states this, but given the eternal challenge of remote imaging seems to be improving the resolution it makes sense to me that it ***should*** be pointing down. Love a good should.

## Debugging

* I've found the pyorbital function get_next_passes to be quite unreliable, with it returning a different number of upcoming passes every time I run it.

Apparently [thorsteinssonh](https://python.hotexamples.com/examples/pyorbital.orbital/Orbital/-/python-orbital-class-examples.html#0xa7b6b686779f5f321573714f47731cb8cbe2273eb24d4cac932577d2f097d93c-12,,109,) has the same problem in his project, and wrote a custom function which seems to work quite well. 

I guess I could either fix the repo, or just fucking move on.