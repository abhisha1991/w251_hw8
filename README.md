# w251_hw8 by abhisha@berkeley.edu

This repo is for the homework listed here: https://github.com/MIDS-scaling-up/v2/tree/master/week08/hw

The homework heavily relies on this project tool: https://github.com/tzutalin/labelImg

### Questions:

#### 1. In the time allowed, how many images did you annotate?

I annotateed 18 images in total

#### 2. How many instances of the Millennium Falcon did you annotate? How many TIE Fighters?

It was a fairly even split between the number of TIE fighters vs falcons (about 10 each)

#### 3. Based on this experience, how would you handle the annotation of large image data set?

It definitely needs to be automated - perhaps the TIE fighters are a prime example, some features like the distinctive box like structures of TIE planes can be extracted and self annotated. The other aspect of this is that if an exact frame in the video has TIE fighters, its likely that the next few frames are also TIE fighters. Similar explanation for the falcon planes. The triaging of these images can also be done by taking random samples of 5 second clips and assigning them to first level triagers, followed by a second set of triagers who "cross validate" the results reported by the first set.

#### 4. Think about image augmentation? How would augmentations such as flip, rotation, scale, cropping, and translation affect the annotations?

They ideally shouldnt affect these annotations because the classes of the 2 planes are distinctive enough, ie, they dont resemble each other at all. This however, could get problematic if the 2 classes for annotation resembled each other in some way, like say 2 species of a dog. If dog type A was augmented (by cropping, changing color tone etc.), then the image could possibly lead to someone classifying that class as dog type B. The scaling, rotation etc. will however affect the bounding box sizes and shapes and co-ordinates. Those will need to be adjusted according to the augmentation technique applied.

#### 5. Describe the following augmentations in your own words

Flip - flips the image along some axis, typically along x or y axis.

Rotation - rotates the image along some angle, typically (+ or -) 90 degrees, 180 degrees etc.

Scale - zooms in or out the image based on some scaling value (1.5x or 2x)

Crop - crops the image to obtain a subset of the image

Translation - translates the object in the image horizontally or vertically to give it an appearance of movement 

Noise - adds some jitter to the pixel to make the image appear "grainy" and "noisy"

#### 6. Image annotations require the coordinates of the objects and their classes; in your option, what is needed for an audio annotation?

For audio, we will perhaps need dimensions such as time clips (start and end time) of the object / person of interest. Other dimensions such as the frequency of the voices in the audio clips can also be captured. If there is a limited number of "well known" subjects in the audio clip (say a conversation between two people, Bob and Alice) - then we can also tag the subjects when annotating the clips.
