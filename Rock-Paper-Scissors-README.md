# WHAT IS IT?  

This is an agent-based model of competition, based on the game Rock-Paper-Scissors. 

# HOW IT WORKS

Rock-Paper-Scissors is a hand game in which players simulatenously make one hand motion (rock, paper, or scissors) and the winner is determined by a set of rules: (i) rock beats scissors, (ii) paper beats rock, and (iii) scissors beats paper.  

In this ABM, agents move randomly in 2D space and "play" the game locally. Each agent is defined to a team -- rock, paper, or scissors. In the current model verison, the agents are split evenly among the 3 teams and they move randomly in the environment. If two agents come within some set radius of each other, they "compete" and the losing agent joins the team of the winning agent (e.g., if a "rock" and a "paper" "bump into" each other, then the "rock" agent is transformed into a "paper"). The game comtinues until all agents are on the same team. 

# HOW TO USE IT

To play:   
(1) Choose the number of "players" (i.e., agents) in the model via the slider on the interface.  
(2) Click the "setup" button to initialize the game.  
(3) Click the "go" button to run a simulation.    

# THINGS TO NOTICE

During a simulation, view the environment window and plots to monitor the success of each team. When the game finishes, the winning team is announced in the command line.

# THINGS TO TRY

Adjust the slider and see how the number of "players" impacts the rate at which a winner is obtained. Can you optimize the number of "players" to converge to a win in the least amount of ticks? 

# EXTENDING THE MODEL

Below are some ideas for how this ABM could be extended/adjusted:  

* The model could be adjusted so that losing agents are removed from the model instead of switching teams. 

* The number of ticks to convergence could be output via a monitor or the command line. 

* BehaviorSpace could be used to run replicate simulations to output relevant data for analyzing the distribution of wins between each team (rock, paper, and scissors) or the relationship between number of agents (and/or size of environment) and time to convergence. 

* The model could be adjusted to include adaptive decision-making, where agents move to avoid agents that will beat them at the game (e.g., rock moves away from paper) and/or towards agents that they will beat (e.g., rock moves towards scissors). Will including goal-directed movement both away from and towards others agents result in a longer time to convergence, in general? Additionally, agents (or teams) could be made to be "smarter" than other agents using probabilities.

* Additional buttons/sliders could be added to increase flexibility in the setup (e.g., enable the user to control the initial distribution of teams, enable the user to control the interaction radius)

# NETLOGO FEATURES

The interactive interface allows users to adjust the number of players in the game. 

# RELATED MODELS

The Random Walk Example model in NetLogo's Model Library > Code Examples was used to develop this model. 

# CREDITS AND REFERENCES

This ABM was inspired by a post on X which can be seen here: https://x.com/juanbuis/status/1600155605112496129   

The NetLogo Dictionary and Google's AI assistant were helpful in translating ideas to NetLogo syntax. 
