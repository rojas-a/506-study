# CS 506 Complete Study Guide
*Compiled from all labs — questions reproduced word for word*

---

## LAB 2 — Distance & Similarity

### Multiple Choice

**1.** What is the Euclidean Distance between i and j? *(i = (0,0), j = (1,1))*

- (a) √2 ✓
- (b) 2
- (c) 4
- (d) √2/2

---

**2.** What is the manhattan distance between i and j (using coordinates from above)?

- (a) √2
- (b) 2 ✓
- (c) 4
- (d) √2/2

---

**3.** What is the Jaccard similarity between image 1 and image 2?
*(Image 1: p₁=1, p₂=1, p₃=0, p₄=1 | Image 2: p₁=0, p₂=1, p₃=1, p₄=0)*

- (a) 1/4 ✓
- (b) 1/2
- (c) 1
- (d) 0

---

**4.** What is the cosine similarity between A and B? *(A = (1,1), B = (0,1); Hint: cos(θ) = A·B / |A||B|)*

- (a) √2/2 ✓
- (b) π/4
- (c) 1
- (d) −1

---

**5.** What is the jaccard similarity between user 1 and user 0?
*(User 1: The Matrix=1, Arrival=0, Dune=0, Star Wars=1, Iron Man=1 | User 2: The Matrix=0, Arrival=1, Dune=0, Star Wars=1, Iron Man=1)*

- (a) 1/2 ✓
- (b) 3/4
- (c) 1
- (d) 0

---

### Notebook Open-Response Questions (Lab 2)

**6.** What does cosine distance represent in the example above? *(after computing cosineDist(data[0], data[1]))*

**7.** What does Euclidean distance represent in the example above? *(after computing minkowskiDistance(data[0], data[1], 2))*

---
---

## LAB 3 — K-Means Clustering

### Multiple Choice

**1.** Is the following a possible output from K-means clustering? *(shows two overlapping clusters C1 and C2)*

- (a) Yes
- (b) No ✓

---

**2.** For a dataset X with N points, when k = 1, the total cost is:

- (a) var(x)
- (b) N ∗ var(x) ✓
- (c) 1
- (d) 0

---

**3.** For a dataset X with N points, when k = N the total cost is:

- (a) var(x)
- (b) N ∗ var(x)
- (c) 1
- (d) 0 ✓

---

**4.** Dataset: [−2, −1.5, .5, 1, 5.5, 6, 6.5]. With initial centroids 0 and 2, what are the final centroids?

- (a) 1 and 5.5
- (b) 0 and 6
- (c) -0.5 and 6 ✓
- (d) 0 and 3.25

---

**5.** Consider the 1-dimensional dataset: [3, 5, x]. With k = 2, what is the smallest integer value of x, (x > 5) for which x will always be alone in its own cluster no matter the initialization?

- (a) 6
- (b) 10 ✓
- (c) 8
- (d) 9

---

**6.** Lloyd's algorithm always converges

- (a) True ✓
- (b) False

---

### Notebook Open-Response Questions (Lab 3)

**Predictions (before running K-Means):**

**7.** Describe the shape of the data.

**8.** What shape of data is optimal for K-Means?

**9.** Do you think this dataset is optimal for K-means?

**Observations (after running K-Means):**

**10.** Does the algorithm converge to an optimal solution?

**11.** How would you describe the behavior of the algorithm through the iterations?

**12.** What about K-Means makes it handle this shape of data poorly (hint: think of the cost function)?

**Bonus:**

**13.** Consider varying the distance between the elongated cluster and the other two clusters. What is the minimum distance between the clusters such that K-means "optimally" identifies the 3 clusters?

---
---

## LAB 4 — K-Means++ and Hierarchical Clustering

### Multiple Choice

**1.** Is the following a possible output of K-means++ clustering? *(shows three roughly equal pie-slice clusters)*

- (a) Yes
- (b) No ✓

---

**2.** To find the optimal number of clusters in K-means, we run K-means multiple times for different values of k then we pick the one with the lowest cost

- (a) True
- (b) False ✓

---

**3.** What does it mean if the silhouette score for a data point is close to 1?

- (a) The cluster is likely tight and far from others ✓
- (b) The point lies on the boundary of clusters
- (c) The point does not belong in its cluster

---

**4.** Let k = 2. Is K-means++ with a Euclidean distance-based cost function ideal for the following data? *(shows elongated cluster + compact cluster)*

- (a) Yes, there are clearly two clusters here
- (b) No, we should use manhattan distance instead to account for the elongated cluster
- (c) No, k-means performs poorly on this data set because it assumes roughly spherical and equal sized clusters ✓

