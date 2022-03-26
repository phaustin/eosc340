# Day 20: Stock and flow with multiple feedbacks

**To review**: **Climate feedbacks** are changes to the net radiative flux into and out of the *top
of the Earth's atmosphere* in response to changes in the Earth's temperature. They can be included
in the earth's energy budget equation in this form:

$$
\frac{d\Delta E}{dt} =\Delta F+\Delta R=\Delta F+f\Delta T 
$$ (eq:stock1)

Here, $\Delta E$ is the change in the column energy from a reference equilibrium value, the climate
forcing $\Delta{F}$ in $W\,m{-2}$ is a change in the net radiative flux into the top of the Earth's
atmosphere (positive downward) that is *independent of temperature*, $\Delta$R is the planet's
response to the forcing, which can also be written in terms of the climate feedback $f\,\Delta T$ as
a change in the TOA radiative flux that occurs as a result of a change in the Earth's temperature .
The **climate feedback factor** $f$ has units of $W\,m^{-2}\,K^{-1}$ and is the negative inverse of
the climate sensitivity (i.e. $f=-1/\lambda$).  If $f$ is positive, then the climate feedback is
amplifying, and if f is negative then the climate feedback is stabilizing. For the climate to be
stable, $f$ must be negative; otherwise, a rise/drop in temperature would feed back into a positive/negative growth rate for and
drive the Earth to a completely new equilibrium.  However, the total climate feedback factor $f$
characterizes several different feedback processes, some of which are amplifying, and some of which
are stabilizing.

## Major Climate feedbacks

In addition to the Planck feedback, there are many feedbacks that operate in the Earth's climate
system, on many different time scales.  However, over the time scale of a human lifetime ($\sim$80
years) there are five main feedback processes that affect the climate.

### Water Vapor

Water vapour feedback arises because liquid water emits more vapor as it warms.  As the
temperature of the climate system increases, the maximum amount of water the atmosphere can hold
also increases.  Since most of the Earth surface is covered in ocean, this warming results in more
evaporation and increases the amount of water vapour in the Earth's atmosphere.  Since water vapour
is a powerful greenhouse gas, this increase in water vapour reduces the amount of long-wave flux
radiated from the atmosphere to space, causing the temperature to increase even more.  This makes
water vapour feedback an amplifying feedback process.  It is positive because it acts to decrease
the negative (upward) outgoing longwave radiation (OLW).

### Lapse rate


The strength of the greenhouse effect does not only depend on the amount of greenhouse gas in the
atmosphere, but also on the atmospheric lapse rate=dT/dz.  If the lapse rate were zero, so that the
top of the atmosphere were the same temperature as the bottom of the atmosphere, the top of the
atmosphere would radiate energy to space at the same rate it absorbs energy from below and there
would be no greenhouse effect.  As the lapse rate gets more negative, the top of the atmosphere
becomes colder relative to the surface, and the greenhouse effect becomes stronger.

Exactly how the lapse rate changes as the Earth's temperature changes is not obvious because it
depends on many processes, such as the strength of convection and how quickly atmospheric water
vapour declines with height.  However, simulations done using climate models indicate that as the
Earth's temperature rises, the top of the troposphere tends to warm faster than the surface, making
the lapse rate more positive.  If the lapse rate more positive, then the top-bottom temperature
contrast and the greenhouse effect are reduced and more outgoing long-wave radiation escapes from
the top of the atmosphere.  This makes the lapse rate feedback a stabilising feedback process, is
negative because it increases OLW.

### Ice-albedo


Ice and snow generally reflect short-wave radiation much better than rock, dirt, or water.  Snow has
an albedo of about $\alpha$ = 0.8-0.9 and ice has a slightly lower albedo between $\alpha$ =
0.5-0.7, while the ocean's albedo is around $\alpha$ = 0.06 and land is between $\alpha$ = 0.1-0.3.
As the Earth's temperature increases the ice and snow on mountains and near the poles begins to
melt, reducing the Earth's albedo and causing more short-wave radiation to be absorbed by the
surface, increasing the temperature further.  This process is called the ice-albedo feedback, and it
is an amplifying feedback process. It has a positive sign because it increases the net positive
downward shortwave.

### Clouds

