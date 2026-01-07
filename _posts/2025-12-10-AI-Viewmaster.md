---
layout: post
title: How to create AI-Generated ViewMaster Reels 
---

I grew up loving View-Masters. They are the perfect toy: simple mechanics, great results. You press a lever, see a 3D photo, and so on, up to seven times. Sometimes the photos form a story. I recently picked up a ViewMaster from a nearby antique shop, along with two discs (one of a memorable hike[^1], and one a surreal depiction of the Three Little Pigs). I wanted to make my own discs immediately.


<img src="/assets/images/viewmaster_icon.png" alt="ViewMaster example" width="10">


Luckily, Michael Ironwood and co. provide this exact service at [Image3D](https://www.image3d.com/retroviewer_stereo/customer/account/login/)[^2]. They offer two options: you can create a reel of 2D images (cool) or you can create a reel of *3D images* (extremely cool). To do the latter, you need a stereogram, commonly collected by stereoscopic cameras. I don’t have a stereoscopic camera but I do have a PhD in machine learning and a sense that today’s generative models might have the capabilities to compensate. 

3D images come in two varieties, both of which mimic how our eyes see different perspectives of the same scene by providing a slightly different image to each eye. The first is an anaglyph where the two perspectives are superimposed and viewed with special glasses; each lens filters for a specific color. 3D movies, for example, use anaglyph images. The second is a stereogram, where each eye[^3] receives a separate image[^4]. Stereograms can be rendered in one of two ways. An image pair where you need to cross your eyes to get the effect is called “crossy” while an image pair where you look straight ahead with a softened gaze is “parallel” or “wall-eyed”. Crossy images are the same as parallel images, albeit in a swapped order (because your eyes are crossed!). View-Masters use parallel images.

To create stereographic left and right pairs of parallel images, a machine learning model must do two things well: depth estimation (to render the scene from different perspectives) and inpainting (to fill in the gaps). Lucky for us, they can, with great success! The relevant task is "monocular depth estimation" and people have found that we're able to infer surprisingly detailed 3D structure from a single image. This blog post has a nice summary of advances in depth estimation[^5] along with  instructive examples; in my experience, I found that models often overestimate depth (for example, in a group photo with multiple rows, the model overestimates distance between rows). There were also a few instances where the model misclassified foreground as background. Inpainting is similarly a machine learning success story, but does sometimes struggle with fine detail (I noticed this most when the model was required to inpaint hair, or chunks of hair would be left behind). Helpfully, ViewMaster images are so small that errors are also difficult to notice. I chose to use [Immersity](https://immersity.ai/) for both depth estimation and inpainting, although their approach to inpainting appears rudimentary and worse than what you'd expect given what a Google Pixel can do. The benefits of Immersity's depth estimation outweighed the costs (both literal and practical).


<img src="/assets/images/viewmaster_pipeline.png" alt="ViewMaster example" width="10">


An unequivocally great use of AI, I think. If you want details on the exact pipeline – I used a combination of Immersity's Immersive Conversion, Keynote, and a Jupyter notebook to cut the images down to the right size –  I’m happy to share. A success!


[^1]: It was Franconia Ridge, a hike I will never do again
[^2]: I did find a guide to making the reels from scratch, but it’s beyond the scope of my time and abilities. 
[^3]: Do animals with more eyes have better depth estimation? Depends on how far their eyes are from each other!
[^4]: Tools to convert stereograms to anaglyphs exist (this is a deterministic transform)
[^5]: https://medium.com/@patriciogv/the-state-of-the-art-of-depth-estimation-from-single-images-9e245d51a315




