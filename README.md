# Electron-positron Colliders Event Generator for n(iDM) Package

## What is it?

This package is a Mathematica-based code allowing to calculate constraints/sensitivities from electron-positron colliders for (n)iDM models. The method of the calculation is briefly described in [2405.08081](https://arxiv.org/abs/2405.08081). 


## How to launch

Download the full directory and check the example code included.

### Dependencies

To run our package, two tools have to be installed: Wolfram Mathematica (tested on version 13.1) and a C compiler. 


## (Currently) generators implemented

A generic niDM model with a dark photon and/or a dark Higgs mediator is implemented (see the generic niDM approach in [2505.XXXXX](https://arxiv.org/abs/2505.xxxxx)). 

Generating channels available: XXXX XXX XXX . All computed at tree-level and decomposed into steps (first generates the intermediate mediator and then make the mediator decay - ignores the decay width of the mediator, see comments on this topic in [2405.08081](https://arxiv.org/abs/2405.08081) and [1911.03176](https://arxiv.org/abs/1911.03176)

## (Currently) analyses implemented TBC

Also, we have only focused on missing energies so far. However, for other kinds of searches, one can simply compute the total number of events ab inition using the total cross-section and the integrated luminosity of the detector, then, normalize the number of events simulated.

Last, we currently only focused on BaBar and Belle II. Although, considering other e+e- colliders should not be a difficult task.



## Code structure TBC



### Initial mediator generator TBC 

For the moment, only the usual niDM model with a dark photon mediator is implemented (implementing other models would require substantial work). 
  
