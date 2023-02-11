# Voron Igor
It's a few good printers.

## What this is
This is my mods for a Voron Legacy.

## What did I mod?
Oh, not much.

### The tensioning idlers and motor mounts
It seems silly to come up with a good implementation and not use it simply because you
want to 'harken back' to the bad ol' days.

I have always disliked designs that tension the belts by moving the motor - and needing to
loosen/tighten 2 or more screws, relying on the motor to slide smoothly against a printed surface,
and/or needing to reach hard-to-reach places to adjust.  So I adapted the tension idlers from
the V2.4, and the motor mounts as well.

### The Y rod mounts
I elected to use some OpenBuilds 2020 extrusion I had, so it probably wasn't perfect, and the slots
were different...but the difference highlighted a design flaw in the original Legacy: The Y rods
get supported by two different datums at each end.

In the back, there is a single part that is located by the 2020 slot, and the rod spacing is fixed, and
as accurate and repeatable as the printer used to print that part.

In the front, the original idlers were a sandwich on the top and bottom of the 2020, and used pockets
to hold the rods.  Any variation the in the 2020 would mean that those rods could be not parallel.

So, I simply made a new Y rod support (x4), into which I also made a small cut so that when turned
the right direction, would allow the full travel of the gantry.

This also means that I could remove the idler tensioners, if need be, without unmounting the gantry.

### The Z axis
I found the original Legazy Z to be very...problematic. 

The rods were spaced far apart, which seemed to make rocking and binding of the whole thing to be too easy.

On top of rocking, it needed manual adjusting of the buildplate with screws. Which were on a wobbly Z axis.
That you had to touch.

This isn't 'harkening back', this is regressing.

So I adapted something like the Jubilee. I didn't know about the Voron Trident at the time, so that's what I was looking off of.

I didn't like the Jubilee's use of springs to hold down the kinematic table, because I could easily see myself
trying to lift a magnetic build plate off and stretching the springs. The springs Jubilee used were also tiny fiddly little bits.
So I came up with a solution to use magnets as effectively as possible, given what I had and could easily model.
The result is something that uses cheap magnets, in something like a Halbach array.

### UnKlicky Tap?
I wanted to try making a Tap upgrade for a printer.

I'd already tried doing the KlickyNG probe, and got it working with the 'Z Calibration' hardware and Klipper module,
in order to hopefully work with any build plate I might want.

I can't say I liked it. Too much to configure, and too much that could go wrong. Naturally, when I saw the Voron Tap,
I realized I wanted something that simple - just touch the damn nozzle to the surface. Simple, right?

Right?

Because the Igor is using 8mm rods, it's not exactly stiff. Mass is a problem (always is on all printers),
and adding more wasn't an option. I also didn't want to have to source more special parts for my Igor.

I also have been wanting to try compliant mechanisms ('flexures') for a while.

Thus is born an X carriage with a linear flexure and a UnKlicky-esque probe.

This is _very_ experimental, and will probably not work well when trying to do higher velocity or acceleration.
The flexure is exactly that - flexible - and while it is contrained in which way it likes to flex, it's difficult to prevent all
other axis of movement when just using plastic and in the size envelope of a Voron carriage.

This is likely something that would need tuning, based on the printer printing it and the filament used.

The reason I'm still including this and going forward with it is that I'm going to lean on Klipper's `input shaping`
to compensate for and measure the wobbliness.

Wish me luck.

## FAQ
### Why isn't this perfect
Partly because I was working on this through a couple upversions of FreeCAD, partly because I was learning more advanced
CAD as I went along, and partly because if there is one negative thing I might accuse the Voron designers of, it's CAD-wanking.

Sure, their designs work well, *and* they have a nice aesthetic, but when working from the STEP models, some things I had to
just take dimesions and start over, because of curved surfaces and such didn't let me easily mod things, or the imported STEP
would develop problems in FreeCAD when I tried to alter them.

### Why not include the full CAD files?
* My CAD files are a mess
* I use the FreeCAD-realthunder snap.
* If you open them in another FreeCAD version, they will likely break, or need a 'recompute now', at which time they will break.
* STEP files are stable

### Why the name 'Igor'?
Some people joking online saying the Legacy should have been named 'Frankenstein'
because they built it out of leftover parts. This is wrong, because Frankenstein was
the name of the *doctor*, not his creation.

I think it would be far more appropriate to adopt the name of a character from
Terry Pratchett's *Discworld* series:
 * the approach to self-improvement
 * the extreme recycling/upcycling
 * the spirit of Reprap in which one Igor can make many more
 * the way it is always just behind me when I need it

Alternative names I considered:
 * That Thing In the Cellar
 * Box O' Parts
 * Reprap Centipede





