<!-- .slide: class="slide-title" data-background-color="#000000" data-background-image="../assets/background.jpg" data-background-repeat="no-repeat" data-background-opacity="0.45" data-background-position="center" -->

<div class="container">
<div class="col-large" style="text-align: left;">

ENVS258 Environmental Geophysics
<br>
Gravimetry

</div>
<div class="col-small" style="text-align: right;">

[<img src="../assets/university-of-liverpool-white.png" style="width: 35%">](https://www.liverpool.ac.uk/earth-ocean-and-ecological-sciences/)

</div>
</div>

<div class="r-stretch">

# Ground-based gravimetry

</div>

## Instructor: **[Leonardo Uieda](https://www.leouieda.com)**


<i class="fas fa-envelope fa-fw"></i> [Leonardo.Uieda@liverpool.ac.uk](mailto:Leonardo.Uieda@liverpool.ac.uk)
<span style="margin: 0 20px">|</span>
<i class="fab fa-twitter fa-fw"></i> [@leouieda](https://twitter.com/leouieda)
<span style="margin: 0 20px">|</span>
[<i class="fab fa-creative-commons"></i><i class="fab fa-creative-commons-by"></i> CC-BY 4.0 License](https://creativecommons.org/licenses/by/4.0/)

<!------->

<!--<div class="centered">-->
<!--<div>-->

<!--# Learning outcomes-->

<!--1. Explain the workings on relative gravimeters-->
<!--1.-->

<!--</div>-->
<!--</div>-->

---

<div class="container">
<div class="col-large small">

# Absolute gravimeters

Measure gravity acceleration along the vertical

High accuracy at [μGal level](http://microglacoste.com/wp-content/uploads/2018/02/FG5-X-Brochure.pdf)
(1e-8 m/s²)

Usually work by dropping a mass in a vacuum

Costly, large power consumption, long reading time, difficult to deploy in the
field (even the "portable" versions)

Progress is being made to make them more viable for field deployment (e.g., for
time-lapse measurements)

</div>
<div class="col-small tiny">

[Microg LaCoste A10 portable absolute gravimeter](http://microglacoste.com/product/a10-outdoor-absolute-gravimeter/)

<img src="../images/A10_absolute_gravity_meter.jpg" style="width: 80%;">

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: [Jeff Kennedy, USGS](https://www.usgs.gov/media/images/a10-absolute-gravity-meter)
(public domain)

</div>

---

<div class="container">
<div class="col-large small">

# Relative gravimeters

Measure a change in gravity acceleration along the vertical

High accuracy at [μGal level](http://microglacoste.com/wp-content/uploads/2019/01/CG-6-Brochure_R5.pdf)
(1e-8 m/s²)

Usually a mass and spring system

Suffers from drift, requires referencing to a base station with known gravity

Light-weight, fast reading time, low power consumption, truly portable

</div>
<div class="col-small tiny">

[Microg LaCoste CG5 relative gravimeter](http://microglacoste.com/product/cg-6-autograv-gravity-meter/)

<img src="../images/Autograv_CG5_P1150838.JPG" style="width: 90%;">

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: [Sandeep vats](https://en.wikipedia.org/wiki/File:Autograv_CG5_P1150838.JPG)
(GNU FDL)

</div>

---

# Gravity networks

<div class="container">
<div class="col-large small">

Tie relative measurements to a base station with known gravity (measured with
an absolute gravimeter)

1. Take a relative measurement at the base station
1. Measure on point 1
1. Calculate the difference
1. Add difference to known gravity

</div>
<div class="col-small tiny">

<img src="../images/gravity-network.svg" style="width: 100%;">

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: Leonardo Uieda
(CC-BY)

</div>

---

# Gravity networks

<div class="container">
<div class="col-large small">

Ideal survey would take measurements between all points

Gravity calculated through least-squares adjustment of the differences

More time-consuming so only done when high accuracy is required

Example: geodetic determination of a vertical datum (the geoid)

</div>
<div class="col-small tiny">

<img src="../images/gravity-network-full.svg" style="width: 100%;">

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: Leonardo Uieda
(CC-BY)

</div>

---

# Gravity networks

<div class="container">
<div class="col-large small">

Minimal network is a closed loop

Gravity is calculated by adding the difference in readings to known gravity at
the base station

Often used for regional geophysical surveys

Sensitive to errors since there are no redundant observations

Measure at the base station at the start and end to correct for instrumental
drift

</div>
<div class="col-small tiny">

<img src="../images/gravity-network-minimal.svg" style="width: 100%;">

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: Leonardo Uieda
(CC-BY)

</div>

---

# Drift

<div class="container">
<div class="col-large small">

Gravimeter readings drift with **time** so they reflect changes in gravity +
drift

Needs to be removed from observations

Take readings at base station twice and assume the drift is linear

Calculate drift on other points based on time of reading and remove it

`$ \text{drift}_i = \alpha \Delta t_i $`

</div>
<div class="col-small tiny">

<img src="../images/gravity-drift.svg" style="width: 100%;">

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: Leonardo Uieda
(CC-BY)

</div>

---

# Convert readings to mGal

<div class="container">
<div class="col-large small">

Some gravimeters require conversion of meter readings to mGal (1 mGal = 1e-5
m/s²)

Use a conversion table provided by manufacturer (specific to each instrument)

(reading - range) * scale_factor + mGal_value

Example: reading = 2154.23

(2154.23 - 2100) * 1.00520 + 2111.66 = 2166.17 mGal


</div>
<div class="col-small small">

|Reading range|mGal value|scale factor|
|:---|:------|:------|
|1800|1810.10|1.00518|
|1900|1910.62|1.00518|
|2000|2011.14|1.00519|
|2100|2111.66|1.00520|
|2200|2212.18|1.00521|

<div class="tiny">

Conversion table for LaCoste & Romberg Model G gravimeter. The more modern CG5
and CG6 don't require conversion (they give you the value in mGal directly).

</div>

</div>
</div>

---

# Leveling

<div class="container">
<div class="col-large small">

The gravimeter is leveled (aligned with the vertical) before taking a reading

Manually using a bubble level in older models (newer models do this
automatically)

Vertical is defined as the direction of gravity

So what we measure is the **magnitude of the gravity acceleration vector**
<br>
(this will be important in the next lesson)

</div>
<div class="col-small tiny">

<img src="../images/DetalleNivelDeBurbuja.jpg" style="width: 100%;">

Example of a bubble level used to indicate if a surface is horizontal
(perpendicular to gravity).

</div>
</div>

<div class="r-stretch bottom-right">

Image credit: [aTarom](https://commons.wikimedia.org/wiki/File:DetalleNivelDeBurbuja.jpg)
(public domain)

</div>

---

# Not covered here

Solid Earth tides:

* Sun and Moon pull on the Earth, moving the ground up and down
* Causes measurable gravity differences

High precision surveying (microgravity):

* Used to detect small changes in gravity (microGal level)
* Examples: tunnels, chambers, caves, graves, etc
* Requires extra care with drift (linear assumption is not good enough)

---

# Not covered here (continued)

Atmospheric effects:

* Changes in pressure influence readings for high precision surveys

Glacial isostatic adjustment (GIA):

* Areas with "recent" lost of glaciers (northern Canada, Scandinavia, etc) are
  rebounding upward
* Change in height creates a change in measured gravity
* Visible effect when comparing multiple surveys

---

# Summary of acquisition

1. Start at a base station with known gravity
1. Level the gravimeter
1. Take reading, time, and position (lat, lon, height)
1. Repeat for other locations
1. Finish back at the base station

---

# Summary of processing

1. Calculate the drift rate
1. Remove drift from readings
1. Convert readings to mGal
1. Calculate mGal difference with base station
1. Add known gravity to the measured differences

---

<!-- END MATTER -->
<!-- ====================================================================== -->

<!-- .slide: class="slide-license" -->

<div class="centered">
<div>

<p class="license-icons">
<i class="fab fa-creative-commons"></i><i class="fab fa-creative-commons-by"></i>
</p>

Unless otherwise noted,
the contents of this lecture are
licensed under the
<br>
[Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

</div>
</div>
