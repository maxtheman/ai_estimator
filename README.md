# ai_estimator

<!-- WARNING: THIS FILE WAS AUTOGENERATED! DO NOT EDIT! -->

This file will become your README and also the index of your
documentation.

## Install

\#AI Estimator

This code is a proof of concept intended larger project that aims to
assist with property management tasks. It is designed to help with the
estimation of materials needed for a roofing job. It takes into account
various factors such as the size and shape of the roof, the type of
materials being used, and the specific requirements of the job.

## Calculations

The code uses the OpenAI API to interact with the user and perform tasks
based on the user’s input. It can create estimates for property
renovations or repairs, retrieve property owner details from the
database, retrieve property information from the database, retrieve
building structure information from the database, and retrieve materials
templates from the database.

The code is organized into several classes and functions, each with a
specific role. For example, the
[`SupportedTrade`](https://maxtheman.github.io/ai_estimator/core.html#supportedtrade)
and
[`RequiredRoofingMaterials`](https://maxtheman.github.io/ai_estimator/core.html#requiredroofingmaterials)
classes define the types of jobs and materials that the calculator can
handle. The
[`Material`](https://maxtheman.github.io/ai_estimator/core.html#material)
class represents a specific type of material, including its name, role,
how many units are in a package, the cost per unit, and a waste factor
to account for any material that might be wasted during the job.

The
[`RoofInputMeasurements`](https://maxtheman.github.io/ai_estimator/core.html#roofinputmeasurements)
class represents the measurements of the roof, including the length and
width of the area, the total length of the roof area, and specific
measurements for different parts of the roof like ridges, valleys,
rakes, etc. The
[`RoofingSettings`](https://maxtheman.github.io/ai_estimator/core.html#roofingsettings)
class represents the assumptions for a roofing calculator, like how many
shingles are needed per square foot of roof, how many nails are needed
per square foot, etc.

The
[`MaterialTemplate`](https://maxtheman.github.io/ai_estimator/core.html#materialtemplate)
class represents a template for a specific brand of materials, including
the name of the template, a list of materials, and the roofing settings.
The
[`LineItem`](https://maxtheman.github.io/ai_estimator/core.html#lineitem)
class represents a line item in the estimate, including the material
needed, the number of packages needed, and the cost per package. The
[`MaterialList`](https://maxtheman.github.io/ai_estimator/core.html#materiallist)
class represents a list of materials needed for a roofing job, including
the trade (roofing) and a list of line items.

Finally, the
[`RoofEstimate`](https://maxtheman.github.io/ai_estimator/core.html#roofestimate)
class is the main part of the calculator. It takes in the required roles
of materials, the measurements of the roof, and the material templates.
It then validates the templates, calculates the quantity and cost of
each material, and generates an estimate of the materials needed for the
job.

\##AI Usage

Uses Langchain’s `ChatOpenAI` Agent and tool decorators to provide the
above calculations to the Agent. Examples are provided showing how the
data is supposed to flow and a hardcoded example given a single full
property.

## How to to install

1.  Clone this repo
2.  Set `OPEN_API_KEY`
3.  pip install requirements.txt
4.  Then, open in VSCode with the Jupyter extension or start jupyter
    from command line. Development was done with `nbdev`

How to use:

First,

Run this in the terminal to run on Modal: www.modal.com:

First, `modal token new` to set up your own modal account

`nbdev_export` to get the latest package exported from jupyter
`modal serve ai_estimator/server.py` to see the docal preview

`modal deploy` to set it to run on your account

See demo running at:
https://maxtheman–ai-estimator-run-server.modal.run/
