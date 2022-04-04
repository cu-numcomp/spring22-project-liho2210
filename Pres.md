# Ceres Solver


## Links
* [Ceres Website](http://ceres-solver.org/index.html)
* [Ceres Github Repo](https://github.com/ceres-solver/ceres-solver)
* [Additional Tutorial](https://towardsdatascience.com/how-to-create-a-c-project-using-ceres-solver-f3d67c8044f3)


## Background
Ceres Solver is a C++ library used to optimize large and complicated problems. In particular Ceres is known for being able to solve Non-linear Least Squares problems. It has been used by Google for over a decade. 

## Key Problems Solved
Ceres is a domain-specific tool used primarily for modeling and solving complex optimization problems like non-linear least squares problems with bounds constraints and unconstrained general optimization problems. 

## Stakeholders
The software is open source, but primarily developed by a small team. Notable users include Google, Blender, Microsoft and OpenMVG. Primarily, users implement Ceres to aid in estimation techniques related to 3D imaging and bundle adjustment. 
The developers allow for contribution from outside developers through their GitHub repository. 

## Metrics and Features
Features of the library include a robust modeling API that supports Derivatives, Loss Functions and Manifolds; as well as a recognition system to implement the most appropriate optimization algorithm to best suit the needs of a system when solving complex problems like Non-linear Conjugate Gradients and Levenburg-Marquardt methods.
Ceres boasts an extensively optimized code base designed with C++ templating, which along with GPU acceleration support for NVIDIA GPU cards, provides high speed solving ability. 

<p align="center">
  <img src="https://raw.githubusercontent.com/cu-numcomp/spring22-project-liho2210/main/img/Screen%20Shot%202022-04-04%20at%2011.39.28%20AM.png?token=GHSAT0AAAAAABQS4WUROJINQLI3W76TKMX4YSUNABA" />
</p>


## What I've Learned
Both of the tutorials I used were very unhelpful for a new user. The installation process was tedious and poorly documented. After many hours of trial and error, I was finally able to get the system installed on a virtual machine and play around with the functionality.

In the first tutorial I completed, I used Ceres Solver to solve bounds constrained robustified non-linear least squares problems in the form:
<p align="center">
  <img src="https://raw.githubusercontent.com/cu-numcomp/spring22-project-liho2210/main/img/Screen%20Shot%202022-04-03%20at%208.14.47%20PM.png?token=GHSAT0AAAAAABQS4WURP2V55UTHEF7KGQF2YSTR7TA" />
</p>

The expression within the sum of the equation above is known as the Residual Block, with the term (xi1, ..., xik) is known as the Parameter Block. F_i() represents a Cost Function and p_i() is a Loss Function. In cases where p_i(x) = x and the bounds Lj and Uj are negative infinity and infinity, respectively, the result is a non-linear least squares problem in the form: 

<p align="center">
  <img src="https://raw.githubusercontent.com/cu-numcomp/spring22-project-liho2210/main/img/Screen%20Shot%202022-04-03%20at%209.11.06%20PM.png?token=GHSAT0AAAAAABQS4WUQCOYLGNK53LSX2F3SYSTTR5A" />
</p>

After creating the required Cost Functor to compute the residual function and constructing a non-linear least squares problem to use it, I ran the included 'helloworld' file using Ceres Solver, and the resulting output was displayed:
<p align="center">
  <img src="https://raw.githubusercontent.com/cu-numcomp/spring22-project-liho2210/main/img/Screen%20Shot%202022-04-04%20at%2011.03.48%20AM.png?token=GHSAT0AAAAAABQS4WURTPGXXQXK3BBS7JFUYSUMKOQ" />
</p>

Here we can see Ceres iterate through the function:
<p align="center">
  <img src="https://raw.githubusercontent.com/cu-numcomp/spring22-project-liho2210/main/img/Screen%20Shot%202022-04-04%20at%2011.18.57%20AM.png?token=GHSAT0AAAAAABQS4WURVYJ73BYEMQJ2LOJMYSUMQ5Q" />
</p>

The minimum is defined. Cost is reduced from 4.5125e+01 to 5.02552e-16 and the minimum converges to 10.

## Questions
One question I have about this software is how the flow of functions works throughout the installed directories. There are binary files which will run and invoke the Ceres analysis, but I don't fully understand where to put new files as to make adjustments and experiment with custom values/functions. I will continue to investigate as I work through more tutorials.

## Potential Experiments
A potential experiment for this software would be to analyze the iterative process Ceres follows to solve a complex rootfinding or optimization problem, and compare the cost to that of a different process or simpler solver technique. 

```python

```
