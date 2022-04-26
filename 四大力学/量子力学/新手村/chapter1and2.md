Introduction to Quantum Mechanics
[TOC]

# Part Ⅰ Theory

## 1 The Wave Function

#### 1.1 The Schrodinger Equation

Looking for Particle's wave function$$
\Psi(x,t)
$$by solving the Schrodinger equation$$
i\hbar\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2}+V\Psi
$$Planck's constant$$
\hbar = \frac{h}{2\pi}=1.054573\times10^{-34} \mathrm{Js}
$$

#### 1.2 The Statistical Interpretation

Born's statistical interpretation$$
\int_a^b|\Psi(x,t)|^2\,{\rm d}x = \{\text{probability of finding the particle between a and b}\}
$$

- All quantum mechanics has to offer is statistical information about the possible results.


#### 1.3 Probability

##### 1.3.1 Discrete Variables

The average value of some *function* of *j* is given by $$
\langle f(j)\rangle = \sum_{j=0}^\infty f(j)P(j)
$$The **variance** of the distribution$$
\sigma^2\equiv\lang(\Delta j)^2\rang
$$The **standard deviation**$$
\sigma = \sqrt{\lang j^2\rang - \lang j\rang^2}
$$

##### 1.3.2 Continuous Variables

$\rho(x)$: **probability density**$$
P_{ab} = \int_a^b\rho(x)\,{\rm d}x
$$Rules:$$
\int_{-\infty}^\infty\rho(x)\,{\rm d}x=1 \\
\lang x\rang=\int_{-\infty}^\infty x\rho(x)\,{\rm d}x \\
\lang f(x)\rang=\int_{-\infty}^\infty f(x)\rho(x)\,{\rm d}x \\
\sigma^2 \equiv\lang(\Delta x)^2\rang=\lang x^2\rang-\lang x\rang^2
$$

#### 1.4 Normalization 

**Normalizing** the wave function (square-integrable)$$
\int_{-\infty}^\infty|\Psi(x)|^2\,{\rm d}x=1
$$Proof the Schrodinger equation automatically preserves the normalization of the wave function: $$
\begin{aligned}
    \frac{\partial\Psi}{\partial t} = \frac{i\hbar}{2m}\frac{\partial^2\Psi}{\partial x^2}-\frac{i}{\hbar}V\Psi 
    &,\quad\frac{\partial\Psi^*}{\partial t} = -\frac{i\hbar}{2m}\frac{\partial^2\Psi^*}{\partial x^2}+\frac{i}{\hbar}V\Psi^* \\ &\downarrow\\
    \frac{\partial}{\partial t}|\Psi|^2=\frac{\partial}{\partial t}(\Psi^*\Psi) & =\Psi^*\frac{\partial\Psi}{\partial t}+\frac{\partial \Psi^*}{\partial t}\Psi \\ &\downarrow \\
\frac{d}{dt}\int_{-\infty}^\infty|\Psi(x)|^2\,{\rm d}x &= \int_{-\infty}^\infty\frac{\partial }{\partial t}|\Psi(x)|^2\,{\rm d}x=0 \qquad {\rm QED}
\end{aligned}
$$


#### 1.5 Momentum

For a particle in state $\Psi$, the expectation value of $x$ is$$
\lang x\rang=\int_{-\infty}^\infty x|\Psi(x)|^2\,{\rm d}x = \int\Psi^*\left[x\right]\Psi\,{\rm d}x
$$the expectation value of **momentum** is $$
\lang p\rang=m\frac{d\lang x\rang}{dt}=-i\hbar\int\left(\Psi^*\frac{\partial\Psi}{\partial x}\right)dx = \int\Psi^*\left[-i\hbar(\partial/\partial x)\right]\Psi\,{\rm d}x
$$
- operator: $x\rightarrow \text{position}; -i\hbar(\partial/\partial x)\rightarrow\text{momentum}$

the expectation of any $Q(x,p)$ is $$
\lang Q(x,p)\rang = \int\Psi^*[Q(x,-i\hbar\partial/\partial x)]\Psi\,{\rm d}x
$$

