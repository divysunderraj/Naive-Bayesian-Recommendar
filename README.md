# Naive-Bayesian-Recommendar
This is a recommendation system based on the principles of a Naive Bayes Classifier. 

The simplified idea behind how the algorithm works is that the system chooses the rating for the movie in question with the highest probability. This is based on calculated likelihoods from the ratings that other users gave compared to ratings that we know the current user gave. 

The Naive Bayes Classifier works, in this case, as treating the probability of each rating as a class probability. I.e., $P(C) = P(m_i = rating)$ where $m_i$ is the i-th item in the datset.

The likelihood probabilities are calculated as $\prod\limits_{j=1} P(r_j = k \mid r_i = rating)$ where $r_j$ is the rating of the j-th rated item by the user in question and $k$ is one of the possible ratings. 

We consider the ratings for the different movies to be independent. 

Therefore, we end up with this as the posterior probability calculation for a user $u$:
  ### $P(r_{u,i} = rating) \propto	P(m_i = rating) \prod\limits_{j=1} P(r_j = k \mid r_i = rating)$
  
[Link to research method is based on](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8787761) 

Sources: https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8787761
