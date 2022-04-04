# Ceres Solver


## Links
* [Ceres Website](http://ceres-solver.org/index.html)
* [Ceres Github Repo](https://github.com/ceres-solver/ceres-solver)


## Background
Ceres Solver is a C++ library used to optimize large and complicated problems. In particular Ceres is known for being able to solve Non-linear Least Squares problems. It has been used by Google for over a decade. 

Features of the library include a robust modeling API that supports Derivatives, Loss Functions and Manifolds; as well as a recognition system to implement the most appropriate optimization algorithm to best suit the needs of a system when solving complex problems like Non-linear Conjugate Gradients and Levenburg-Marquardt methods.

## Key Problems Solved
Rootfinding? Interpolation? Regression?
Is it general-purpose software or domain-specific? What makes it unique?

## Stakeholders
Who develops the software, who uses it, who pays for it?
What are they looking for?
How do they communicate and collaborate?
Who uses the software?
Who is impacted (positively or negatively) by use of the software?

## Metrics and Features
How do concepts like accuracy, conditioning, stability, and cost appear?
If the software is fast, how is "fast" defined?
If the software is accurate, what does accuracy mean? Could you make a plot, say accuracy vs cost? How would you label the axes to make it relevant to a stakeholder?
Would different stakeholders want different axes (because they care about different things)?
Are there modeling decisions made in the interest of good conditioning? Are there algorithmic choices made for stability?

## What I've Learned
In the tutorial I completed, I used Ceres Solver to solve bounds constrained robustified non-linear least squares problems in the form:
![image](https://raw.githubusercontent.com/cu-numcomp/spring22-project-liho2210/main/img/Screen%20Shot%202022-04-03%20at%208.14.47%20PM.png?token=GHSAT0AAAAAABQS4WURP2V55UTHEF7KGQF2YSTR7TA)
$$\begin{split}\min_{\mathbf{x}} &\quad \frac{1}{2}\sum_{i} \rho_i\left(\left\|f_i\left(x_{i_1}, ... ,x_{i_k}\right)\right\|^2\right) \\
\text{s.t.} &\quad l_j \le x_j \le u_j\end{split}$$

## Questions

## Potential Experiments


```python

```