- **Ehrenfest's theorem**$$
\frac{d\lang p\rang}{dt} = \left\langle \frac{\partial V}{\partial x}\right\rangle 
$$proof: $
\frac{d\lang p\rang}{dt} = -i\hbar\int \frac{\partial}{\partial t}\left(\Psi^*\frac{\partial\Psi}{\partial x}\right)=-i\hbar\left(\frac{i}{\hbar}\right)\int-|\Psi|^2\frac{\partial V}{\partial x}dx
$

#### 1.6 The Uncertainty Principle

- **de Broglie formula** $$
p=\frac{h}{\lambda}=\frac{2\pi\hbar}{\lambda}
$$

- Heisenberg's **uncertainty principle**$$
\sigma_x\sigma_p\geq\frac{\hbar}{2}
$$


##  2 Time-Independent Schrodinger Equation

#### 2.1 Stationary States

 Separation of variables $\Psi(x,t)=\psi(x)\varphi((t)$
 $$
\begin{aligned}
    \frac{d\varphi}{dt} &= -\frac{iE}{\hbar}\varphi \qquad\rightarrow \qquad\varphi(t)=e^{iEt/\hbar} \\
    -\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}&+V\psi =E\psi \qquad \text{time-independent Schrodinger equation}
\end{aligned}
$$

Three Answers: 
  
- stationary states $$
\Psi(x,t) = \psi(x)e^{iEt/\hbar}
$$
- *states of definite total energy*  
  - **Hamiltonian** : $H(x,p)=\frac{p^2}{2m}+V(x)$ 
  -  Hamiltonian *operator* : $$\hat{H}=-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}+V(x)$$
  - Rewrite time-independent S_e : $$
\hat{H} \psi= E\psi
$$
  -   expectation value of the total energy : $\langle H\rangle=E$ & $\langle H^2\rangle=E^2$
  - variance: $\sigma_H=0$    
- **linear combination** of separable solutions  $$
\Psi(x,t) = \sum_{n-1}^\infty c_n\psi(x)e^{-iE_n t/\hbar}=\sum_{n-1}^\infty c_n\Psi_n(x,t)
$$
  - stationary states $\Psi_n(x,t) = \psi_n(x)e^{iEt/\hbar}$
  - $|c_n|^2$ : *probability* that a measurement of the energy would return the value $E_n$ $$
\sum_{n-1}^\infty |c_n|^2=1  \\
\langle H\rangle=\sum_{n-1}^\infty |c_n|^2E_n
$$

Four therom 
- For  normalizable solutions, the separation constant $E$ must be $real$
- $\psi(x)$ can always be taken to $real$
- If $V(-x)=V(x)$ then $\psi(x)$ can always be taken to be either even or odd
- $E$ must $> V_{min}$


#### 2.2 The Infinite Square Well

> $$
V(x) = \begin{dcases}
    0  & 0\leq x \leq a \\
    \infty & otherwise
\end{dcases}
$$

Outside the well, $\psi(x) = 0$
Inside the well (**simple harmonic oscillator** equation)$$
\frac{d^2\psi}{dx^2} = -k^2\psi,\qquad \text{where} \,k\equiv\frac{\sqrt{2mE}}{\hbar}
$$
 - $E\geq 0$
 - general solution: $\psi(x) = A\sin(kx)+B\cos(kx)$
 - **boundary conditions**: $\psi(0)=\psi(a)=0$
 - *distinct* solutions & normalize  $$
\psi_n(x)\sqrt{\frac{2}{a}}\sin\left(\frac{n\pi}{a}x\right),\qquad\text{with} \, E_n=\frac{n^2\pi^2\hbar^2}{2ma^2}\quad(n=1,2,3,...)
$$
 - **ground state**: $\psi_1$ 
 - propeties for $\psi_n$
   - alternately **even** or **odd**
   - each successive state has one more **node**(zero-crossing)
   - matually **orthogonal** $$
\int\psi_m(x)^*\psi_n(x)\,{\rm d}x=\delta_{mn}
$$
   - **complete** $$
f(x) = \sum_{n=1}^\infty c_n\psi_n(x) \qquad c_n=\int\psi_n(x)^*f(x)\,{\rm d}x
$$

