$$

\begin{align*}
f(t)&=\begin{cases}
    f_1(t)&a_1<t<a_2\\
    f_2(t)&a_2<t<a_3\\
    \vdots\\
    f_{m-1}(t)&a_{m-1}<t<a_m\\
    f_m(t)&a_m<t<a_{m+1}\\
\end{cases}
&\implies&

\begin{array}{l r}
&f_1(t)\cdot u(t - a_1)u(-t + a_2)\\
&f_2(t)\cdot u(t - a_2)u(-t + a_3)\\
&\vdots\phantom{0000}\\
&f_{m-1}(t)\cdot u(t - a_{m-1})u(-t + a_m)\\
+&f_m(t)\cdot u(t - a_m)u(-t + a_{m+1})\\
\hline
&f(t)\\
\end{array}
\\
\\
\\
g(t)&=\begin{cases}
    g_1(t)&b_1<t<b_2\\
    g_2(t)&b_2<t<b_3\\
    \vdots\\
    g_{n-1}(t)&b_{n-1}<t<b_n\\
    g_n(t)&b_n<t<b_{n+1}\\
\end{cases}
&\implies&
\begin{array}{l r}
&g_1(t)\cdot u(t - b_1)u(-t + b_2)\\
&g_2(t)\cdot u(t - b_2)u(-t + b_3)\\
&\vdots\phantom{0000}\\
&g_{n-1}(t)\cdot u(t - b_{n-1})u(-t + b_m)\\
+&g_n(t)\cdot u(t - b_n)u(-t + b_{n+1})\\
\hline
&g(t)\\
\end{array}
\\
\\
\\
g(-\tau+t)&=\begin{cases}
    g_1(-\tau+t)&t - b_2<\tau<t - b_1\\
    g_2(-\tau+t)&t-b_3<\tau<t+b_2\\
    \vdots\\
    g_{n-1}(-\tau+t)&t-b_n<\tau<t+b_{n-1}\\
    g_n(-\tau+t)&t-b_{n+1}<\tau<t+b_n\\
\end{cases}

&\implies&

\begin{array}{l r}
&g_1(-\tau+t)\cdot u(\tau-t + b_2)u(-\tau+t - b_1)\\
&g_2(-\tau+t)\cdot u(\tau-t + b_3)u(-\tau+t - b_2)\\
&\vdots\phantom{0000}\\
&g_{n-1}(-\tau+t)\cdot u(\tau-t + b_m)u(-\tau+t - b_{n-1})\\
+&g_n(-\tau+t)\cdot u(\tau-t + b_{n+1})u(-\tau+t - b_n)\\
\hline
&g(-\tau+t)\\
\end{array}

\end{align*}

$$

$$
\begin{align*}
U[f_{1}](\tau, t) &= u(t - a_1)u(-t + a_2) & U[g_{1}](\tau, t) &= u(\tau-t + b_2)u(-\tau+t - b_1) & \\
U[f_{2}](\tau, t) &= u(t - a_2)u(-t + a_3) & U[g_{2}](\tau, t) &= u(\tau-t + b_3)u(-\tau+t - b_2) & \\
&\vdots&\vdots\\
U[f_m](\tau, t) &= u(t - a_m)u(-t + a_{m+1}) & U[g_n](\tau, t) &= u(\tau-t + b_{n+1})u(-\tau+t - b_n) & \\
\end{align*}

$$


$$
\begin{array}{l r}
&g_1(-\tau+t)\cdot U[g_1](\tau, t) \cdot \biggl(f_1(\tau)\cdot U[f_1](\tau, t) +\dots+f_m(\tau)\cdot U[f_m](\tau, t)\biggr)\\
&g_2(-\tau+t)\cdot U[g_2](\tau, t) \cdot \biggl(f_1(\tau)\cdot U[f_1](\tau, t) +\dots+f_m(\tau)\cdot U[f_m](\tau, t)\biggr)\\
&\vdots\phantom{0000}\\
&g_{n-1}(-\tau+t)\cdot U[g_{n-1}](\tau, t) \cdot \biggl(f_1(\tau)\cdot U[f_1](\tau, t) +\dots+f_m(\tau)\cdot U[f_m](\tau, t)\biggr)\\
+&g_n(-\tau+t)\cdot U[g_n](\tau, t) \cdot \biggl(f_1(\tau)\cdot U[f_1](\tau, t) +\dots+f_m(\tau)\cdot U[f_m](\tau, t)\biggr)\\
\hline
&f(\tau)\cdot g(-\tau+t)\\
\end{array}
$$

