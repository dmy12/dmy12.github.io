
**Bounding Bermudans** _Thomas Roos_
___

#### Preliminaries

A `Bermudan swaption` gives the holder the right to enter into a fixed versus floating swap at a set of future exercise dates. 

A `standard Bermudan swaption`, is characterised by the fact that it is exercisable into a swap whose notional (and fixed rate) is the same for all coupons.

`Accreting Bermudans` are exercisable into swaps whose notionals increase coupon by coupon, while `amortising Bermudans` are exercisable into swaps whose notionals decrease for each coupon. 

Economically, accreting Bermudans arise from the issuing of callable zero-coupon bonds, with the notional accreting at (or close to) the fixed rate of the bond. Amortising Bermudans can be used, for example, to hedge the prepayment risk on a loan, with the amortising notionals representing the loan repayment schedule.

The ASwap can be decomposed into a portfolio of co-initial standard swaps:
$$
V^a(t)=\sum_{k=1}^n -\delta N_kV(t;0,k)
$$
as well as into a portfolio of co-terminal standard swaps:
$$
V^a(t)=\sum_{k=1}^n \delta N_kV(t;k,n)
$$
where $\delta N_k \equiv N_k - N_{k-1}$, with $N_{-1}=N_n \equiv 0$, $V(t;i,j)$ be the value of a unit notional vanilla swap spanning $T_i$ to $T_j$, with $B(t;i,j)$ being the value of the corresponding standard Bermudan swaption.

#### Model-independent bounds

Upper bounds: amortisers.
$$
B^{amo}(t) \leq \sum_{k=1}^{n-1} | \delta N_k| B(t;0,k)+N_{n-1} B(t;0,n)
$$

Upper bounds: accreters:
$$
B^{acc}(t) \leq N_0 B(t;0,n)+\sum_{k=1}^{n-1} | \delta N_k| B(t;k,n)
$$

Lower bounds: amortisers.
$$
B^{amo}(t)\geq N_0 B(t;0,n)-\sum_{k=1}^{n-1} | \delta N_k| B(t;k,n)
$$

Lower bounds: accreters.
$$
B^{acc}(t)\geq N_{n-1}B(t;0,n)- \sum_{k=1}^{n-1} | \delta N_k| B(t;0,k)
$$

_Remarks: the conclusion is simple and the method is easy to operate. Surprisingly, the lower bound and upper bound are quite tight in practice._

#### Synthetic Accreting Vols

$$
w_k=-\delta N_k A(T_0;T_0,T_k)/A^a(T_0)
$$

$$
\sigma^a= \sqrt{\sum_{j=1}^n \sum_{k=1}^n w_j w_k \rho_{jk}\sigma_j \sigma_k}
$$

Let $\hat{\sigma_j} = w_j \sigma_j$, $z_j = |\frac{w_j \sigma_j}{w_n \sigma_n}|$, then for accreter, 

$$
(\sigma^a)^2 = (\hat{\sigma_n})^2 (1-2\sum_{j=1}^{n-1} z_j \rho_{jn}+\sum_{j=1}^{n-1} \sum_{k=1}^{n-1} z_j z_k \rho_{jk})
$$
i.e.,
$$
(\sigma^a)^2 = (\hat{\sigma_n})^2 ((1-\sum_{j=1}^{n-1} z_j \rho_{jn})^2+\sum_{j=1}^{n-1} \sum_{k=1}^{n-1} z_j z_k (\rho_{jk}-\rho_{jn}\rho_{kn}))
$$
Assume $$1-\sum_{j=1}^{n-1} z_j \leq 0$$ and $$\rho_{jk} \geq min(\rho_{jn},\rho_{kn}) \geq 0$$
we can obtain a lower bound for $\sigma^a$, which is the case when all correlations equal to $1$.

Note that 
$$
\sum_{j=1}^{n-1} z_j=\dfrac{\sum_{j=1}^{n-1} (N_j-N_{j-1})A_j\sigma_j}{N_{n-1}A_n \sigma_n}
$$
the condition $1-\sum_{j=1}^{n-1} z_j \leq 0$ holds for most of the cases. 

Moreover, if $\sigma$ is constant and $\rho_{jk}=1, \forall j,k$, we have $\sigma^a = \sigma_n$. 




