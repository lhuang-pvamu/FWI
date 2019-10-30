The Forward Problem
===================


In this exercise, you will implement a solver for the 1D scalar acoustic wave equation with absorbing boundary conditions,

.. math::

	\begin{split}
	(\frac{1}{c(x)^2}\partial_{t^2}-\partial_{x^2})u(x,t) & = f(x,t), \\ 
	(\frac{1}{c(0)}\partial_t-\partial_x)u(0,t) & = 0, \\ 
	(\frac{1}{c(1)}\partial_t+\partial_x)u(1,t) & = 0, \\ 
	u(x,t) & = 0 \quad\text{for}\quad t \le 0,
	\end{split}


where the middle two equations are the absorbing boundary conditions, the last equation gives initial conditions, :math:`x \in [0,1]`, and :math:`t \in [0,T]`. The model velocity is given by the function :math:`c(x)`.

In our notation, we write that solving this PDE is equivalent to applying a nonlinear operator \(\mathcal{F}\) to a model parameter \(m\), where :math:`m(x) = \frac{1}{c(x)^2}` for the scalar acoustics problem.

We then write that :math:`\mathcal{F}[m] = u`.
