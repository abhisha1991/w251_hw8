# w251_hw8 by abhisha@berkeley.edu

This repo is for the homework listed here: https://github.com/MIDS-scaling-up/v2/tree/master/week08/hw

The homework heavily relies on this project tool: https://github.com/tzutalin/labelImg

Questions:

1. In the time allowed, how many images did you annotate?
I annotateed 18 images in total

2. How many instances of the Millennium Falcon did you annotate? How many TIE Fighters?
It was a fairly even split between the number of TIE fighters vs falcons (about 10 each)

3. Based on this experience, how would you handle the annotation of large image data set?
It definitely needs to be automated - perhaps the TIE fighters are a prime example, some features like the distinctive box like structures of TIE planes can be extracted and self annotated. The other aspect of this is that if an exact frame in the video has TIE fighters, its likely that the next few frames are also TIE fighters. Similar explanation for the falcon planes. The triaging of these images can also be done by taking random samples of 5 second clips and assigning them to first level triagers, followed by a second set of triagers who "cross validate" the results reported by the first set.

4. Think about image augmentation? How would augmentations such as flip, rotation, scale, cropping, and translation affect the annotations?
They ideally shouldnt affect these annotations because the classes of the 2 planes are distinctive enough, ie, they dont resemble each other at all. This however, could get problematic if the 2 classes for annotation resembled each other in some way, like say 2 species of a dog. If dog type A was augmented (by cropping, changing color tone etc.), then the image could possibly lead to someone classifying that class as dog type B. The scaling, rotation etc. will however affect the bounding box sizes and shapes and co-ordinates. Those will need to be adjusted according to the augmentation technique applied.

