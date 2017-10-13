# The Perceptoron Learning Algorithm

Implementation in python, using Jupyter Notebook.

The algorithm creates a target function f and data set D to visualize on simple example
how the Perceptron Learning Algorithm works. It takes d = 2 (2 dimensions)
and assumes X = [−1, 1] × [−1, 1] with uniform probability of picking each
x ∈ X .

In each run, we choose a random line in the plane as the target function f (picks two points on a plane
randomly and finds a line passing though them), one side of the line maps to +1 and the other maps
to −1. We then choose the inputs xn (vector) of the data set as random points (uniformly in X), and
we evaluate the target function on each xn to get the corresponding output yn.
Now, in each run, we use the Perceptron Learning Algorithm to find g. We start the PLA
with the weight vector w being all zeros (sign(0) = 0 => all points are initially
misclassified), and at each iteration the algorithm chooses a point randomly
from the set of misclassified points and adjusts weights to classify the chosen point correctly.

To visualize the performance we find two quantities: the number of iterations that PLA takes to converge to g,
and the disagreement between f and g which is P[f(x) 6= g(x)] (disagreement between f and g functions on their
classification of a random point).

The main method - ```perform_experiments(number_of_points)``` takes an integer argument (N) which indicated the
number of training points for PLA.
The two constants ```NUMBER_OF_EXPERIMENTS``` and ```NUMBER_OF_TEST_POINTS``` are set accordingly to
1000 and 400 (feel free to change them!)

The last two cells are used for plotting the single experiment (PLA for a set of N points)
for N = 10 and N = 100. Two files N=10.png and N=100.png, in my opinion, illustrate well how accurate PLA
is for these cases (how close to each other are f and g)