The cloud feedback effect depends on several processes.  As we discussed in the Day 9 notes, low
clouds tend to reflect more short-wave radiation, cooling the Earth, while high clouds allow short
wave through but trap outgoing long-wave radiation, warming the Earth.  As the temperature of the
Earth changes, the amount of high and low clouds will change, altering how much radiation clouds
trap and reflect.  In addition, changes in the water vapour content of the atmosphere will alter the
average size of the water droplets in the clouds, which will affect their albedo and emissivity.
Finally, changes in the atmospheric temperature will affect whether the clouds are made of water
droplets or ice crystals, which will alter their albedo and emissivity as well.

The many ways in which clouds could change as the temperature changes makes the cloud feedback
effect the most uncertain and least understood of all the climate feedbacks.  However, it appears
that as the temperature of the Earth increases, the amount of low clouds decreases and the amount
of high clouds increases, warming the climate further and making the cloud feedback an amplifying
feedback process.


## Climate Sensitivity and Feedbacks

Given this list, how can we learn more about each of these feedbacks, and how they contribute
to the total feedback $f$ and the climate sensitivity
$\lambda = -1/f$?

Repeating equation {eq}`eq:stock1`
 
$$ 
\frac{d\Delta E}{dt} =\Delta F+f\Delta T
$$ (eq:stock2)

Where again, $E$ is the energy stored in the climate system in $J\,m^{-2}$, $\Delta F$ is
the climate forcing in $W\,m^{-2}$, $\Delta T$ is the average temperature change of the
climate (usually, but not always, taken to be the surface temperature), and $f$ is the
climate feedback factor in $W\, m^{-2} K^{-1}$.

Fortunately, to a good approximation the total feedback can be split into 
individual components:
 
 $$
\frac{d\Delta E}{dt} =\Delta F+f_{PL} \Delta T+f_{WV} \Delta T+f_{A} \Delta T+f_{LR} \Delta T+f_{C} \Delta T 
$$

Here, $f_{PL}$ is the feedback factor due to the Planck long-wave radiation feedback, $f_{WV}$ ik
that due to the water vapour feedback, $f_{A}$ is that due to the ice-albedo
feedback, $f_{LR}$ is that due to the lapse rate feedback, and
$f_{c}$ is that due to the cloud feedback (all in $W\,m^{-2}\,K^{-1}$).  For
simplicity, we can factor the temperature change $\Delta T$ out of each feedback term and
write 

$$
\frac{d\Delta E}{dt} =\Delta F+\left(\sum f_{i}  \right)\Delta T 
$$ (eq:stock3)

Since at equilibrium $d\Delta E/dt$ = 0, we can write

$$
\Delta F=-\left(\sum f_{i}  \right)\Delta T 
$$

but we already know from {eq}`eq:stock2` that in equilibrium $\Delta T = \lambda \Delta F$ and 
the feedbacks sum, so that the climate sensitivity is:

$$
\lambda =-\frac{1}{f} =-\frac{1}{\sum f_{i} }  
$$

In words, {eq}`eq:stock2` is saying that long as the individual feedbacks sum to a negative number
then there is a positive temperature change $\Delta T$ large enough to balance a positive
forcing $\Delta$F (and this also works in the opposite direction, such that a negative cooling
$\Delta$F can be offset by a negative temperature change).  However, if the feedbacks sum to a
positive number, then there is nothing that can hold back $d\Delta E/dt$ from growing indefinitely
for positive $\Delta$F.  This situation where the net feedback is amplifying is called
``runaway feedback''.


## Climate Feedback Factors


Now the question becomes how to calculate the climate feedback factors.  The climate feedback
factor is defined as the change in the top-of-atmosphere (TOA) radiative flux due to a change in the
Earth's temperature.  Therefore, we can calculate the climate feedback factor by calculating how
much the TOA heat flux changes when the temperature changes.  It also makes it simpler to show how
 the various feedback factors are calculated below.

As the surface temperature changes, various components of the climate (cloud cover, lapse rate,
water vapour, etc) will also change, producing a change in the radiation at the top of the
atmosphere we will denote as $\Delta$R. Whatever the component, we can then (using the chain rule)
calculate the feedback factor 

$$
\begin{equation}
   \label{21)} 
f_{x} =\frac{\Delta R}{\Delta T} =\left(\frac{\Delta R}{\Delta climate_{x} } \right)\left(\frac{\Delta climate_{x} }{\Delta T} \right) 
\end{equation} 
$$

