## Regular conductors

To undebrstand why semiconductors are special you must first understand why regular conductors conduct electricity. A simplified explanation revolves around the fact that electrons in elements can be found in 2 different "layers" - the valence layer and the conduction layer. In order for an electron to jump away from an atom and flow to a different one it must be in the conduction layer.

##### A conductor usually looks like this:

`.img--50, center`![[Conductor.excalidraw|100%]]

As clearly visible the layers overlap energetically meaning that the conductor atoms posses some electrons in the valence layer that can already start flowing if pressure is applied.

##### Most insulating materials then look like this:

`.img--50, center`![[Insulator.excalidraw|100%]]

In insulators any electron that finds itself in the valence requires at minimum, the energy that separates the conduction layer and the valence layer, to start flowing. 

#### Now this is where semiconductors come in

A semiconductor behaves like a sort of insulator with the difference being that their gap area is usually quite small. This allows for some electron flow with relatively low pressure.

Now a superconductor becomes even more interesting when you mix it with other substances. This is called 'doping' the semiconductor. There are 2 types of doped semiconductors:
1. Semiconductors mixed with atoms that have 5 electrons on the outer shell __(Type N)__
2. Semiconductors mixed with atoms that have 3 electrons on the outer shell __(Type P)__

### Type N semiconductors

`.img--50, center`![[NSemiconductor.excalidraw|100%]]

As visible on the drawing this semiconductor (made from silicon) has been mixed with arsenic which has a large amount of electrons in the outer shell. 

This means that the electrons from arsenic have a higher energy level, but as visible on the diagram their energy does not surpass the conduction energy level of the semiconductor. This arsenic atom basically acts as a donor of electrons making this semiconductor easily liberate electrons with a small energy input.

### Type P semiconductors

`.img--50, center`![[PSemiconductor.excalidraw|100%]]

Type P semiconductors are the reverse of type N semiconductors. Instead of supplying electrons, the substances they are mixed with can absorb themm introducing artificial gaps into the charge distribution. The electrons from the covalent bonds of the semiconductor only need a small amount of energy to occupy these gaps.

### The PN union

#todo add diagram

When the 2 types of semiconductors are joined together, a depletion zone is formed at the join area. This depletion zone is formed because electrons from the N semiconductor flow to the P semiconductor and both semiconductors are saturated. 

The depletion zone acts as resistance for electrons attempting to pass through.

Now the most interesting property of this union is that when current is
applied in the P-N direction (Inverse polarization) the depletion zone grows, increasing the resistance. The reverse happens when current is applied in the N-P direction (the depletion zone shrinks decreasing the resistance). 

This is because when current is applied in reverse, electrons are drawn away from the N semiconductor and are pushed into the P semiconductor which saturates them.  When the current is applied correctly the reverse happens desaturating the semiconductors.

#todo add diagram

### The diode

What we created by joining the P and N semiconductors is called a diode. The __*P side*__ of the diode is called an __*anode*__ and the __*N side*__ of the diode is called a __*catode*__.

A perfect diode acts as a step from infinite resistance to 0 resistance when voltage is applied forward. Here's a graph of how that would act (IP - Inverse polarization, PD - Direct polarization):


`.img--75, center`![[PerfectDiode.excalidraw|100%]]

A real worl diode ofcourse doesn't act like that and has a different, yet quite similar, graph pattern:


`.img--50, center`![[RealDiode.excalidraw|100%]]

The most important part to note about diodes is that they are capable of varying their resistance based on the current/voltage passing through.

### The transistor

A transistor is a circuit element that has either a NPN form or a PNP form. It has 3 connection points: 
1. Collector (The entrance for the main electricity flow)
2. Emmiter (The exit for the main electricity flow)
3. Base (The controller that regulates the transistor's resistance)
As the name suggests the NPN transistor is composed of 3 N-P-N semiconductors joined together. 
When current is applied to the central semiconductor (the base pin) the resistance between the emmitter and the collector falls until saturation. The current graph (graphed against voltage in the base pin) can be seen here:

`.img--75, center`![[Transistor.excalidraw|100%]]


The current goes from being almost 0 at the 'Cut' section to linearly growing at the 'Conduction' section to beign flat in the 'Saturation' section up until the destruction of the transistor.

#todo Talk about the FET transistor