$$
\begin{array}{l r}
&C_1(\tau,t)\\
&C_2(\tau,t)\\
&\vdots\phantom{0000}\\
&C_{n-1}(\tau,t)\\
+&C_n(\tau,t)\\
\hline
&f(\tau)\cdot g(-\tau+t)\\
\end{array}
\implies
f(\tau)\cdot g(-\tau+t)
=
\sum_{k=1}^nC_k(\tau, t)
$$

$$

\begin{align*}

C_k(\tau, t) &= g_k(-\tau+t)\cdot U[g_k](\tau, t) \cdot \biggl(f_1(\tau)\cdot U[f_1](\tau, t) +\dots+f_m(\tau)\cdot U[f_m](\tau, t)\biggr)\\

&=g_k(-\tau+t)\cdot \biggl(f_1(\tau)\cdot U[f_1](\tau, t)\cdot U[g_k](\tau, t)  +\dots+f_m(\tau)\cdot U[f_m](\tau, t)\cdot U[g_k](\tau, t)\biggr)\\

&=g_k(-\tau+t)\sum_{h=1}^m\biggl(f_h(\tau)\cdot U[f_h](\tau, t)\cdot U[g_k](\tau, t)\biggr)

\end{align*}

$$

$$
\begin{align*}
    
    \text{Let }U[i](\tau, t) &= u(\tau - i_1)\cdot u(-\tau + i_2) & i_1 < i_2\\
    \text{Let }U[j](\tau, t) &= u(\tau - j_1)\cdot u(-\tau + j_2) & j_1 < j_2\\
\end{align*}
$$

$$
\begin{align*}
\text{Note that }u(\tau - i_1)\cdot u(\tau - j_1)&=\begin{cases}
    u(\tau - i_1) & i_1 \ge j_1 \\
    u(\tau - j_1) & j_1 > i_1  \\
\end{cases}\\
\text{And that }u(-\tau + i_2)\cdot u(-\tau + j_2)&=\begin{cases}
    u(-\tau + i_2) & i_2 \le j_2 \\
    u(-\tau + j_2)& j_2 < i_2  \\
\end{cases}\\
\text{Then }
U[i](\tau, t)\cdot U[j](\tau, t) &= \begin{cases}
    u(\tau - i_1)\cdot u(-\tau + i_2) & i_1 \ge j_1 \wedge i_2 \le j_2\\
    u(\tau - i_1)\cdot u(-\tau + j_2) & i_1 \ge j_1 \wedge j_2 < i_2 \\
    u(\tau - j_1)\cdot u(-\tau + i_2) & j_1 > i_1  \wedge i_2 \le j_2 \\
    u(\tau - j_1)\cdot u(-\tau + j_2) & j_1 > i_1  \wedge j_2 < i_2 \\
\end{cases}

\end{align*}
$$

$$

\begin{align*}
\text{Let }U^h_k(\tau, t) &= U[f_h](\tau, t)\cdot U[g_k](\tau, t)\\
&=\begin{cases}
    u(\tau - a_h)\cdot u(-\tau + a_{h+1}) & a_h \ge t-b_{k+1} \wedge a_{h+1} \le t - b_k\\
    u(\tau - a_h)\cdot u(-\tau + t - b_k) & a_h \ge t-b_{k+1} \wedge t - b_k < a_{h+1} \\
    u(\tau - t+b_{k+1})\cdot u(-\tau + a_{h+1}) & t-b_{k+1} > a_h  \wedge a_{h+1} \le t - b_k\\
    u(\tau - t+b_{k+1})\cdot u(-\tau + t - b_k) & t-b_{k+1} > a_h  \wedge t - b_k < a_{h+1} \\
