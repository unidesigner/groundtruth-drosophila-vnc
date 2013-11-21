Segmented anisotropic ssTEM dataset of neural tissue
----------------------------------------------------

The ground truth stack 1 contains 20 sections from serial section Transmission Electron Microscopy (ssTEM) of the Drosophila melanogaster third instar larva ventral nerve cord. The cube measures 4.7 x 4.7 x 1 microns approx, with a resolution of 4.6 x 4.6 nm/pixel and section thickness of 45-50 nm.

### The challenge
Use *stack 1* to train pixel classifiers for the purpose of automatic segmentation of neural structures in ssTEM. For instance, use 80% of the sections to train, and 20% of the sections for validation. Apply the classifier to the raw data of *stack 2* (test data) and send us the results, so we're able to compute pixel-wise and other error measures in the subsequent neuron reconstruction pipeline.

### License
This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported License.](http://creativecommons.org/licenses/by-nc-sa/3.0/deed.en_US)
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/3.0/deed.en_US"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-nc-sa/3.0/88x31.png" /></a>

You are free to use this data set for the purpose of generating or testing non-commercial image segmentation software. If any scientific publications derive from the usage of this data set, you must cite:

*Segmented anisotropic ssTEM dataset of neural tissue.* Stephan Gerhard, Jan Funke, Julien Martel, Albert Cardona, Richard Fetter. figshare. Retrieved 16:09, Nov 20, 2013 (GMT) http://dx.doi.org/10.6084/m9.figshare.856713

### Contact

[Stephan Gerhard](mailto:git@unidesign.ch)


### Content

    /stack1/
       /raw: The raw 8-bit greyscale images
       /membranes: Series of binary images of segmented membranes
       /mitochondria: Series of binary images of segmented mitochondria
       /synapses: Series of binary images of segmented synapses
       /labels: Series of merged labels including oriented membranes, membrane junctions,
                mitochondria and synapses. The pixels are labeled as follows:
                0   -> membrane | (0°)
                32  -> membrane / (45°)
                64  -> membrane - (90°)
                96  -> membrane \ (135°)
                128 -> membrane "junction"
                159 -> glia/extracellular
                191 -> mitochondria
                223 -> synapse
                255 -> intracellular
    
    /stack2/
      /raw: The raw 8-bit greyscale images
  
  
