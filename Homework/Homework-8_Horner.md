# Intro to AI-driven Science on Supercomputers

## Week 8 Homework

#### Dan Horner (danhorner@berkeley.edu)

---

# AI Problems of Personal and Professional Interest

## Personal Interest

During graduate school, I studied electron scattering and impact ionization using theoretical and computational methods. In general, the calculations I performed were based on directly solving very large systems of linear equations representing partial differential equations (PEDEs) describing the quantum procesesses. At that time my research involved three areas: 
- computational methods to more efficiently solve the linear equations, using some of the most powerful parallel computing resources at the time, 
- mathematical techniques to more accurately represent the underlying PDEs, and
- approximations to the full, and often very complicated, quantum procesesses so that they could realistically be modeled on finite computing resources.

The main challenge in solving these types of problems, compared with more traditional electronic structure and quantum chemistry simulations is the complex boundary conditions for the solutions. Due to the charged particles involved, the solutions never "go to zero" and require very large mathematical representations. However, these ionization and break-up processess are ubiquitous in many fields, from [plasma physics](https://doi.org/10.1063/5.0050793), [material science](https://link.springer.com/article/10.1140/epjd/s10053-021-00204-6), and even [biology](https://journals.aps.org/pra/abstract/10.1103/PhysRevA.104.012817).

If AI models could be trained to efficiently solve these types of PDEs, it would allow investigations with more dimensions (i.e., more electrons, and atoms) using fewer approximations. In this application, solving PDEs with AI, "training data" has a somewhat different meaning compared to image classification, for example./ The general idea is to devise a loss function that can be minimized through training a artificial neural network to learn the solution:  https://www.pnas.org/doi/full/10.1073/pnas.1718942115, https://onlinelibrary.wiley.com/doi/10.1002/gamm.202100006, https://www.infoq.com/news/2020/12/caltech-ai-pde/ .

Since the problems of interest are physics and chemistry problems, overall success would be measured by how well the results of simulation agree with experimental results, and how new and novel phenomena could be predicted. Although, a parallel metric is how much larger and/or complex processes could be investigated; opening doors to explore completely new areas (generally impractical to investigate experimentally)


## Professional Interest

In my current professional role as a data scientist, I often work with aviation operations and maintenance data. Currently, I forecast asset utilization and estimate various fleet-wide impacts (i.e., mishaps, unplanned maintenance, demand for spare parts, etc.). One interesting application that I have considered is predicting individual component failure, rather than just the aggregate 'failure rate'. Failure of critical aircraft components is generally considered an extremely undesirable occurrence and so relying just on mathematical models instead of direct inspections is unlikely to happen any time soon. A more reasonable approach is to forecast which components are very unlikely to be near failure and could avoid frequent inspections.

Aviation is a data-rich field: modern aircraft have a vast array of sensors continuously collecting a myriad of data points about the aircraft and its operating environment; additionally, weather, flight paths, maintenance records are generally available. One of the challenges, however, is finding sufficient instances of "failure" in the real world (i.e., training data), and accordingly, it might make more sense to consider the future *status* (remaining service life) of a component rather than trying to guess when it will actually fail.

Since the goal is to predict future states, time series analysis would be an appropriate approach. That is, I would develop a model that takes recent observations (sensors, weather, maintenance, etc.) as inputs and predicts the future state (eg., wear and tear, failure likelihood, etc.) of one or more aircraft components. The training data is likewise the collected observations and maintenance inspection reports that describe and quantify the status of each particular component. Additional training data could come from engineering studies in laboratory settings. While generally only varying a small number of parameters at a time, lab studies explore a wider range of conditions than experienced in ordinary operation, and often proceed to component failure. 

Im my view success could be evaluated in a technical sense through continued comparison of predicted status. Additionally in a business sense success would be measured by the number of avoided inspections and avoided component replacements.
