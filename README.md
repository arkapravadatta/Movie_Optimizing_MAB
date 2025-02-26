Title: OptimizingMovie Recommendations UsingMulti-Armed Bandits

Background: In the world of online streaming, user satisfaction and engagement are critical
metrics for the success of a movie recommendation system. A well-designed
recommendation algorithm can significantly enhance the user experience by suggesting
movies that align with their preferences, leading to higher platform retention and usage.
Recommendation systems face the challenge of balancing exploration (discovering new
movies) with exploitation (recommending known favourites) to maximize user satisfaction
over time.

Scenario: Imagine a leading online movie streaming platform, TrendMovie Inc., that aims to
become the go-to destination for personalized movie recommendations. The platform
features a vast collection of movies catering to diverse audiences. TrendMovie Inc. wants to
optimize its recommendation strategy to deliver maximum user satisfaction while
maintaining a high level of engagement. Each movie recommendation is treated as an
interaction with the user, and their feedback is used to refine the recommendation strategy
dynamically.

Objective: Your objective is to design and implement a recommendation system using
Multi-Armed Bandit (MAB) algorithms to maximize cumulative user satisfaction. The
system should dynamically allocate recommendations by learning user preferences in
real-time, striking the right balance between exploration and exploitation.

Dataset Description: The dataset contains user ratings for a variety of movies. Key columns
in the dataset include:

● User ID: A unique identifier for each user.
● Movie ID: A unique identifier for each.
● Rating: A score provided by the user for a movie (on a scale of 1 to 5).
● Timestamp: The time when the rating was given (optional for this assignment).

Link for accessing the dataset:
https://drive.google.com/file/d/1gfobhqlVCw8Oo52JCiYpEBGhG5k7cWBr/view?usp=driv
e_link

Environment Details:
Arm:
Each movie represents an "arm" in the MAB framework. The probability of a movie being
liked by a user is initially unknown and will be estimated based on user feedback during
the interactions.

For example:
● Arm1: Movie A
● Arm2: Movie B
● Arm3: Movie C …. and so on, for all movies in the dataset.

Reward Function:
The reward function is defined based on user ratings:
● Reward = 1: The user rates the movie high star (e.g., 4 or 5 stars).
● Reward = 0: The user rates the movie low star (e.g., 1, 2, or 3 stars).


Assumptions: Run simulations for 1000 iterations for each policy


Requirements and Deliverables:
1. Load the movie ratings dataset and preprocess it as needed.
2. Define the environment and compute rewards. 
3. Implement a random policy for movie recommendations and print each iteration.
4. Implement a greedy policy that always recommends the movie with the highest
estimated reward and print each iteration. 
5. Implement the epsilon-greedy policy, where with probability ε you explore
(recommend a random movie) and with probability (1-ε) you exploit (recommend
the best-known movie). Try with ε =0.1, 0.2, 0.5, and print each iteration. What
value of ε yields the best performance?
6. Implement the UCB algorithm for movie recommendations and print each iteration.
7. Plot the cumulative rewards for all policies on a single graph to compare their
performance. 
8. Determine which policy performs the best based on cumulative reward. Provide a conclusion summarizing the decision-making process and the
trade-offs between exploration and exploitation.