- $\bigstar$ $$
\Psi(x,t)=\sum_{n=1}^{\infty}c_n\sqrt{\frac{2}{a}}\sin \left(\frac{n\pi}{a}x\right)e^{-i(n^2\pi^2\hbar/2ma^2)t} \\ 
c_n = \sqrt{\frac{2}{a}}\int_0^a\sin\left(\frac{n\pi}{a}x\right)\Psi(x,0)\,{\rm d}x
$$

- $$
\hat{H}\psi_n = E_n\psi_n \quad\rightarrow \quad \langle H\rangle = \sum |c_n|^2E_n$$

<br>

#### 2.3 The Harmonic Oscillator

> $$V(x)=\frac{1}{2}m\omega^2 x^2 \\ \hat{H} = \frac{1}{2m}\left[\hat{p}+(m\omega x)^2\right]$$

##### 2.3.1 Algebratic Method

$$
\left[\hat{A},\hat{B}\right] \equiv \hat{A}\hat{B} - \hat{B}\hat{A}  \rightarrow \left[x,\hat{p} \right] = i\hbar \\
\hat{a}_{\pm}\equiv\frac{1}{\sqrt{2\hbar m\omega}}(\mp i\hat{p}+m\omega x) \, \rightarrow \, \begin{dcases}
    x = \sqrt{\frac{\hbar}{2m\omega}}(\hat{a}_++\hat{a}_-)\\
    \hat{p} = i\sqrt{\frac{\hbar m\omega}{2}}(\hat{a}_+-\hat{a}_-)
\end{dcases} \\
\downarrow \\
\begin{dcases}
    \hat{a}_+\hat{a}_- = \frac{1}{\hbar\omega}\hat{H}-\frac{1}{2}  \\ 
    \hat{a}_-\hat{a}_+ = \frac{1}{\hbar\omega}\hat{H}+\frac{1}{2}  \\ 
\end{dcases} \qquad \rightarrow  \qquad \bigstar \quad
    \hbar\omega\left(\hat{a}_{\pm}\hat{a}_{\mp}\pm \frac{1}{2} \right)\psi = E \psi \\  \downarrow \\
\begin{aligned}   
    \hat{H}(\hat{a}_+\psi) = (E+\hbar\omega)(\hat{a}_+\psi)  \\
    \hat{H}(\hat{a}_-\psi) = (E-\hbar\omega)(\hat{a}_-\psi)  
\end{aligned}
$$

There occurs a "lowest rung" : $\hat{a}_-\psi_0=0 \,\rightarrow\, $ $$
\psi_0 = \left(\frac{m\omega}{\pi\hbar}\right)^{1/4}e^{-\frac{m\omega}{2\hbar}x^2},\qquad \text{with}\qquad E_0 =\frac{1}{2}\hbar\omega
$$

Exited states, increasing the energy by $\hbar\omega$ with each step: $$
\psi_n=A_n(\hat{a}_+)^n\psi_0(x),\qquad \text{with}\qquad E_n = \left(n+\frac{1}{2}\right)\hbar\omega
$$

Normalization algebraically 
 - $\hat{a}_+\psi_n=c_n\psi_{n+1},\qquad \hat{a}_-\psi_n=d_n\psi_{n-1}$

$$
\int_{-\infty}^\infty f^*(\hat{a}_{\pm}g)\,{\rm d}x = \int_{-\infty}^\infty (\hat{a}_{\mp}f)^*g\,{\rm d}x \\ \downarrow \\
 \\\begin{cases}
     c_n = \sqrt{n+1} \\
     d_n = \sqrt{n}
 \end{cases}\qquad\leftarrow 
 \,\begin{dcases}
    \int_{-\infty}^\infty (\hat{a}_{\pm}\psi_n)^*(\hat{a}_{\pm}\psi_n)\,{\rm d}x = \int_{-\infty}^\infty (\hat{a}_{\mp}\hat{a}_{\pm}\psi_n)^*\psi_n\,{\rm d}x  \\
    \hat{a}_+\hat{a}_-\psi_n = n\psi_n,\qquad \hat{a}_-\hat{a}_+\psi_n = (n+1)\psi_n
\end{dcases} \\ \Downarrow \\ \bigstar\quad \psi_n = \frac{1}{\sqrt{n!}}(\hat{a}_+)^n\psi_0(x)$$


