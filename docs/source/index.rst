.. role:: underline
    :class: underline

Welcome to HODLR's Documentation!
*********************************

About HODLR:
============

:math:`\texttt{HODLR}` is a fast solver for matrices based on the Hierarchical Off-Diagonal Low-Rank (HODLR) structure. This software is the implementation and the extension of `this <https://link.springer.com/article/10.1007/s10915-013-9714-z>`_ article. The solver has also been extended to matrices not necessarily arising out of kernels and higher dimensions.Low-rank approximation of the appropriate blocks are obtained using rook pivoting. The domain is subdivided based on a KDTree. The solver is fairly general, works with minimal restrictions and has been parallelized using OpenMP

The code is written in C++ and features an easy-to-use interface, where the user provides input through a ``kernel`` object which abstracts data of the matrix through a member function `getMatrixEntry(int i, int j)` which returns the entry at the :math:`i^{\mathrm{th}}` row and :math:`j^{\mathrm{th}}` column of the matrix.

The current release has the following capabilities:

- Fast MatVecs: Obtains :math:`A x` at a cost of :math:`\mathcal{O}\left(N\log{N}\right)`
- Fast Solve: Solves linear systems :math:`A x = b` in :math:`\mathcal{O}\left(N\log^2\left(N\right)\right)`
- Fast Determinant Computation: Additional Cost of :math:`\mathcal{O}\left(N\log{N} \right)`

Doc Contents
============
.. toctree::
   :maxdepth: 2
   :caption: Contents:

   home
   installation

Other Links
===========

Learn more about HODLR by visiting the

* Code Repository: http://github.com/sivaramambikasaran/HODLR
* Documentation: http://hodlr.rtfd.io
