# Lab-10---Low-Light-Image-Enhancement-with-a-Pretrained-SID-Model

💡 What Did That Small Change Do?
I bumped the darkFactor setting up a notch, moving it from 0.03 to 0.05.Think of it this way:
the original setting (0.03) made the simulated input image almost pitch black it was like trying to see in a closet with the door closed. The new setting (0.05) still makes the image very dark, but it's like leaving the closet door slightly ajar; there's just a tiny bit more light signal reaching the camera sensor (the network).

The Effect on the Result:

Cleaner Input:
Since the network starts with a slightly brighter image, the random noise (the graininess) isn't as overwhelming. When the image is too dark, the noise takes over everything. By giving it 2% more light, we boost the actual image details relative to the noise.

Better Network Performance: 
The enhancement network doesn't have to work as hard or perform such extreme amplification to bring out the details. This usually results in a much cleaner final image—less digital-looking junk and a more realistic restoration of color and texture.Essentially, we made the simulated low-light problem slightly easier for the deep learning network to solve, and the final picture will look noticeably less noisy and more defined.


![images](https://github.com/Khan548-codes/Lab-10---Low-Light-Image-Enhancement-with-a-Pretrained-SID-Model/blob/main/images/Screenshot%202025-11-20%20105228.png)