##### 2.3.2 Analytic Method

$$
 \frac{d^2\psi}{d\xi^2}=(\xi^2-K)\psi \qquad\xi\equiv\sqrt{\frac{m\omega}{\hbar}}x\quad K\equiv\frac{2E}{\hbar\omega}
 $$

To begin with at very large $\xi$

$$
 \frac{d^2\psi}{d\xi^2}\approx\xi^2\psi\qquad \underrightarrow{|x|\rightarrow\infty} \qquad \psi(\xi)=h(\xi)e^{-\xi^2/2}  
$$

$$\qquad \underrightarrow{\qquad\frac{d\psi}{d\xi},\frac{d^2\psi}{d\xi^2}\qquad} \qquad
\frac{d^2h}{d\xi^2}-2\xi\frac{dh}{d\xi}+(K-1)h=0 \\
$$ 

In the form of *power serires* in $\xi$ $$
h(\xi) = \sum_{j=0}^\infty a_j\xi^j \quad \underrightarrow{\quad\frac{dh}{d\xi}\,,\,\frac{d^2h}{d\xi^2}\quad}  \\ \sum_{j=0}^\infty[(j+1)(j+2)a_{j+2}-2ja_j+(K-1)a_j]\xi^j  = 0  \\ \Downarrow \\
a_{j+2}=\frac{(2j+1-K)}{(jh+1)(j+2)}a_j \quad \rightarrow \quad h(\xi)=h_{\rm even}(\xi) +h_{{\rm odd}}(\xi)
$$

For physically acceptable solutions: $$
\begin{aligned}
    K=&2n+1 \Rightarrow E=(n+1/2)\hbar\omega \quad{\rm ,for}\,n=0,1,2,\dots \\ &\downarrow \\ a_{j+2}=&\frac{-2(n-j)}{(jh+1)(j+2)}a_j 
\end{aligned}
$$


Nomalized stationary state
$$
\bigstar \qquad \psi_n(x) = \left(\frac{m\omega}{\pi\hbar}\right)^{1/4}\frac{1}{\sqrt{2^nn!}}H_n(\xi)e^{-\xi^2/2} 
$$

- The first few of $H_n(\xi)$ 
  - $H_0=1$
  - $H_1=2\xi$
  - $H_2 = 4\xi^2-2$
  - $H_3 = 8\xi^3-12\xi$ 

<br>

#### 2.4 The Free Particle

> $$
V(x) = 0
$$

$$
\frac{d^2\psi}{dx^2} = -k^2\psi,\quad\text{where}\quad k\equiv\frac{\sqrt{2mE}}{\hbar} \\\downarrow\\
\Psi(x,t)=Ae^{ik \left(x-\frac{\hbar k}{2m}t\right)}  +Be^{-ik \left(x-\frac{\hbar k}{2m}t\right)}
$$

Represents a wave traveling to *right* and another going to *left*, as well write $$
\Psi_k(x,t)=Ae^{i \left(kx-\frac{\hbar k^2}{2m}t\right)}  \\ k\equiv\pm\frac{\sqrt{2mE}}{\hbar},\text{with}\begin{cases}
    k>0 \Rightarrow \text{traveling to the right}  \\
    k<0 \Rightarrow \text{traveling to the left}
\end{cases}
$$
*This wave function is not normalizable*
$$
\int_{-\infty}^{+\infty} \Psi_k^*\Psi_k{\rm d}x=|A|^2\int_{-\infty}^{+\infty} {\rm d}x=|A|^2(\infty)
$$
- **Plancherel's therem** $$
f(x) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty} F(k)e^{ikx}{\rm d}k \leftrightarrow F(k)=\frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} f(x)e^{-ikx}{\rm d}x
$$

Now *this* can be normalized $$
\Psi(x,t) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty}  \phi(k)e^{i \left(kx-\frac{\hbar k^2}{2m}t\right)} {\rm d}k \\
\begin{cases}
        \Psi(x,0) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty}  \phi(k)e^{ikx} {\rm d}k   \\
\phi(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} \Psi(x,0)e^{-ikx} {\rm d}x
\end{cases}
$$

