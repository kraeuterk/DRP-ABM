# WHAT IS IT?  

This is an agent-based model of a generalized tumor microenvironment (TME) in 2D, developed using NetLogo software. 

# HOW IT WORKS

The TME ABM consists of 3 cell ("agent") types (NetLogo "breeds") -- normal (stromal), cancer, and immune cells -- which interact with each other and the spatial environment. We assume normal cells to be fixed in space and cancer and immune cells to be mobile. In particular, cancer cells move randomly in 2D space and immune cells move towards (i.e., target) cancer cells. If two agents come within some set radius of each other, they may interact. Interactions are modeled as uni-directional. The implications of interactions are based on the following assumptions: 

* If an immune cell interacts with a cancer cell, then the "health" of that cancer cell is reduced. When the health has reached a certain threshold (<= 0), the cancer cell is converted to a normal cell. This represents the death of the cancer cell and subsequent replacement by a normal cell. For simplicity we assume this replacement to be instantaneous.    
* If a cancer cell interacts with a normal cell, then the “health” of that normal cell is reduced. When the health has reached a certain threshold (<= 30), the normal cell is converted to a cancer cell.   

All interactions are stochastic. We assume some cell behavior is depended on spatial location (i.e., tumor boundary vs tumor core). An additional feature of immune cells is recruitment (unlimited capacity). That is, based on a stochastic procedure, additional immune cells are added into the environment. Interactions between cell types and immune recruitment lead to changes in the sizes of the cell populations. In this version, simulations run indefinitely. 

For full model details, see the NetLogo code in: Tumor-Microenvironment-ABM.nlogox

# HOW TO USE IT

To experiment:   
(0) Download NetLogo and all relevant files found in this repository.     
(1) Choose the number of "cancer cells" in the model and behavioral probabilities via the sliders on the interface.  
 * behavioral probabilities:
   * pcs = Probability that the Cancer Spreads
   * pik = Probability that the Immune cells attack (Kill) the cancer cells
   * pir = Probabilitiy that the Immune cells Recruit additional immune cells  
(2) Click the "setup" button to initialize the TME.    
(3) Click the "go" button to run a simulation.      

# THINGS TO NOTICE

During a simulation, view the environment window and plots to monitor the status of the cell populations. 

# THINGS TO TRY

Adjust the number of cancer cells via the input widget on the interface and/or the behavioral probabilities via the sliders and see how the number of "cancer cells" and/or immune efficacy impacts system dynamics. For a fixed initial number of cancer cells, can you optimize the immune response to converge to a cancer free environment in the least amount of ticks? 

# EXTENDING THE MODEL

Below are some ideas for how this ABM could be extended/adjusted:  

* The model could be adjusted based on published experimental data to improve biological accuracy (e.g., specific cancer type, accurate cell ratios)
  
* The model could be extended to 3-D (e.g., topologically accurate representation of a tumor in the body)

* Additional buttons/sliders could be added to increase flexibility in the setup (e.g., enable the user to control the initial distribution of cells, enable the user to control the interaction radius)

* Features such as adjustable immune response and cell targeting could be included to represent treatments such as immunotherapy and radiation, respectively.

* Immune recruitment can be set to be in relation to the number of cancer cells in the environment.

*  A stopping criterion can be added to limit simulation time to a fixed experimental time range.    

* The number of ticks to convergence to a cancer-free microenvironment could be output via a monitor or the command line. 

* BehaviorSpace could be used to run replicate simulations to output relevant data for analyzing the distribution of times to convergence or the relationship between number of each cell type (and/or size of environment) and time to convergence.

There is much that could be done to extend this model and improve its biological accuracy and scientific relevance. It is recommended that published literature and experimental data guide future model modifications.    

Note: Due to time constraints, this model version is left including an issue with the elimination of normal cells and immune cells. An update is required (at least) in the subprocedure "check-mortality". 

# NETLOGO FEATURES

The interactive interface allows users to adjust the number of each cell type in the environment and the behavioral probabilities.  

# RELATED MODELS

Our Rock-Paper-Scissors model inspired the initial design (e.g., 3 cell types in competition) of this ABM. 

# CREDITS AND REFERENCES   

The NetLogo Dictionary and Google's AI assistant were helpful in translating ideas to NetLogo syntax. 
