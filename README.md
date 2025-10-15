# Supercoefficients for Kerr-cat

This project is a python package that demonstrates supercoefficient approach for the analysis of the 
parametrically driven single-degree-of-freedom circuits, based on the theory presented 
in the paper [**"Exact amplitudes of parametric processes in driven Josephson circuits"**](https://arxiv.org/abs/2501.07784).

Supercoefficent approach allows to calculate the amplitudes of various parametric processes present
in a circuit Hamiltonian. the bookkeeping is made systematic by coefficients which appropriately
keep track of the order of each parametric process. The main advantage of the approach that it is
agnostic to the system Hamiltonian, reminiscent to a Taylor series of a function:
$$
\hat{{H}}=\omega_0\hat{a}^\dag\hat{a}+&\sum\limits_{ n,l,p=0}^{\{l,p\}^\prime}{C}_{nl,p}(\hat{a}^{\dag n}\hat{a}^{n+l}+\hat{a}^{\dag n+l}\hat{a}^{n})(e^{ip(\omega_d{t}{+}\gamma)}+e^{-ip(\omega_d{t}{+}\gamma)})
$$
The concrete coeffcients, ${C}_{nl,p}$, contain comprehensive information about the circuit and make it easier to distinguish 
and track how different properties—such as drive power, circuit topology, and zero-point fluctuations—contribute 
to the various parametric processes.

$L_\mathrm{U} = \dfrac{\Phi_0}{2\pi I_\mathrm{U}}$


# installation instructions

The project requires the following packages:

- numpy (mandatory)
- sympy (mandatory)
- scipy (mandatory)
- jupyter (for examples)
- matplotlib (for examples)

Schrieffer-Wolff procedure generator (currently under the development and distributed as a wheel only)
-swg (downloadadle from https://dl.cloudsmith.io/public/cs-x033/swg/python/simple/)

To install project, execute "pip install -r requirements.txt" in the package directory.

The package could be rebuilt locally with "python -m build" and installed with pip from dist directory 
but still requires "ip install swg --index-url https://dl.cloudsmith.io/public/cs-x033/swg/python/simple/" before swg package is made public.

# Examples

You can start exploring project's functionality by running the .ipynb files in 'examples'. The examples include:

- General guide for the optimization of circuit designs (example for a Kerr-cat).
- Full scale simulation to benchmark the Kerr-cat circuit designs for the case of SNAIL- and SQUID-based driven circuits
- Agnostic Schrieffer-Wolff procedure for the case of multiple drives in single-degree-of-freedom circuits.

# citing 

If you use the project for your research, please cite [**this article**](https://arxiv.org/abs/2501.07784).

# contacts

For inquiries, comments, suggestions etc. you can contact the authors at **supercoefficients@gmail.com**.

# acknowledgements

The project uses some GUI widgets from [ninatool](https://github.com/sandromiano/ninatool) repo. The main functionality of NINA is 
to compute the Taylor expansion coefficient of the effective potential energy function of an arbitrary flux-biased 
superconducting loop. The loop can host any combination of Josephson junctions (JJs) and linear inductances. NINA can also
 compute the Hamiltonian series expansion of an arbitrary Josephson nonlinear oscillator (limited for now to a single mode).