- $v_{\text{classical}} = v_{\text{group}} = 2v_{\text{phase}}$


#### 2.5 The Delta-Function Potential


##### 2.5.1 Bound States and Scattering States

$$
\begin{dcases}
    E<V(\infty) \Rightarrow \text{bound state}  \\
    E>V(\infty) \Rightarrow \text{scattering state}
\end{dcases}
$$


##### 2.5.2 The Delta-Fuction Well

> $$
V(x) = -\alpha\delta(x)
$$

(1) bound state $E<0$

$$
\frac{d^2\psi}{dx^2}= \kappa^2\psi,\quad\text{where} \quad\kappa\equiv\frac{\sqrt{-2mE}}{\hbar} \\
\Downarrow \\
\psi(x) = \begin{dcases}
    Be^{\kappa x}, &(x<0)  \\
    Fe^{-\kappa x}, &(x>0)
\end{dcases}
$$

- boundary conditions at $x=0$:
  - $\psi$ is always continuous; $\Rightarrow F=B$
  - $d\psi/dx$ is continuous except at points where the potential is infinite.
$$ \psi(0) = B \Rightarrow \kappa = \frac{m\alpha}{\hbar^2}
$$Proof: ($\epsilon\rightarrow 0$)$$
-\frac{\hbar^2}{2m}\int^{+\epsilon}_{-\epsilon}\frac{d^2\psi}{d^2x}dx+\int_{-\epsilon}^{+\epsilon}V(x)\psi(z)dx=E\int^{+\epsilon}_{-\epsilon}\psi(x)dx=0 \\ 
\Rightarrow \Delta\left(\frac{d\psi}{dx}\right) = \frac{2m}{\hbar^2}\lim_{\epsilon\rightarrow0}\int_{-\epsilon}^{+\epsilon}-\alpha\delta(x)\psi(z)dx=-\frac{2m\alpha}{\hbar^2}\psi(0)  \\ 
\begin{dcases}
    d\psi/dx|_+ = -B\kappa \\
    d\psi/dx|_- = +B\kappa
\end{dcases} \qquad\Rightarrow\qquad \Delta\left(\frac{d\psi}{dx}\right) =-2B\kappa 
$$

Norminized $\rightarrow B=\sqrt{\kappa}$
$$
\psi(x) = \frac{\sqrt{m\alpha}}{\hbar}e^{-m\alpha|x|/\hbar^2};\qquad E=-\frac{m\alpha^2}{2\hbar^2}
$$

(2) scattering state $E>0$

$$
\frac{d^2\psi}{dx^2}= -k^2\psi,\quad\text{where} \quad k\equiv\frac{\sqrt{2mE}}{\hbar}  \\ \Downarrow  \\
\psi(x) = \begin{dcases}
    Ae^{ikx}+Be^{-ikx}, &(x<0)  \\
    Fe^{ikx}+Ge^{-ikx}, &(x>0)
\end{dcases}
$$
- Boundary conditions
  $$
F+G=A+B $$

$$\begin{cases}
    \Delta(d\psi/dx) = ik(F-G-A+B) \\
    \psi(0) = (A+B)
\end{cases}\Rightarrow$$

$$
ik(F-G-A+B) = -\frac{2m\alpha}{\hbar^2}(A+B)
$$

$$
F-G=A(1+2i\beta)-B(1-2i\beta),\qquad\text{where }\beta\equiv\frac{m\alpha}{\hbar^2k}
$$

When wave come from left:
$A$: amplitude of the incident wave
$B$: amplitude of the reflected wave
$F$: amplitude of the transmitted wave
$$
B = \frac{i\beta}{1-i\beta}A,\qquad F = \frac{1}{1-i\beta}A,\qquad G =0
$$

The *relative* probability of reflection and transmission:$$
R\equiv\frac{|B|^2}{|A|^2}=\frac{\beta^2}{1+\beta}=\frac{1}{1+(2\hbar^2E/m\alpha^2)}  \\
T\equiv\frac{|F|^2}{|A|^2}=\frac{1}{1+\beta} = \frac{1}{1+(m\alpha^2/2\hbar^2E)}
$$ 
Discussion:
- If $E>V_{\max}$, then $T=1$ and $R=0$
- If $E<V_{\max}$, then $T=0$ and $R=1$
  - if $T\neq 0$, **tunneling**

