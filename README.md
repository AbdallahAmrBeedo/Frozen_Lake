# Frozen_Lake
In this project, we worked on solving Frozen Lake 8x8 problem which is one of the environments on OpenAI GYM, this is a toolkit supporting teaching agents
various things from walking to playing games. The environment has an 8x8 iced area where the agent should walk inside to find his frisbee, of course walking on ice isn't that easy so the agent should know well which move to take based on his past trials. We manipulated the learning rate of the agent based on the efficiency he gets on his trials till we reach the best percentage of solved episodes from the total episodes.

The environment is from OpenAI gym environments. The game is a toy text game in the form of 8x8 tiles each tile has a state (number) and sequence of actions (right, left, up, down). The story of the game is some friends tossing around a frisbee at the park when one of them made a wild throw that left the frisbee out in the middle of the lake, so you must help him to get the frisbee. The water is mostly frozen, but there are a few holes where the ice has melted. If he steps into one of those holes, he'll fall into the freezing water. At this time, there's an international frisbee shortage, so it's absolutely imperative that you navigate across the lake and retrieve the disc. However, the ice is slippery, so he won't always move in the direction you intend.
The tiles are described as:
-	S: starting tile
-	F: frozen ice safe to walk on
-	H: hole of melted ice, you well fall down
-	G: the goal you intend to reach

The game is over when you step on a hole tile (h) or reach the goal tile (g).
Q-Learning is a basic form of Reinforcement Learning which uses Q-values (also called action values) to iteratively improve the behavior of the learning agent.

New Q(s,a)= (1 - α) Q(s,a) + α [ reward + γ.maxQ(s',a')]

- s: Current State of the agent.
- a: Current Action Picked according to some policy.
- s': Next State where the agent ends up.
- a': Next best action to be picked using current Q-value estimation, i.e. pick the action with the maximum Q-value in the next state.
- R: Current Reward observed from the environment in Response of current action.
- 𝛾: (>0 and <=1) Discounting Factor for Future Rewards. Future rewars are less valuable than current rewards so they must be discounted. Since Q-value is an estimation of expected rewards from a state, discounting rule applies here as well.
- 𝛼: Step length taken to update the estimation of Q (s,a).