\end{cases}\\\\
&=\begin{cases}
    u(\tau - a_h)\cdot u(-\tau + a_{h+1}) & a_h + b_{k+1} \ge t\wedge a_{h+1} + b_k\le t\\
    u(\tau - a_h)\cdot u(-\tau + t - b_k) & a_h + b_{k+1} \ge t\wedge a_{h+1} + b_k > t \\
    u(\tau - t+b_{k+1})\cdot u(-\tau + a_{h+1}) & a_h + b_{k+1} < t\wedge a_{h+1} + b_k\le t\\
    u(\tau - t+b_{k+1})\cdot u(-\tau + t - b_k) & a_h + b_{k+1} < t\wedge a_{h+1} + b_k > t \\
\end{cases}\\
&=\begin{cases}
    u(\tau - a_h)\cdot u(-\tau + a_{h+1}) & a_h + b_{k+1} \ge t\ge a_{h+1} + b_k\\
    u(\tau - a_h)\cdot u(-\tau + t - b_k) & a_h + b_{k+1} \ge t\wedge a_{h+1} + b_k > t \\
    u(\tau - t+b_{k+1})\cdot u(-\tau + a_{h+1}) & a_h + b_{k+1} < t\wedge a_{h+1} + b_k\le t\\
    u(\tau - t+b_{k+1})\cdot u(-\tau + t - b_k) & a_h + b_{k+1} < t < a_{h+1} + b_k \\
\end{cases}
\end{align*}

$$

$$
\text{The definition of } C_k(\tau, t) \text{ will be:}
$$
$$
C_k(\tau, t) = g_k(-\tau+t)\sum_{h=1}^m{U^h_k(\tau, t)f_h(\tau)}
$$

$$
\begin{align*}
\text{Convolution:}\\ 
F(t) &= f(t) * g(t)\\
&= \int_{-\infin}^{\infin}{f(\tau)\cdot g(-\tau+t)d\tau}\\
&=\sum_{k=1}^n\Biggr[\int_{-\infin}^{\infin}{C_k(\tau, t)d\tau}\Biggr]\\
&=\sum_{k=1}^n\Biggr[\int_{-\infin}^{\infin}{C_k(\tau, t)d\tau}\Biggr]\\
&=\sum_{k=1}^n\Biggr[\int_{-\infin}^{\infin}{\Biggr[g_k(-\tau+t)\sum_{h=1}^m{U^h_k(\tau, t)f_h(\tau)}\Biggr]d\tau}\Biggr]\\
&=\sum_{k=1}^n\Biggr[\int_{-\infin}^{\infin}{\Biggr[\sum_{h=1}^m{f_h(\tau)g_k(-\tau+t)U^h_k(\tau, t)}\Biggr]d\tau}\Biggr]\\
&=\sum_{k=1}^n\sum_{h=1}^m\int_{-\infin}^{\infin}{\Biggr[{f_h(\tau)g_k(-\tau+t)U^h_k(\tau, t)}\Biggr]d\tau}\\
\end{align*}

$$

## Integral of $U^h_k(\tau, t)$

$$
\begin{align*}
\forall\alpha,\beta.(\alpha\le&\beta).\int_{-\infin}^\infin{u(\tau-\alpha)u(-\tau+\beta)}d\tau&\tau<\alpha\text{ or }\beta<\tau\implies0\\
&=\int_{\alpha}^\beta{u(\tau-\alpha)u(-\tau+\beta)}d\tau&\alpha<\tau<\beta\implies1\\
&=\int_{\alpha}^\beta{}d\tau
\end{align*}
$$

We use the same argument to conclude that:

