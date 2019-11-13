The Forward Problem
===================

Many types of wave motion can be described mathematically by the equation :math:`u_{tt} = \nabla \cdot (c^2\nabla u)+f`. We use a more compact notation for the partial derivatives to save space:

.. math::

	u_t = \frac{\partial u}{\partial t}, \quad u_{tt} = \frac{\partial^2 u}{\partial t^2} 

Let's implement a solver for the 1D scalar acoustic wave equation with absorbing boundary conditions. Let :math:`u(x,t)` be the displacement at time t and at space location x, which is the wavefield. The displacement function :math:`u` is governed by the following mathematical model.

.. :label: euler

.. math::

	\begin{split}
	\frac{1}{c(x)^2} u_{tt}(x,t) - u_{xx}(x,t) & = f(x,t), \\ 
	\frac{1}{c(0)}u_t(0,t)-u_x(0,t) & = 0, \\ 
	\frac{1}{c(1)}u_t(1,t)+u_x(1,t) & = 0, \\ 
	u(x,t) & = 0 \quad\text{for}\quad t \le 0,
	\end{split}


where the middle two equations are the absorbing boundary conditions, the last equation gives initial conditions, :math:`x \in [0,1]`, and :math:`t \in [0,T]`. The model velocity is given by the function :math:`c(x)`.

In our notation, we write that solving this PDE is equivalent to applying a nonlinear operator :math:`\mathcal{F}` to a model parameter :math:`m`, where :math:`m(x) = \frac{1}{c(x)^2}` for the scalar acoustics problem.

We then write that :math:`\mathcal{F}[m] = u`.

.. :doc:`source <./source>`

Contents:

.. toctree::
   :maxdepth: 1

   source.rst