---

**5.** You transform a 2D dataset of concentric circles onto a 1D space using z = (x − x̄)² + (y − ȳ)². Would k-means be able to identify 3 concentric clusters in this new 1 dimensional space?

- (a) Yes ✓
- (b) No

---

**6.** How many clusters would be created by cutting the dendrogram as below? *(dendrogram with horizontal cut line, leaves: 3, 4, 6, 1, 2, 5)*

- (a) 7
- (b) 6
- (c) 5
- (d) 4 ✓

---

**7.** Which link function(s) would make Hierarchical clustering well suited for the following dataset? *(elongated clusters separated from compact cluster)*

- (a) Single-link distance ✓
- (b) Complete-link distance
- (c) Ward's distance
- (d) All of the above

---

**8.** Which clusters get merged if using Euclidean and complete-link distance? *(shows clusters AB, CD, EF with coordinates A(0,0), B(1,1), C(4,1), D(4,0), E(0,−2), F(−1,−2))*

- (a) AB and CD
- (b) CD and EF
- (c) AB and EF ✓

---

**9.** Using Euclidean and complete-link distance for A = (1, 2), B = (3, 5), C = (4, 1), D = (7, 3), E = (6, 6) what is the merging order?

- (a) AC → DE → BDE → ABCDE
- (b) AC → DE → ABC → ABCDE ✓
- (c) AC → ABC → DE → ABCDE

---

**10.** How would you compare the clustering represented by the left plot versus the right plot? (select all that apply)

- (a) the left plot represents 3 clusters, the right plot represents 4 clusters ✓
- (b) the right plot has more data than the left plot
- (c) the gray cluster (top one) on the left plot has more points than the gray cluster (top one) on the right ✓
- (d) the left plot contains at least one point with a negative silhouette score

---

**11.** We TYPICALLY prefer clusterings with higher average silhouette scores and uniformly distributed silhouette scores across data points

- (a) True ✓
- (b) False

---

**12.** What is the average silhouette score for a clustering with k = N?

- (a) 0
- (b) 1 ✓
- (c) ∞
- (d) √k

---

### Notebook Open-Response Questions (Lab 4)

**Interpreting silhouette plots:**

**13.** Which value of k produces the most uniform cluster sizes (similar heights)?

**14.** Which k value has the highest average silhouette score?

**15.** Based on the silhouette analysis, what is the optimal k for this dataset?

---
---

## LAB 5 — Review: K-Means(++), Hierarchical Clustering, DBScan, Soft Clustering

### Multiple Choice