$$
\begin{align*}
\forall\alpha,\beta,f.(\alpha\le&\beta).\int_{-\infin}^\infin{f(\tau)u(\tau-\alpha)u(-\tau+\beta)}d\tau&\tau<\alpha\text{ or }\beta<\tau\implies0\\
&=\int_{\alpha}^\beta{f(\tau)u(\tau-\alpha)u(-\tau+\beta)}d\tau&\alpha<\tau<\beta\implies f(\tau)\\
&=\int_{\alpha}^\beta{f(\tau)}d\tau
\end{align*}
$$

We can also extend the definition to allow $\alpha$ to be larger than $\beta$:

$$
\begin{align*}
\forall\alpha,\beta&,f.\int_{-\infin}^\infin{f(\tau)u(\tau-\alpha)u(-\tau+\beta)}d\tau\\
&=\begin{cases}
    0&\beta<\alpha\\
    \int_{\alpha}^\beta{f(\tau)u(\tau-\alpha)u(-\tau+\beta)}d\tau&\alpha\le\beta\\
\end{cases}\\
&=\begin{cases}
    0&\beta<\alpha\\
    \int_{\alpha}^\beta{f(\tau)}d\tau&\alpha\le\tau\le\beta\\
\end{cases}\\

\end{align*}
$$

$U^h_k(\tau, t)$ has multiple cases:

$$
\begin{align*}
\forall f:\\
\int_{-\infin}^\infin{f(\tau)U^h_k(\tau, t)}d\tau
&=\begin{cases}
    \int_{-\infin}^\infin{f(\tau)u(\tau - a_h)\cdot u(-\tau + a_{h+1})}d\tau & a_h + b_{k+1} \ge t\ge a_{h+1} + b_k\\
    \int_{-\infin}^\infin{f(\tau)u(\tau - a_h)\cdot u(-\tau + t - b_k)}d\tau & a_h + b_{k+1} \ge t\wedge a_{h+1} + b_k > t \\
    \int_{-\infin}^\infin{f(\tau)u(\tau - t+b_{k+1})\cdot u(-\tau + a_{h+1})}d\tau & a_h + b_{k+1} < t\wedge a_{h+1} + b_k\le t\\
    \int_{-\infin}^\infin{f(\tau)u(\tau - t+b_{k+1})\cdot u(-\tau + t - b_k)}d\tau & a_h + b_{k+1} < t < a_{h+1} + b_k \\
\end{cases}\\
&=\begin{cases}
    \int_{a_h}^{a_{h+1}}{f(\tau)}d\tau & a_h + b_{k+1} \ge t\ge a_{h+1} + b_k\\
    \int_{a_h}^{t - b_k}{f(\tau)}d\tau & a_h + b_{k+1} \ge t\wedge a_{h+1} + b_k > t \\
    \int_{t-b_{k+1}}^{a_{h+1}}{f(\tau)}d\tau & a_h + b_{k+1} < t\wedge a_{h+1} + b_k\le t\\
    \int_{t-b_{k+1}}^{t - b_k}{f(\tau)}d\tau & a_h + b_{k+1} < t < a_{h+1} + b_k \\
\end{cases}\\
\end{align*}
$$


# Example 1
## $f(t)$ and $g(t)$
$$
\begin{align*}
f(t)&=\begin{cases}
    0&-\infin<t<0\\
    1&0<t<1\\
    0&1<t<\infin\\
\end{cases}
\\
g(t)&=\begin{cases}
    0&-\infin<t<0\\
    t&0<t<1\\
    0&1<t<\infin\\
\end{cases}
\\
g(-\tau+t)&=\begin{cases}
    0&t<\tau<\infin\\
    -\tau+t&t-1<\tau<t\\
    0&-\infin<\tau<t-1\\
\end{cases}

\end{align*}
$$
## Boundraries

When calculating the integral we look at every combination of $h$ and $k$ and multiply $f_h$ with $g_k$. Notice however that some values of $h$ and $k$ will yield a constant $0$, implying that the integral will be zero as well. In the following tables I have included all values of $h$ and $k$ but I will not do every $U_k^h$. For situations where boundraries including infinity look in the appendix.

