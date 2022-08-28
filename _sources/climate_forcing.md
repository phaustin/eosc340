---
jupytext:
  cell_metadata_filter: all
  formats: ipynb,md:myst
  notebook_metadata_filter: all,-language_info,-toc,-latex_envs
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

# Day 19: Climate timescales for forcing without feedback

## Review

* In the [Day 9 reading](https://canvas.ubc.ca/courses/84061/modules/564563) we used the radiative forcing equation:

$$
\Delta F=\left(3.8{\rm W\; m}^{-2} \right)\frac{ln\left(new\; pCO_{2} /orig\; pCO_{2} \right) } {ln\left(2\right)}  
$$

to relate the $CO_2$ concentration to the radiative forcing.  

* On [Day 15](https://canvas.ubc.ca/courses/84061/modules/564569) and in the [climate sensitivity definitions](https://phaustin.github.io/eosc340/sensitivity_definitions.html) we linked a forcing $\Delta F$ from $CO_2$ or orbital changes to the long-term equilibrum temperature change $\Delta T$:

$$
\Delta T = \lambda \Delta F
$$

The next step is to understand how $\Delta T$ will change with time, which means that we need
to be able to write and solve a stock and flow equation for the energy of the ocean and atmosphere
as they are pushed by the greenhouse gas forcing $\Delta F$.  Here's an example from the textbook: Dessler (3rd edtion) Figure 6.3:


<img src="./media/dessler_6_3.png" width="80%">

As the figure shows -- on this planet $\Delta T$ first changes rapidily over about 25 years as the upper 100-200 meters of the ocean warms under the new forcing $\Delta F$ and then much more slowly as the lower 1 km
of the ocean is heated.  How is Dessler doing this calculation?

+++ {"answer": " ", "ctype": "question", "quesnum": 7}

## Stock and flow without feedback


### Temperature change in the atmosphere

On [Day 10](https://canvas.ubc.ca/courses/84061/files/19316822?wrap=1) we defined the heat capacity for
dry air $c_p=1004\ J/kg$ which links the change in energy to the change in temperature.
We can use this to find the stock of energy in the atmosphere: if we know the air density $\rho_{air}$, 
then the energy in a thin layer of thickness 
$\Delta z$ and temperature $T$ is going to be:

$$
E_{layer} = \rho_{air} c_p T \Delta z
$$

and the energy of the entire atmosphere is the integral of all these layers:

$$
E_{atmos} = \int_0^\infty \rho_{air} c_p T dz
$$

In addition, if we define the average temperature $T_{avg}$ then we can write:


$$
E_{atmos} = c_p T_{avg} \int_0^\infty \rho_{air} dz = Mc_p T_{avg}
$$ (eq:E)

where $M\ (kg\,m^{-2}) = \int_0^\infty \rho_{air} dz$ is the mass of air in a column.  You've seen this
before as Equation (4) on page 3 of [assignment 3](https://canvas.ubc.ca/courses/84061/files/20085263?wrap=1).
Using that same approach to get the value of $M$ between a surface pressure of 1000 hPa and the top
of the atmosphere where the pressure = 0 gives a values for $M$ of about 10,000 $kg\,m^{-2}$.  $M$ is a constant,
because mass is conserved in the atmosphere, and $c_p$ is also constant.  

If we ignore feedback, then we can write a simple equation for how the stock of energy in the atmosphere
responds to a radiative forcing $\Delta F$:

$$
\frac{\Delta E}{dt} = \Delta F
$$ (eq:stockflow)

where $\Delta$ means the difference between pre-industrial times, when the inflow and outflow were in balance,
and modern times, where we have increased greenhouse gasses and thrown the system out of balance.

Using {eq}`eq:E` we can rewrite {eq}`eq:stockflow` as 

$$
c_p M_{atmos} \frac{\Delta T_{atmos}}{dt} = \Delta F
$$ (eq:stockflow2)

Since $\Delta F$ is constant, this itegrates to 

$$
\Delta T_{atmos} = \frac{\Delta F}{c_p M_{atmos}} \Delta t
$$(eq:delatmos)

+++

### Temperature change in the ocean

Since the ocean is incompressible, we can calculate $M_{ocean}$ by just multiplying the density of seawater
$\rho_w$ by the depth of the ocean layer $D$: 

$$
M_{ocean} = \rho_w D
$$
where $\rho_w = 1030\ kg\,m^{-3}$ for seawater and $D$ is in meters.  Following the same approach that
gave us {eq}`eq:delatmos` gives:

$$
\Delta T_{ocean} = \frac{\Delta F}{c_w M_{ocean}} \Delta t
$$ (eq:delocean)

Note that since $c_w \approx 4000\ J\,kg^{-1}\,K^{-1}$ and seawater is 1000 times denser than air, the average temperature
of even a thin ocean layer changes much more slowly than the atmosphere given the same heating. This is shown
in the Figure 2 -- the ocean is storing almost all the extra energy that has accumulated since 1963.

+++ {"answer": " ", "ctype": "question", "quesnum": 7}

<img src="./media/image7.png" width="60%" >

Figure 2: Changes in the Earth's heat content since 1963.
(skepticalscience.com)

+++

### Melting an ice sheet

How much energy does it take to melt the  1 km of ice that used to cover the Pacific NW?  We already know from'
day 10 that
to change a kg of liquid water into a kg of water vapor takes $l_v$ = 2.5 $\times\ 10^{6}$ J/kg, the latent heat
of vaporization.  Changing 1 kg of ice into 1 kg of liquid takes substantially less energy: the latent
heat of melting for water is $l_{melting}$ = 0.334 $\times\ 10^{6}$ J/kg.  Ice is also less dense than liquid water: $\rho_{ice}$ = 917 $kg\,m^{-3}$, and as with the ocean we don't have to worry about compression, so $M_{ice} = \rho_{ice} D$, where D is the depth of the ice sheet.  That means that if we heat the ice sheet
by flux $\Delta F$ and ask how long it takes to get the energy to turn all of the ice into water, that
$\Delta t$ is given by:

$$
\Delta E_{ice} = M_{ice} l_{melting} = \Delta F \Delta t
$$

+++ {"answer": " ", "ctype": "question", "quesnum": 7}

## Example problem

How long does it take a net forcing of 1
$W\,m^{-2}$ to raise the average temperature of the top 150 m of the
ocean by 1 degree?

$$
\begin{align}
\Delta t = \frac{\rho_{w} c_{w} D \Delta T_{final}}{\Delta F}
\end{align}
$$


Put in some numbers: if $\rho_w$=1030 $kg\,m^{-3}$,
$c_w$=4000 $J\,kg^{-1}\,K^{-1}$,  
D=150 m, $\Delta T_{final}$=1 K, ∆F=1 $W\,m^{-2}$ then I get:

$t_{final}$=618 million seconds, or about 20 years to warm the top of the ocean by 1 degree.




## Summary

-   Climate forcing is the net change in the radiative flux entering and
    leaving the top of the Earth's atmosphere due to processes which are independent
    from a change in the Earth's mean temperature.
    
-   Solving the stock and flow equation without feedback for air, water and ice give
    very different timescales for the response to greenhouse warming.

-   The density and large heat capacity of liquid water make the ocean
    an enormous reservoir for energy that is being added to the system
    by global warming. Most of that energy is being absorbed by the top
    150 meters of the ocean.
