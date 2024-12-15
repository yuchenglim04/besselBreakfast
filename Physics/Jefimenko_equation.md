How to evaluate $\mathbf{E}$, $\mathbf{B}$ directly from Jefimenko's equations??? Is this line of reasoning correct? From Jerry Marion's book

```math
\begin{align*}
&\mathbf{E} (\mathbf{r}_{field} , t)\\
&= \frac{1}{4 \pi \epsilon_0} \int \left[ \frac{\rho(\mathbf{r'}, t_r)}{R^2} \widehat{\mathbf R} + \frac{\dot \rho (\mathbf{r'}, t_r)}{c R} \widehat{\mathbf R} - \frac{\mathbf{\dot J}(\mathbf{r'},t_r)}{c^2 R} \right] d\tau' \\
&= \frac{1}{4 \pi \epsilon_0} \int \left[ \frac{\rho(\mathbf{r'}, t_r)}{R^2} \widehat{\mathbf R} + \frac{\partial_t \rho(\mathbf{r}, t) |_{\mathbf{r} = \mathbf{r'}, t = t_r}}{c R(\mathbf{r}_{field}, \mathbf{r'})} \widehat{\mathbf R} - \frac{\partial_t \mathbf{J} (\mathbf r,t)|_{\mathbf{r} = \mathbf{r'}, t = t_r}}{c^2 R(\mathbf{r}_{field}, \mathbf{r'})} \right] d\tau' \\
&= \frac{1}{4 \pi \epsilon_0} \int \left[ \frac{\rho(\mathbf{r'}, t_r)}{R^2} \widehat{\mathbf R} + \frac{1}{c}\frac{\partial}{\partial t} \left( \frac{\rho(\mathbf{r}, t) }{R(\mathbf{r}_{field},\mathbf{r})} \widehat{\mathbf R} \right) \Biggm |_{\mathbf{r} = \mathbf{r'}, t = t_r} - \frac{1}{c^2}\frac{\partial}{\partial t} \left( \frac{\mathbf{J}(\mathbf{r},t)}{R(\mathrm{r}_{field}, \mathbf{r})} \right)\Biggm |_{\mathbf{r} = \mathbf{r'}, t = t_r}\right] d\tau'\\
&= \frac{1}{4 \pi \epsilon_0} \int \left[ \frac{\rho(\mathbf{r'}, t_r)}{R^2} \widehat{\mathbf R} + \frac{1}{c} \frac{\partial}{\partial t} \left( \frac{\rho(\mathbf{r'}, t_r(t,\mathbf{r'})) }{R(\mathbf{r}_{field},\mathbf{r'})} \widehat{\mathbf R} \right) - \frac{1}{c^2}\frac{\partial}{\partial t} \left( \frac{\mathbf{J}(\mathbf{r'},t_r(t,\mathbf{r'}))}{R(\mathrm{r}_{field}, \mathbf{r'})} \right)\right] d\tau'
\end{align*}
```

