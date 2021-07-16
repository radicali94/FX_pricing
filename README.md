# FX Pricing & estimation des Grecques (indicateurs de risque) - Garman-Kohlhagen 

Estimation de la volatilité implicite à l'aide de la méthode Newton-Raphson (sinon la recherche dichotomique en cas de non-convergence) pour ensuite utiliser le modèle de **Garman Kohlhagen** (dérivé du modèle **Black-Scholes généralisé**) dans le but de faire le pricing des options FX (options européennes).

---
Le modèle Garman-Kohlhagen a pour entrées:
option_type = "p" ou "c" (pour Call ou Put)
fs = prix du sous-jacent
x = strike
t = échéance
v = volatilité implicite
r = taux sans risque
q = paiement de dividendes
b = coût de portage

---
Les sorties du modèle sont:
value = prix de l'option
delta = première dérivée du prix de l'option par rapport au prix du sous-jacent
gamma = seconde dérivée du prix de l'option par rapport au prix du sous-jacent
theta = première dérivée du prix de l'option par rapport au délai d'expiration
vega = première dérivée du prix de l'option par rapport à la volatilité implicite
rho = première dérivée du prix de l'option par rapport au taux sans risque