$$
\begin{array}{c | c | c | c | c }
    & h = 1    & h = 2  & h = 3  & h = 4  \\\hline
a_h & -\infin  & 0      & 1      & \infin \\\hline
    & k = 1    & k = 2  & k = 3  & k = 4 \\\hline
b_k & -\infin  & 0      & 1      & \infin 
\end{array}
$$
$$
\begin{array}{c | c | c | c }
a_h + b_{k+1} & h = 1    & h = 2  & h = 3  \\\hline
k = 1         & -\infin  & 0      & 1      \\\hline
k = 2         & -\infin  & 1      & 2      \\\hline
k = 3         & \text{*} & \infin & \infin \\
\end{array}
$$
$$
\begin{array}{c | c | c | c }
a_{h+1} + b_k & h = 1   & h = 2   & h = 3    \\\hline
k = 1         & -\infin & -\infin & \text{*} \\\hline
k = 2         & 0       & 1       & \infin   \\\hline
k = 3         & 1       & 2       & \infin   \\
\end{array}
$$
$$\text{*}\infin-\infin\text{ may not be defined but these will not be used anyway}$$

### $U_2^2(\tau,t)$
These are the only values for $h$ and $k$ where the integral will give a value. 
$$
\begin{align*}
U^h_k(\tau, t)&=\begin{cases}
    u(\tau - a_h)\cdot u(-\tau + a_{h+1})       & a_h + b_{k+1} \ge t\ge    a_{h+1} + b_k\\
    u(\tau - a_h)\cdot u(-\tau + t - b_k)       & a_h + b_{k+1} \ge t\wedge a_{h+1} + b_k > t \\
    u(\tau - t+b_{k+1})\cdot u(-\tau + a_{h+1}) & a_h + b_{k+1} < t\wedge   a_{h+1} + b_k\le t\\
    u(\tau - t+b_{k+1})\cdot u(-\tau + t - b_k) & a_h + b_{k+1} < t <       a_{h+1} + b_k \\
\end{cases}\\&=\begin{cases}
    u(\tau - 0)\cdot u(-\tau + 1)       & 1 \ge t\ge    1   \\
    u(\tau - 0)\cdot u(-\tau + t - 0)   & 1 \ge t\wedge 1   > t \\
    u(\tau - t+1)\cdot u(-\tau + 1)     & 1 < t\wedge   1   \le t\\
    u(\tau - t+1)\cdot u(-\tau + t - 0) & 1 < t <       1   \\
\end{cases}\\&\text{Notice that certain ranges are redundant or can be simplified}\\&=\begin{cases}
    u(\tau - 0)\cdot u(-\tau + t - 0)   & 1 > t \\
    u(\tau - t+1)\cdot u(-\tau + 1)     & 1 \le t\\
\end{cases}\\&=\begin{cases}
    u(\tau)\cdot u(-\tau + t)           & 1 > t \\
    u(\tau - t + 1)\cdot u(-\tau + 1)   & 1 \le t\\