how to do the integral: given a $d\tau'$ at $\mathbf{r'}$, we evaluate $t_r = t - |\mathbf{r} - \mathbf{r'}|/c$, i.e. $\mathbf{r'}$ is the independent variable, $t_r$ depends on $\mathbf{r'}$.

Where the last row is due to $\frac{\partial}{\partial t} t_r(t, \mathbf{r'}) = 1$, and the t this time is that of $\mathbf{E}(\mathbf{r}_{field}, t)$.

$$\rho(\mathbf{r}, t) = q \ \delta^{3}(\mathbf{r} - \mathbf{w}(t))$$
$$\mathbf{J}(\mathbf{r}, t) = q \ \delta^{3}(\mathbf{r} - \mathbf{w}(t)) \mathbf{\dot w}(t) = \rho(\mathbf{r}, t) \mathbf{\dot w}(t)$$
$$\mathbf{R} (\mathbf{r}_{field} \ , \mathbf{r}_{charge})= \mathbf{r}_{field} \ - \mathbf{r}_{charge}$$
$$\pmb{\beta} = \mathbf{\dot w}/c$$

$$
\begin{align*}
V(\mathbf{r}, t) &= \frac{1}{4\pi\epsilon_0}\int_{\mathbb{R^3}} \frac{\rho(\mathbf{r'},t_r)}{R}d\tau'\\

&= \frac{1}{4\pi\epsilon_0}\int^{\infty}_{-\infty} \frac{q\ \delta(t_r - t + |\mathbf{r} - \mathbf{w}(t_r)|/c)}{R(\mathbf{r}, \mathbf{w}(t_r))} dt_r \\

&=\frac{1}{4\pi\epsilon_0} \frac{q}{R\ (1-\pmb{\beta}\ \cdot \mathbf{\widehat{R}})}
\end{align*}
$$

Essentially, the volume integral reduces to a path integral because the density is non-zero at some point in time only along the path. The integrand reduces further to a delta function. So we're changing variables from 3D Cartesian coordinates to a single parameter, here the retarded time.  

Before: $\mathbf{r'}$ is independent, $t_r(t,\mathbf{r'})$  
After: $t_r$ is independent, $\mathbf{r'} = \mathbf{w}(t_r)$

The point that contributes to the integral satisfies $$t_r - t + |\mathbf{r} - \mathbf{w}(t_r)|/c = 0$$

Only a single solution exists for a given $(\mathbf{r},t)$

Overall, the integrating over the delta function tacks on a factor

$$\frac{1}{K} = \frac{1}{1-\pmb{\beta} \cdot \mathbf{\widehat{R}}}$$

Similarly,

$$
\begin{align*}
&\mathbf{E} (\mathbf{r}, t) \\

&= \frac{1}{4 \pi \epsilon_0} \int \frac{\rho(\mathbf{r'}, t_r)}{R^2} \widehat{\mathbf R} d\tau'

+ \frac{1}{c} \frac{\partial}{\partial t} \int \frac{\rho(\mathbf{r'}, t_r(t,\mathbf{r'})) }{R(\mathbf{r},\mathbf{r'})} \widehat{\mathbf R} d\tau'

- \frac{1}{c^2}\frac{\partial}{\partial t} \int  \frac{\rho(\mathbf{r'},t_r(t,\mathbf{r'})) \mathbf{\dot w}(t_r(t, \mathbf{r'}))}{R(\mathrm{r}, \mathbf{r'})}  d\tau'\\


&= \frac{1}{4 \pi \epsilon_0} \int^{\infty}_{-\infty} \frac{q\ \delta(t_r - t + |\mathbf{r} - \mathbf{w}(t_r)|/c)}{R(\mathbf{r}, \mathbf{w}(t_r))^2} \widehat{\mathbf R} dt_r

+ \frac{1}{c} \frac{\partial}{\partial t} \int^{\infty}_{-\infty} \frac{q\ \delta(t_r - t + |\mathbf{r} - \mathbf{w}(t_r)|/c)}{R(\mathbf{r}, \mathbf{w}(t_r))} \widehat{\mathbf R} dt_r

- \frac{1}{c^2}\frac{\partial}{\partial t} \int^{\infty}_{-\infty}  \frac{q\ \delta(t_r - t + |\mathbf{r} - \mathbf{w}(t_r)|/c) \mathbf{\dot w}(t_r)}{R(\mathbf{r}, \mathbf{w}(t_r))}  dt_r
\end{align*}
$$

$$\mathbf{E} (\mathbf{r}, t) = \frac{q}{4\pi\epsilon_0} \left( \frac{\mathbf{\widehat{R}}}{KR^2} + \frac{1}{c} \frac{\partial}{\partial t}  \frac{\mathbf{\widehat{R}}}{KR} - \frac{1}{c} \frac{\partial}{\partial t} \frac{\pmb{\beta}}{KR}\right)$$


Do all these make sense? 
________________________________________________________

$$\mathbf{B}(\mathbf{r}, t) = \frac{\mu_0}{4 \pi} \int \left[ \frac{\mathbf{J}(\mathbf{r'},t)}{R^2} + \frac{\mathbf{\dot J} (\mathbf {r'}, t)}{cR} \right] \times \widehat{\mathbf{R}} d\tau'$$
