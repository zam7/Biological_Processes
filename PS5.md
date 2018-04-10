

```python
from aide_design.play import*

P = 16000 * u.mg/(u.m**2 * u.day) # capacity factor
alpha = 75 * 1/u.m # specific surface area
Q = 8 * 10**6 * u.L/u.day # flow rate
r = 2.0 # recycle ratio
HL = 21600 * u.L/(u.m**2 * u.day)  # hydraulic loading
S0 = 250 * u.mg/u.L
Se = 30 * u.mg/u.L

A = Q*(1+r)/HL
print(A)

exponent = Q.to(u.m**3/u.day)*(1+r)/A
print(exponent)
Kg = (50 + 1000 * 10**(-0.000055*(Q*(1+r)/A).magnitude))*(u.mg/u.L)
print(Kg)

H = ((Kg * np.log((S0+r*Se)/(Se*(1+r))))+(((S0-Se)/(1+r))))*(Q*(1+r))/(P*alpha*A)
print(H)

SL = (Q*S0)/(A*H)
print(SL)

```

$$ HL = \frac{Q+Q_r}{A} $$
$$ A = \frac{Q(1+r)}{HL} $$

$$ SL = \frac{QS_0}{AH} $$

$$ K_g ln(\frac{S_0 + rS_e}{S_e(1+r)}) + \frac{S_0-S_e}{1+r} = \frac{P\alpha AH}{Q(1+r)} $$

$$ H = \frac{Q(1+r)}{P\alpha A}[K_g ln(\frac{S_0 + rS_e}{S_e(1+r)}) + \frac{S_0-S_e}{1+r}] $$
