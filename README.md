# CS-559-Homework-7-solution

Download Here: [CS 559 Homework #7 solution](https://jarviscodinghub.com/assignment/cs-559-homework-7-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

1. (100pts) In this computer project, we will design an SVM. You may use an existing library for solving the
quadratic optimization problem that is associated with the SVM. For example, the free software Octave has
such a command named “quadprog” to solve such problems. Other than that, you cannot use any existing
machine learning/SVM library. As usual, please include the computer codes in your report.
(a) Draw 100 points x1, . . . , x100 independently and uniformly at random on [0, 1]2
. These will be our input
patterns.
(b) Given xi =

xi1
xi2

, let
di =

1, xi2 < 1 5 sin(10xi1) + 0.3 or (xi2 − 0.8)2 + (xi1 − 0.5)2 < 0.152 −1, otherwise (1) denote the desired classes corresponding to the input patterns. Let C1 = {xi : di = 1} and C−1 = {xi : di = −1}. The region where di is 1 is the union of the region that remains below the mountains and the region that remains inside the sun in the figure below. Sketch the points xi , indicate (with different colors or markers) their desired class. Make sure your samples include at least one point inside the sun. (c) Pick an appropriate kernel (write it down in your report) and design an SVM that separates the classes C1 and C−1. Recall that the result of the SVM will be a discriminant function g(x) = PIs i=1 αidiK(xi , x) +θ, where αi are some positive constants, Is is the set of the indices of support vectors, and θ is the optimal bias. Provide a rough sketch of the decision boundaries H , {x : g(x) = 0} H+ , {x : g(x) = 1} H− , {x : g(x) = −1}. 1 together with the support vectors. Note that the support vectors will be either on H+ or H−. Your SVM should be able to perfectly separate the two classes with no exceptions of misclassified input patterns. Example solution: What I am expecting is a figure like this. The red crosses are input patterns with desired class 1, and the black diamonds are the input patterns with desired class −1. The decision boundary H (the blue line) can perfectly separate the two classes that were otherwise not linearly separable. There are 7 support vectors (marked by black circles) on H+ (the black line), and 6 support vectors (marked by red circles) in H− (the red line) for a total of 13 support vectors. As expected, there are no patterns in between the “guard lines” H+ and H−. Of course, the Kernel that I used is a secret. Note that plotting the decision boundary H , {x : g(x) = 0} (or plotting H+ or H−) as a nice perfect line is quite a difficult task. What you can do instead is to approximate it as: for x1 = 0, 0.001, 0.002, . . . , 0.999, 1 for x2 = 0, 0.001, 0.002, . . . , 0.999, 1 if g(x) is close enough to 0, then put a point in coordinates (x1, x2). end end That is more-or-less what I did in my own figure (That is why the decision boundaries are not perfect and there are some “gaps” in between, you can even see the points that form the lines when you zoom in the PDF). Of course, you can use better techniques for generating the boundary curves if you like.