**1.** How will point p be assigned? *(Min_pts = 3; p is near core point k with p partially outside k's epsilon neighborhood)*
*(Note: we are assuming that for a point to be considered a part of p's epsilon neighborhood, it must be entirely in the circle representing p's neighborhood)*

- (a) p is a core point, so we will iterate on its entire epsilon neighborhood
- (b) p is a border point, so we will iterate on its entire epsilon neighborhood
- (c) p is a border point, so we will assign it to k's cluster and move onto the other points in k's neighborhood ✓
- (d) p is a noise point, so we won't assign it to any cluster

---

**2.** Keeping epsilon the same and increasing min_pts in DBScan will likely increase the number of noise points

- (a) True ✓
- (b) False

---

**3.** Keeping epsilon the same and increasing min_pts in DBScan will likely increase the number of core points

- (a) True
- (b) False ✓

---

**4.** Is the following a possible output of DBScan? *(shows 4 petal-shaped clusters C1, C2, C3, C4 overlapping at center)*

- (a) Yes
- (b) No ✓

---

**5.** Is DBScan well suited for the following dataset? *(shows spiral/concentric ring dataset)*

- (a) Yes ✓
- (b) No

---

**6.** DBScan, like K-means, requires you to specify the number of clusters

- (a) Yes
- (b) No ✓

---

**7.** Using cosine distance to calculate epsilon neighborhoods would likely enable us to detect the two natural clusters here.

- (a) True
- (b) False ✓

---

**8.** One way to initialize GMM clustering is to use K-means since it also performs well when clusters are Gaussian

- (a) True ✓
- (b) False

---

**9.** In GMM, what is the likelihood of the data (with N data points) when k=N

- (a) ∞ ✓
- (b) −∞
- (c) 1
- (d) 0

---

**10.** Is the following a possible output from K-means++ clustering? *(same spiral/concentric dataset)*

- (a) Yes ✓
- (b) No

---

**11.** Is the following a possible output of K-means clustering? *(3-cluster spiral/petal dataset)*

- (a) Yes ✓
- (b) No

---

**12.** The difference between K-means and K-means++ is that K-means++ is faster, hence the ++

- (a) True
- (b) False ✓

---

**13.** Consider the 1-dimensional dataset {4,5,x}. With k = 2 and x > 5, what is the smallest value of x BEYOND which x will always be in its own cluster?

- (a) 7 ✓
- (b) 9
- (c) 6
- (d) 8

---

**14.** Is the following a possible output from k-means++ clustering? *(C1 = single point, C2 = large cluster)*

- (a) Yes ✓
- (b) No

---

**15.** Is the following a possible output of k-means clustering? *(C1 large sector, C2 and C3 smaller sectors — pie chart cut)*

- (a) Yes ✓
- (b) No

---

**16.** One way to divide clusters in Hierarchical Clustering's Divisive Algorithm (as opposed to agglomerative) is to use a partitional clustering method like K-means.

- (a) True ✓
- (b) False

---

**17.** Using Euclidean and complete-link distance, what is the merging order for A = (0, 0), B = (1, 1), C = (3, 0), D = (0, −2)?

- (a) AB → ABD → ABCD
- (b) AB → CD → ABCD
- (c) AB → ABC → ABCD ✓

---

**18.** How many clusters would be created by cutting the dendrogram below as shown? *(dendrogram with leaves: 3, 4, 6, 1, 2, 5, 7, 10, 9, 8)*

- (a) 5
- (b) 4
- (c) 6
- (d) 7 ✓

---

**19.** Which clusters get merged next if using Euclidean and complete-link distances? *(clusters AB, CD, EF with A(0,0), B(1,1), C(4,1), D(4,0), E(−1,−2), F(0,−2))*

- (a) AB and EF ✓
- (b) AB and CD
- (c) CD and EF

---

**20.** The Manhattan distance is always less than or equal to the Euclidean distance between two points in a 2D space.

- (a) True
- (b) False ✓

---

**21.** In n-dimensional space the Manhattan distance equals the Euclidean distance for

- (a) Points where all the coordinates are the same except for one ✓
- (b) Points where all the coordinates are different except for one
- (c) Points where all the coordinates are zero except for one
- (d) all of the above

---

**22.** Consider arbitrary points A and B in Rⁿ s.t. A ≠ B. For which distance function d, is d(A, B) invariant to scaling? i.e., c ∗ d(A, B) = d(A, B) for any constant c

- (a) Euclidean distance
- (b) Chebyshev Distance
- (c) Cosine Distance ✓
- (d) Manhattan Distance

---

**23.** What is the Jaccard distance between two completely different documents (i.e. no words in common at all)?

- (a) -1
- (b) 1 ✓
- (c) 0
- (d) Depends on the size of the documents

---

**24.** How many parameters does GMM need to estimate for k clusters and 1D data?

- (a) 3k ✓
- (b) k
- (c) 4k
- (d) √k

---

**25.** Since outliers most likely don't belong to any cluster, the probabilities of belonging to each cluster, assigned by a GMM, will all be small

- (a) True
- (b) False ✓

---

**26.** What type of distribution does each cluster follow in a GMM?

- (a) Normal ✓
- (b) Geometric
- (c) Hypergeometric
- (d) Poisson

---
---

## LAB 7 — Singular Value Decomposition (SVD) / LSA

### Multiple Choice

**1.** As k increases, the frobenius distance between a matrix and its rank-k approximation decreases

- (a) True ✓
- (b) False

---

**2.** The rank-k approximation of an n × m matrix also has dimension n × m.

- (a) True ✓
- (b) False

---

**3.** What is the rank of the following dataset? *(scatter plot showing points roughly along a single line in 2D space)*

- (a) 1
- (b) 2 ✓
- (c) 3
- (d) 4

---

**4.** Let A be an m×n matrix of rank r. After using SVD for feature extraction, we will still have an m × n matrix.

- (a) True
- (b) False ✓

---
---

## LAB 8 — K-Nearest Neighbors (KNN)

### Multiple Choice

**1.** KNN has a long training time

- (a) True
- (b) False ✓

---

**2.** if k is too large in KNN, this can lead to underfitting

- (a) True ✓
- (b) False

---

**3.** What can we use to map the bodies of movie reviews to a space where we can run KNN?

- (a) K-means
- (b) DBScan
- (c) LSA (Latent Semantic Analysis) ✓
- (d) Hierarchical Clustering

---

**4.** What distance function should we use to identify the semantic similarity of LSA-generated embeddings?

- (a) Cosine ✓
- (b) Euclidean
- (c) Manhattan
- (d) Chebyshev

---

### Notebook Open-Response Questions (Lab 8)

**5.** How could we potentially improve our model?

**6.** What are the limitations of KNN in our use case?

**7.** What can we do to try and find the ideal value for k in KNN?

**8.** What would happen if we tried to use a distance function other than cosine?

---
---

## LAB 10 — Support Vector Machines (SVM)

### True/False (from slides)

**1.** If correctly classified points far from the margin are moved farther from the margin, the SVM will always move (i.e., the street)

*(Answer: False — correctly classified points far from the margin do not affect the SVM street)*

---

**2.** Multiplying an SVM by a constant c > 1 will retract the margin of the SVM

*(Answer: True — scaling up w retracts the margin since margin width = 2/‖w‖)*

---

### Short Answer (from slides)

**3.** What is the width of the street for the following SVM: x₁ + x₂ + 1 = 0?

*(Answer: width = 2/‖w‖ = 2/√2 = √2)*

---

**4.** Should we expand or retract this SVM? *(two versions shown in slides — evaluate based on whether margin width > or < 1)*

---
---

## LAB 11 — Linear Regression

### Multiple Choice

**1.** The estimate β̂ is a random variable with mean β

- (a) True ✓
- (b) False

---

**2.** According to linear regression, the following is a linear model: Ŷ = β₀ + β₁X + β₂X²

- (a) True ✓
- (b) False

---

**3.** According to linear regression, the following is a linear model: Ŷ = β₀ + β₁X + β₂²X²

- (a) True
- (b) False ✓

---

**4.** Let's say α = 5%. What are we likely to conclude if we get a p-value of 0.03?

- (a) The likelihood of observing our data under the null hypothesis is low, so we reject the null hypothesis ✓
- (b) The likelihood of observing our data under the null hypothesis is low, so we FAIL to reject the null hypothesis
- (c) The likelihood of observing our data under the null hypothesis is low, so our observation is wrong, and we fail to reject the null hypothesis

---

**5.** Does the following plot indicate homoscedasticity? *(residuals vs fitted plot showing roughly constant band)*

- (a) Yes
- (b) No ✓

---

**6.** Does this NQQ plot support the normality of residuals assumption for linear regression? *(Q-Q plot showing points following diagonal closely)*

- (a) Yes ✓
- (b) No

---

**7.** The following correlation matrix is indicative of high multicollinearity *(heatmap showing 3 features highly correlated with each other)*

- (a) True ✓
- (b) False

---

### Notebook Open-Response Questions (Lab 11)

**8.** What do you observe about the shape of the observed data? Any chance that OLS regression may have been a mistake? What assumptions could we have violated?

**Food for thought (train2.csv):**

**9.** How would you describe the data from train2.csv? Is it skewed, what is its shape?

**10.** Even if you don't know of any other linear models, consider how you would describe the data (e.g., quadratic, logarithmic, etc).

**11.** If we were to fit train2.csv's data to an OLS regression and calculate p-values, would they be trustworthy? Why or why not?

---
---

## LAB 12 — Neural Networks

### Multiple Choice

**1.** Consider a binary classification task requiring 2 input neurons, 4 total hidden neurons, and 1 output neuron. There will be fewer total parameters (i.e., weights and biases) if all the hidden neurons are placed into one hidden layer as opposed to two hidden layers

- (a) True
- (b) False ✓

---

**2.** Consider a binary classification task requiring 1 input neuron, 5 total hidden neurons, and 1 output neuron. There are fewer total parameters in a network where all hidden neurons are in a single hidden layer compared to a network where the neurons are split into two hidden layers, where layer 1 has 2 neurons and layer 2 has 3 neurons, respectively.

- (a) True ✓
- (b) False

---

**3.** The activation function A(x) = x applies a non-linear transformation to the hidden layers

- (a) True
- (b) False ✓

---

**4.** Even with a complex architecture, a neural network with no activation function in hidden layers is the same as a neural network with no hidden layers.

- (a) True ✓
- (b) False

---

**5.** In deep networks with tanh or sigmoid activations, early layers struggle to learn because gradients become too small by the time they reach the first layer

- (a) True ✓
- (b) False

---

**6.** You train a fully connected network with tanh activations and sigmoid outputs. Input features have large positive means. What will happen?

- (a) Most hidden features will be constant (either all 1 or all -1) on initialization and take a very long time to change because gradients are very small. ✓
- (b) It will work fine - neural networks can adapt to any features
- (c) The network will crash because finding the derivative of the sigmoid function is not possible

---

**7.** Consider a single ReLU neuron with weights initialized from a symmetric distribution and data centered at 0. If the bias b is initialized to a small positive value (e.g. 0.01), then more than 50% of data points will make the neuron activate.

- (a) True ✓
- (b) False

---

### Notebook Open-Response / Reflection Questions (Lab 12)

**Minimal Architecture:**

**8.** Pick a target test accuracy (TARGET_ACC) that you think is "good enough" for the spirals. Justify your choice in 1–2 sentences.

**9.** Report the *smallest* architecture from the sweep that hits your target. Is the optimal activation function the same one you would have picked from section 2?

**Compare the techniques:**

**10.** Fill in the table below using your numbers. Which technique gave you the **best test accuracy per parameter** for the spirals problem? Explain in 2–3 sentences why you think that is (think about: how much redundancy each technique can exploit; whether spirals data has the structure that technique assumes).

| Technique           | params  | test_acc | acc / param |
|---------------------|---------|----------|-------------|
| Sweep best          | 9       | 0.920    | 0.1022      |
| Pruning (50%)       | 109\*   | 0.956    | 0.0088      |
| Distilled student   | 17      | 0.928    | 0.0546      |
| Low-rank (best `r`) | 133     | 0.956    | 0.0072      |

**Reflection Questions:**

**R1.** Looking at the activation animations, what does a "dead ReLU neuron" look like? Did your final model have any?

**R2.** Compare `visualizations/arch_baseline_weighted.png` with `visualizations/arch_pruned.png`. Which inputs / hidden-units lost the most connections? Does that match which directions of `X_train` you'd guess matter most?

**R3.** Why does knowledge distillation often produce a student that beats *training the same architecture from scratch* on hard targets? What information is the teacher providing that the raw labels don't?

**R4.** When would low-rank factorization be most useful, and when would it *not* help much? (Hint: think about the rank of the trained weight matrix.)

**R5.** Considering everything you've seen, write down the rule of thumb you'd use to pick (i) an activation function and (ii) a hidden layer size if you were given a brand-new 2D classification problem you hadn't seen before.

---
---

## LAB 12 GLM — Generalized Linear Models

### True/False & Multiple Choice (from slides)

**1.** Recall: Which of the following assumptions does a residual NQQ plot allow us to test for an ordinary linear regression?

*(Answer: Normality of residuals)*

---

**2.** True or false: the following NQQ plot indicates that this dataset has normally distributed residuals *(plot shown in slide)*

*(Answer depends on shape of the Q-Q plot shown)*

---

**3.** Recall: which of the following assumptions does a residual vs. fitted values plot allow us to test (select all that apply)?

*(Answer: Linearity of relationship between predictors and outcome; Homoscedasticity / constant variance of residuals)*

---

**4.** True or false: the following residual vs. fitted values plot indicates that this dataset has a linear relationship between predictors and response, and homoscedasticity *(plot shown in slide)*

*(Answer depends on the plot shown — likely False given the GLM context)*

---
---

## QUICK REFERENCE — Answers Summary

### Lab 2
1. (a) √2 | 2. (b) 2 | 3. (a) 1/4 | 4. (a) √2/2 | 5. (a) 1/2

### Lab 3
1. (b) No | 2. (b) N∗var(x) | 3. (d) 0 | 4. (c) −0.5 and 6 | 5. (b) 10 | 6. (a) True

### Lab 4
1. (b) No | 2. (b) False | 3. (a) tight & far from others | 4. (c) No, k-means assumes spherical equal-sized clusters | 5. (a) Yes | 6. (d) 4 | 7. (a) Single-link | 8. (c) AB and EF | 9. (b) AC→DE→ABC→ABCDE | 10. (a)(c) | 11. (a) True | 12. (b) 1

### Lab 5 (Review)
1. (c) border point, assign to k's cluster | 2. (a) True | 3. (b) False | 4. (b) No | 5. (a) Yes | 6. (b) No | 7. (b) False | 8. (a) True | 9. (a) ∞ | 10. (a) Yes | 11. (a) Yes | 12. (b) False | 13. (a) 7 | 14. (a) Yes | 15. (a) Yes | 16. (a) True | 17. (c) AB→ABC→ABCD | 18. (d) 7 | 19. (a) AB and EF | 20. (b) False | 21. (a) same except one | 22. (c) Cosine Distance | 23. (b) 1 | 24. (a) 3k | 25. False | 26. (a) Normal

### Lab 7
1. True | 2. True | 3. 2 | 4. False

### Lab 8
1. False | 2. True | 3. LSA | 4. Cosine

### Lab 11
1. True | 2. True | 3. False | 4. (a) reject null | 5. No | 6. Yes | 7. True

### Lab 12
1. False | 2. True | 3. False | 4. True | 5. True | 6. (a) | 7. True
