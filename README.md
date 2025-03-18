# Electron-positron Colliders Event Generator for n(iDM) - a Mathematica package

## What is it?

This package is a Mathematica-based code allowing to calculate constraints/sensitivities from electron-positron colliders for (n)iDM models. The method of the calculation is briefly described in [2405.08081](https://arxiv.org/abs/2405.08081). 


## How to launch

Download the full directory and check the example code included.

### Dependencies

To run our package, two tools have to be installed: Wolfram Mathematica (tested on version 13.1) and a C compiler. 


## (Currently) generators implemented TBC

A generic niDM model with a dark photon and/or a dark Higgs mediator is implemented (see the generic niDM approach in [2505.XXXXX](https://arxiv.org/abs/2505.xxxxx)). 

Generating channels available: e+e- -> A' gamma , e+e- -> A' h' , e+e- -> Psi -> BB -> K h' , e+e- -> Psi -> BB -> K h'h' . All computed at tree-level.

We decompose the whole events into steps (first generates the intermediate mediator and then make the mediator decay -- it ignores the decay width of the mediator, see comments on this topic in [2405.08081](https://arxiv.org/abs/2405.08081) and [1911.03176](https://arxiv.org/abs/1911.03176).

## (Currently) analyses implemented TBC

Missing energy analysis (rescaling)
Displaced vertices searches (both ono and di-decays)

Last, we currently only focused on BaBar and Belle II. Although, considering other e+e- colliders should not be a difficult task.



## Code structure TBC



### Initial mediator generator TBC 

For processes involving direct production from the initial e+e- collision (e+e- -> A' gamma , e+e- -> A' h'), we use the averaged amplitude squared of the processes to sample the final state SM particles and mediators. 
For processeses coming from Psi decays, we simply follow the particles decay chain and boost the final states SM particles and mediators by the initial Psi velocity (in this way, we can just scale the number of events by the total number of B mesons produced). 

The final data from this first generator is an output of the form:

{EVENT1,EVENT2,...} where each event is of the type: EVENT = {{particle_id,E,p1,p2,p3},{particle_id,E,p1,p2,p3},...} where the particle_id is a number identifying each particle and P={E,p1,p2,p3} the particle 4-momentum.

We follow the particle identification number (particle_id) conventions of https://pdg.lbl.gov/2007/reviews/montecarlorpp.pdf . We use the id -22 for A', -25 for h' and 51 for the ground state \chi while -51 for the excited state \chi* .

For each production channel we have the following events form: 

| Channel  | Event data |
| ------------- | ------------- |
| e+e- -> A' gamma  | EVENT = {{particle_id,E,p1,p2,p3},{particle_id,E,p1,p2,p3},...} |
| Content Cell  | Content Cell  |

  