Show

$$
\delta(x) = \frac{1}{2\pi}\int^{+\infty}_{-\infty}e^{ikx}\,dk
$$

Proof
$$
F(k) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^\infty\delta(x)e^{-ikx}dx=\frac{1}{\sqrt{2\pi}} 
$$

<br>

#### 2.6 The Finite Square Well

> $$
V(x) = \begin{cases}
    -V_0 , & -a \leq x\leq a \\
    0, & |x|>a
\end{cases}
$$

(1) bound state $E<0$

$x<-a,V(x)=0$ $$
\frac{d^2\psi}{dx^2}= \kappa^2\psi,\quad\text{where} \quad\kappa\equiv\frac{\sqrt{-2mE}}{\hbar}  \\
\Downarrow \\
\psi(x) = Be^{\kappa x}
$$


$-a<x<a,V(x)=-V_0$ $$
\frac{d^2\psi}{dx^2}= -l^2\psi,\quad\text{where} \quad l\equiv\frac{\sqrt{2m(E+V_0})}{\hbar} \\
\Downarrow \\
\psi(x) = C\sin(lx)+D\cos(lx)
$$

$x>a,V(x)=0$ $$
\psi(x) = Fe^{-\kappa x}
$$


- even solutions
$$
\psi(x) = \begin{dcases}
    Fe^{-\kappa x} , &(x>a) \\
    D\cos(lx), &(0<x<a)  \\
    \psi(-x) , &(x<0) 
\end{dcases}
$$

- boundary condition at $x = a$$$
\begin{cases}
    Fe^{-\kappa a}=D\cos(la) \\
    -\kappa Fe^{-\kappa a}=-lD\sin(la)
\end{cases} \qquad\Rightarrow\qquad\kappa=l\tan(la)
$$

$$
\begin{dcases}
    z\equiv la\qquad z_0\equiv\frac{a}{\hbar}\sqrt{2mV_0} \\
    (\kappa^2+l^2)=2mV_0/\hbar^2
\end{dcases}
\qquad \Rightarrow  \qquad
\tan z= \sqrt{(z_0/z)^2-1}
$$

Discussion:

- Wide, deep well
$$z_0\rightarrow\infty\qquad\Rightarrow z_n=n\pi/2\qquad\Rightarrow$$

$$E_n+V_0\approx\frac{n^2\pi^2\hbar^2}{2m(2a)^2}\qquad(n=1,3,5,\cdots)$$
- Shallow, narrow well
    - for $z_0<\pi/2$, only one remains

(2) scattering state $E>0$

When wave come from left

$$
\psi(x) = \begin{cases}
    Ae^{ikx}+B^{-ikx},  \qquad&x<-a \\
    C\sin(lx) + D\cos(lx)    &-a<x<a \\
    Fe^{ikx} & x>a
\end{cases}
$$

Boundary conditions
$$
\begin{aligned}
    Ae^{-ika}+B^{ika} = -C\sin(la) + D\cos(la)  \\ 
    ik[Ae^{-ika}-B^{ika}] = l[C\cos(la) + D\sin(la)]  \\ 
    C\sin(la) + D\cos(la) + Fe^{ika} \\
    l[C\cos(la) - D\sin(la)] = ikFe^{ika}
\end{aligned}\qquad\Rightarrow
$$

Eliminate
$$
\begin{aligned}
    B = i\frac{\sin(2la)}{2kl}(l^2 - k^2)F \\
    F = \frac{e^{-2ika}A}{\cos(2la)-i\frac{(k^2+l^2)}{2kl}\sin(2la)}
\end{aligned} \qquad\Rightarrow
$$

Transmission coefficient
$$
T^{-1} = 1+\frac{V_0^2}{4E(E+V_0)}\sin^2\left(\frac{2a}{\hbar}\sqrt{2m(E+V_0)}\right)
$$

when $T=1$
$$
\frac{2a}{\hbar}\sqrt{2m(E+V_0)} = n\pi \qquad\Rightarrow E_n+V_0 = \frac{n^2\pi^2\hbar^2}{2m(2a)^2}
$$


---







