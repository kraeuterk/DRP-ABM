# WHAT IS IT?  

This is an agent-based model of a generalized tumor mircoenvironment (TME) in 2D. 

# HOW IT WORKS

Rock-Paper-Scissors is a hand game in which players simulatenously make one hand motion (rock, paper, or scissors) and the winner is determined by a set of rules: (i) rock beats scissors, (ii) paper beats rock, and (iii) scissors beats paper.  

In this ABM, agents move randomly in 2D space and "play" the game locally. Each agent is defined to a team -- rock, paper, or scissors. In the current model verison, the agents are split evenly among the 3 teams and they move randomly in the environment. If two agents come within some set radius of each other, they "compete" and the losing agent joins the team of the winning agent (e.g., if a "rock" and a "paper" "bump into" each other, then the "rock" agent is transformed into a "paper"). The game comtinues until all agents are on the same team. 

# HOW TO USE IT

To experiment:   
(1) Choose the number of "cancer cells" in the model via the slider on the interface.    
(2) Click the "setup" button to initialize the TME.    
(3) Click the "go" button to run a simulation.      

# THINGS TO NOTICE

During a simulation, view the environment window and plots to monitor the status of the cell populations. 

# THINGS TO TRY

Adjust the sliders and see how the number of "cancer cells" and/or immune efficacy impacts system dynamics. Can you optimize the immune response to converge to a cancer free environment in the least amount of ticks? 

# EXTENDING THE MODEL

Below are some ideas for how this ABM could be extended/adjusted:  

* The model could be adjusted based on published experimental data to improve biological accuracy (e.g., specific cancer type, accurate cell ratios)
  
* The model could be extended to 3-D (e.g., topologically accurate representation of a tumor in the body)

* Additional buttons/sliders could be added to increase flexibility in the setup (e.g., enable the user to control the initial distribution of cells, enable the user to control the interaction radius)

* Features such as adjustable immune response and cell targeting could be included to represent treatments such as immunotherapy and radiation, respectively.

* The number of ticks to convergence to a cancer-free mircoenvironment could be output via a monitor or the command line. 

* BehaviorSpace could be used to run replicate simulations to output relevant data for analyzing the distribution of times to convergence or the relationship between number of each cell type (and/or size of environment) and time to convergence.

There is much that could be done to extend this model and improve its biological accuracy and scientific relevance. Published lierature and experiemental data must guide future model modifications.

# NETLOGO FEATURES

The interactive interface allows users to adjust the number of each cell type in the environment and the behavioral probabilities. 

# RELATED MODELS

Our Rock-Paper-Scissors model inspired the initial design (e.g., 3 cell types in competition) of this ABM. 

# CREDITS AND REFERENCES   

The NetLogo Dictionary and Google's AI assistant were helpful in translating ideas to NetLogo syntax. 