Where the subscript x is either clouds, water vapour, sea ice, etc. Some processes are easier to
characterize than others.  The long-wave radiation emitted by the Earth depends on temperature
directly, via $I_{\uparrow } =-\sigma T^{4} $, so we calculate the Planck feedback factor by
calculating

$$
f_{PL} =\frac{\Delta R}{\Delta T} =\frac{dI_{\uparrow } }{dT} =-4 \sigma T^{3}
$$ (eq:planck)

A more realistic calculation requires averaging 
over the whole surface of the Earth.  Doing so results in an estimate of $f_{PL}$= -
3.2 W $m^{-2}\, K^{-1}$, which is very similar to the feedback one calculates for $\epsilon$ = 1
and T = 240 K (the temperature near the top of the troposphere) using {eq}`eq:planck`
i.e $-4\sigma (240^{3}) =-3.1\; W\, m^{-2} \, K^{-1} $

 The water vapour feedback is given by
 
$$
\begin{equation}
f_{WV} =\frac{\Delta R_{WV} }{\Delta T} =\left(\frac{\Delta R}{\Delta H_{2} O} \right)\left(\frac{\Delta H_{2} O}{\Delta T} \right) 
\end{equation} 
$$
where the $H_2 O$ represents the water vapour content of the Earth's atmosphere.  The ice-albedo feedback is given by

$$
\begin{equation}
f_{A} =\frac{\Delta R_{A} }{\Delta T} =\left(\frac{\Delta R}{\Delta {\rm ice\; area}} \right)\left(\frac{\Delta {\rm ice\; area}}{\Delta T} \right) 
\end{equation} 
$$
where ``ice area'' is the amount of the Earth's surface covered in ice.  The lapse rate feedback is given by

$$
\begin{equation}
  \label{25)} 
f_{LR} =\frac{\Delta R_{LR} }{\Delta T} =\left(\frac{\Delta R}{\Delta LR} \right)\left(\frac{\Delta LR}{\Delta T} \right) 
\end{equation} 
$$
Finally, the cloud feedback is given by

$$
\begin{equation}
  \label{26)} 
f_{WV} =\frac{\Delta R_{C} }{\Delta T} =\left(\frac{\Delta R}{\Delta {\rm clouds}} \right)\left(\frac{\Delta {\rm clouds}}{\Delta T} \right) 
\end{equation} 
$$
where ``clouds'' represents changes in the amount, average height, and properties of the clouds in a cloud model and $\Delta$R${}_{c}$ represents the change in radiation at the top of the atmosphere due to the change in clouds calculated using a radiation code like Modtran.

```{figure} ./media/feedback_factors.png
---
width: 80%
name: fig:factors
---
Feedback Magnitudes, not including the Planck feedback. (IPCC AR4 2007)}
```

{numref}`fig:factors` shows estimates for WV=water vapour, C = cloud, A=Albedo, LR=lapse
rate, WV+LR=combined water vapour and lapse rate, and ALL=everything calculated using climate
models for each of the climate feedback factors, not including the Planck feedback.  Because each
model makes different approximations in order to simulate atmospheric physics, each model has
slightly different estimates of the climate feedback strengths.  The water vapour feedback has the
largest magnitude, with a feedback factor of (1.80 $\pm$ 0.18) W m${}^{-2}$ K${}^{-1}$.  The cloud
feedback C is the most uncertain feedback, with a feedback factor of (0.69 $\pm$ 0.38) W m${}^{-2}$
K${}^{-1}$.  Finally, the albedo feedback has a feedback factor of (0.26 $\pm$ 0.08) W m${}^{-2}$
K${}^{-1}$, and the lapse rate feedback has a feedback factor of (-0.84 $\pm$ 0.26) W m${}^{-2}$
K${}^{-1}$.  When the water vapour and lapse rate feedbacks are added together (WV + LR) there is
cancellation, because models with active convection have both strong negative lapse rate feedback
(because clouds reduce the temperature contrast between the upper atmosphere and the surface) and
strong positive water vapour feedback (because clouds move water vapour up to higher altitudes
where it has a larger greenhouse effect).  The best estimate of the net climate feedback factor
from these four climate feedbacks (ALL in figure 1) is approximately (1.91 $\pm$ 0.2) W m${}^{-2}$
K${}^{-1}$.  Combining this with the Planck feedback value of -3.2 W m${}^{-2}$ K${}^{-1}$ gives a
total climate feedback of $f$ = -1.29 $W\, m^{-2}\,K^{-1}$, and a climate sensitivity of
$\lambda$ = 0.78 $K/(W\,m^{-2})$.