\end{cases}\\&\text{Since we will take the integral later we'll add the requirement that}\\&\text{bounds do not cross.}\\&=\begin{cases}
    0&t<0\\
    u(\tau)\cdot u(-\tau + t)           & 0 \le t < 1\\
    u(\tau - t + 1)\cdot u(-\tau + 1)   & 1 \le t\le 2\\
    0&2<t\\
\end{cases}\\
\end{align*}
$$
As we can see adding the restrictions on t does not change the behaviour of $U^h_k(\tau, t)$ but since the integral will need these restrictions later we might as well add them now.
## Convolution
$$
\begin{align*}
F(t)&=f(t)*g(t)\\
&=\int_{-\infin}^{\infin}{f(\tau)g(-\tau+t)}d\tau\\
&=\sum_{k=1}^n\sum_{h=1}^m\int_{-\infin}^{\infin}{\Biggr[{f_h(\tau)g_k(-\tau+t)U^h_k(\tau, t)}\Biggr]d\tau}\\
&=\int_{-\infin}^{\infin}{\Biggr[f_2(\tau)g_2(-\tau+t)U^2_2(\tau, t)\Biggr]d\tau}\\&=\begin{cases}
    \int_{-\infin}^{\infin}{\Bigr[f_2(\tau)g_2(-\tau+t)\cdot 0\Bigr]}d\tau                           &t<0\\
    \int_{-\infin}^{\infin}{\Bigr[f_2(\tau)g_2(-\tau+t)u(\tau)\cdot u(-\tau + t)\Bigr]}d\tau         & 0 \le t < 1\\
    \int_{-\infin}^{\infin}{\Bigr[f_2(\tau)g_2(-\tau+t)u(\tau - t + 1)\cdot u(-\tau + 1)\Bigr]}d\tau & 1 \le t\le 2\\
    \int_{-\infin}^{\infin}{\Bigr[f_2(\tau)g_2(-\tau+t)\cdot 0\Bigr]}d\tau                           &2<t\\
\end{cases}\\&=\begin{cases}
    0 &t<0\\
    \int_{0}^{t}{\Bigr[f_2(\tau)g_2(-\tau+t)u(\tau)\cdot u(-\tau + t)\Bigr]}d\tau             & 0 \le t < 1\\
    \int_{t - 1}^{1}{\Bigr[f_2(\tau)g_2(-\tau+t)u(\tau - t + 1)\cdot u(-\tau + 1)\Bigr]}d\tau & 1 \le t\le 2\\
    0 &2<t\\
\end{cases}\\&=\begin{cases}
    0 &t<0\\
    \int_{0}^{t}{\Bigr[f_2(\tau)g_2(-\tau+t)\Bigr]}d\tau     & 0 \le t < 1\\
    \int_{t - 1}^{1}{\Bigr[f_2(\tau)g_2(-\tau+t)\Bigr]}d\tau & 1 \le t\le 2\\
    0 &2<t\\
\end{cases}\\&=\begin{cases}
    0 &t<0\\
    \int_{0}^{t}{\Bigr[-\tau+t\Bigr]}d\tau     & 0 \le t < 1\\
    \int_{t - 1}^{1}{\Bigr[-\tau+t\Bigr]}d\tau & 1 \le t\le 2\\
    0 &2<t\\
\end{cases}\\&=\begin{cases}
    0 &t<0\\
    -\frac{1}{2}\tau^2+t\tau\Bigr|_{0}^{t}   & 0 \le t < 1\\
    -\frac{1}{2}\tau^2+t\tau\Bigr|_{t-1}^{1} & 1 \le t\le 2\\
    0 &2<t\\
\end{cases}\\&=\begin{cases}
    0 &t<0\\
    -\frac{1}{2}t^2+t^2 & 0 \le t < 1\\
    -\frac{1}{2}+t+\frac{1}{2}(t-1)^2 - t(t-1) & 1 \le t\le 2\\
    0 &2<t\\
\end{cases}\\&=\begin{cases}
    0 &t<0\\
    \frac{1}{2}t^2 & 0 \le t < 1\\
    -\frac{1}{2}t^2+t & 1 \le t\le 2\\
    0 &2<t\\
\end{cases}\\
\end{align*}
$$










# Appendix
## Infinite boundraries
With a time shift approaching infinity the function will always return a constant $1$ or $0$
$$
\begin{equation}
\begin{align*}
    &\tau\rightarrow\lim_{x\rightarrow\infin}{u(\tau-x)}  \iff \tau\rightarrow0\\
    &\tau\rightarrow\lim_{x\rightarrow\infin}{u(\tau+x)}  \iff \tau\rightarrow1\\
    &\tau\rightarrow\lim_{x\rightarrow\infin}{u(-\tau-x)} \iff \tau\rightarrow0\\
    &\tau\rightarrow\lim_{x\rightarrow\infin}{u(-\tau+x)} \iff \tau\rightarrow1\\
\end{align*}
\end{equation}
$$