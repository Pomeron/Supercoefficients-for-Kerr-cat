# Supercoefficients for Kerr-cat

This project is a Python package that demonstrates the supercoefficient approach for the analysis of the  
parametrically driven single-degree-of-freedom circuits, based on the theory presented  
in the paper [**"Exact amplitudes of parametric processes in driven Josephson circuits"**](https://arxiv.org/abs/2501.07784).

The supercoefficient approach allows to calculate the amplitudes of various parametric processes present  
in a circuit Hamiltonian. The bookkeeping is made systematic by coefficients which appropriately  
keep track of the order of each parametric process. The main advantage of the approach is that it is  
agnostic to the system Hamiltonian, reminiscent of a Taylor series of a function:

$$
\hat{{H}}=\omega_0\hat{a}^\dagger\hat{a}+\sum\limits_{ n,l,p=0}{C}_{nl,p}(\hat{a}^{\dagger n}\hat{a}^{n+l}+\hat{a}^{\dagger n+l}\hat{a}^{n})(e^{ip(\omega_d{t}{+}\gamma)}+e^{-ip(\omega_d{t}{+}\gamma)})
$$

The concrete coefficients, $C_{nl,p}$, contain comprehensive information about the circuit and make it easier to distinguish  
and track how different properties—such as drive power, circuit topology, and zero-point fluctuations—contribute  
to the various parametric processes.

# Installation Instructions

The project requires the following packages:

- numpy (mandatory)
- sympy (mandatory)
- scipy (mandatory)
- swg (Schrieffer-Wolff procedure generator which is currently under development and distributed as a wheel only. Downloadable from [**Cloudsmith**](https://dl.cloudsmith.io/public/cs-x033/swg/python/simple/))
- [ninatool](https://github.com/sandromiano/ninatool)
- jupyter (for examples)
- matplotlib (for examples)

To install the project, execute:

`pip install -r requirements.txt` 

in the package directory.

The package can be rebuilt locally with:

`python -m build`


and installed with pip from the `dist` directory,  
but still requires:

`pip install swg --index-url https://dl.cloudsmith.io/public/cs-x033/swg/python/simple/` 

before the `swg` package is made public.

# Examples

You can start exploring the project's functionality by running the `.ipynb` files in `examples`. The examples include:

- General guide for the optimization of circuit designs (example for a Kerr-cat).
- Full-scale simulation to benchmark the Kerr-cat circuit designs for the case of SNAIL- and SQUID-based driven circuits.
- Agnostic Schrieffer-Wolff procedure for the case of multiple drives in single-degree-of-freedom circuits.

# Citing

If you use the project for your research, please cite [**this article**](https://arxiv.org/abs/2501.07784).

# Contacts

For inquiries, comments, suggestions, etc., you can contact the authors at **supercoefficients@gmail.com**.

# Acknowledgements

The project uses some functionality from the [ninatool](https://github.com/sandromiano/ninatool) repo. The main functionality of NINA is  
to compute the Taylor expansion coefficients of the effective potential energy function of an arbitrary flux-biased  
superconducting loop. The loop can host any combination of Josephson junctions (JJs) and linear inductances. NINA can also  
compute the Hamiltonian series expansion of an arbitrary Josephson nonlinear oscillator (limited for now to a single mode).