## Dessler's feedback notation

As mentioned in the Day 20 slides, Dessler uses a somewhat older feedback notation in Section
6.3. Specifically, he does the following:

1) Writes an "initial temperature change" due to the Planck feedback as:

   $$
   \Delta T_i = - \Delta F/f_{PL}
   $$
   where $\Delta F$ = 3.8 $W\,m^{-2}$ for doubled $CO_2$.  Using $f_{PL}=-3.2\ W\,m^{-2}\,K^{-1}$ 
   gives $\Delta T_i$ = 3.8/3.2 = $2.1\ K$
  
2) Divides each of the feedbacks by the magnitude of the Planck feedback to get the "gain".  For
   example his water vapor gain of $g_{WV}$ = 0.6 is $f_{WV}/|f_{PL}|$ = $f_{WV}/3.2$, so $f_{WV}$ =
   0.6 $\times$ 3.2 = 1.9 $W\,m^{-2}\,K^{-1}$
   
With these two substitutions we've can get the Dessler form of the equilibrium climate sensitivity
from {eq}`eq:stock2`:

$$
\begin{align}
\frac{d\Delta E}{dt}=& 0 =\Delta F+f_{PL} \Delta T+f_{WV} \Delta T+f_{A} \Delta T+f_{LR} \Delta T+f_{C} \Delta T  \\
-\Delta F &= (f_{PL} +f_{WV} +f_{A} +f_{LR}+f_{C} ) \Delta T  \\
-\frac{\Delta F}{|f_{PL}|} & = \frac{(f_{PL} +f_{WV} +f_{A} +f_{LR}+f_{C} )}{|f_{PL}|}\Delta T \\
& \text{and since $f_{PL}$ is negative}: \\
- \Delta T_i & =  (-1 + (g_{WV} +g_{A} + g_{LR} + g_{c})) \Delta T \\
& \text{or rearranging} \\
\Delta T & = \frac{\Delta T_i}{(1 - (g_{WV} +g_{A} + g_{LR} + g_{c}))} \\
& \text{which is Dessler equation 6.4}
\end{align}
$$

## Summary

* Climate feedbacks are processes that depend on the temperature of the Earth and alter the
  radiative balance of the Earth.

* Feedbacks can either amplify (positive $f$) or stabilize (negative $f$) an initial perturbation

* The five major fast climate feedbacks are the Planck radiation, water vapour, 
  atmospheric lapse rate, ice-albedo and cloud feedbacks

* The  Planck feedback occurs when a temperature change alters the outgoing long-wave
  radiation emitted from the top of the atmosphere.  This is a stabilising feedback.

* Water vapour feedback occurs when a temperature change alters the atmospheric water vapour
  content, altering the strength of the greenhouse effect.  This is an amplifying feedback.

* Lapse rate feedback occurs when a temperature change alters the vertical temperature profile,
  changing the strength of the greenhouse effect.  This is a stabilising feedback.

*  Ice-albedo feedback occurs when a temperature change alters the amount of ice on Earth, changing the Earth's albedo.  This is an amplifying feedback.

*  Cloud feedback occurs when a temperature change alters the average amount of cloud cover,
  changing the amount of long wave trapped and short wave reflected by the clouds. This is an
  amplifying feedback.

* The strength of climate feedbacks determine the size of the climate sensitivity. 

* $\lambda =-\frac{1}{\sum f_{i} }$

* The strength of the climate feedbacks can be determined by calculating how much the climate
  changes when the feedback system changes and multiplying that by how much the heat flux at the
  top of the atmosphere changes when the feedback system changes.

*  $f_{x} =\frac{\Delta R}{\Delta T} =\left(\frac{\Delta R}{\Delta climate_{x} } \right)\left(\frac{\Delta climate_{x} }{\Delta T} \right)$

*  The water vapour feedback is the strongest climate feedback, and the cloud feedback is the most uncertain.

* If the net climate feedback factor ever goes above 0, the climate would enter into {runaway
  feedback}, in which temperature increases would increase the amount of heat flux into the
  climate, and the climate would change radically.  Luckily, the amount of $CO_2$ required
  for this to happen on Earth is greater than the available fossil fuel reservoir.


