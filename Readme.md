# Power Purchase Agreement (PPA) Cost Analysis Tool

This tool evaluates the financial performance of a PPA for solar photovoltaic systems. It was created by City of San Diego staff to monitor the financial performance of PPAs within their portfolio and to also model future PPA costs against current commercial utility power.

## Getting Started
Link to the [PPA Cost Analysis Tool](https://bryanolson.github.io/PPACalculator/)

## Getting Started

These instructions will allow you to run the calculator on the web. 

### Prerequisites

In order to run a calculation, you will need a few things:

* 15-Minute Interval Utility Data 
* 15-Minute Interval Solar Production Data (Real or Simulated)

## Assumptions

* Non-residential customer with peak annual load less than or equal to 2MW
* Effective Tariffs: Schedule DG-R (Grandfathered) 
	* [Schedule DG-R](http://regarchive.sdge.com/tm2/pdf/ELEC_ELEC-SCHEDS_DG-R.pdf)
	* [Schedule EECC-CPP-D](http://regarchive.sdge.com/tm2/pdf/ELEC_ELEC-SCHEDS_EECC-CPP-D.pdf)

## Running the tests

The tool will allow you to specify any time period, as long as the interval data includes those dates. 

If the tool is being used to track an existing PPA with real consumption and production data, it is recommended that a single month is analyzed at a time to be compared against utility billing information for that time period.

Currently, the calculator takes approximately 1 minute to produce the final results. 


## Calculator Inputs

A screenshot of the tool is provided below, followed by a description of each input.

![enter image description here](https://github.com/bryanolson/PPACalculator/blob/master/PPA_Image.png?raw=true)


### Start Date, End Date 

* Describes the date range to be analyzed

### Holiday

* If a holiday is within billing period, enter the date of the holiday in MM/DD/YYYY format. In the assumed tariff, a holiday is calculated with the entirety of the day billed in off-peak time-of-use .

### Load Profile

* 15-Minute load data is required. The format of the load data is shown in the screenshot below. The time period of the load profile is irrelevant, as long as the requested Start Date and End Date have data available. This data is currently assumed to be net-energy metered.

### Solar Production
* 15-Minute load data is required. The format of the load data is shown in the screenshot below. The time period of the load profile is irrelevant, as long as the requested Start Date and End Date have data available.

### Meter ID
* The Load Profile requires a Meter ID. See screenshot above for an example.

### PPA Rate
* Enter the PPA Rate, in $/kWh, to be used in the calculation. All current City of San Diego PPAs do not have an escalator, and therefore it is assumed that there is no escalator in the calculation.
### Utility Rate Code
* Select an applicable Utility Rate Code from the list. Currently only one rate code is supported, see Assumptions below for more information.

	
## Outputs
A screenshot of the output table is provided below, followed by a description of each output.
![enter image description here](https://github.com/bryanolson/PPACalculator/blob/master/PPA_table.png?raw=true)
### Solar Electricity Produced (kWh)
* Aggregated electricity produced by solar system in provided date range, in kWh. 
### Utility Electricity Imported (kWh)
* Aggregated electricity consumed from electric grid in provided date range, in kWh.
### Excess Solar (kWh)
* Aggregated electricity produced by solar system in provided date range, in kWh. This information is used to calculate the Net-Energy-Metered (Nem Solar Credit ($)) described below.
### Maximum Demand (kW)
* Highest demand (in kW) for any 15-minute period contained within the provided Load Profile.
### Electricity Cost ($)
* Total cost determined from applying the time-of-use costs described in the chosen tariff to the utility only load profile. 
### Demand Cost ($)
* Total demand cost determined by calculating and combining both the on-peak demand and maximum demand for the provided date range. 
### PPA Cost ($)
* Aggregated electricity produced by solar system multiplied with the PPA Rate input.
### NEM Solar Credit ($)
* Applied generation credit calculated by applying time-of-use tariff schedule against exported electricity produced by the solar system.
### Total Bill For Month ($)
* Combined Electricity Cost, Demand Cost, NEM Solar Credit and PPA Cost described above.

A screenshot of the output graph is provided below, followed by a brief description. 

![enter image description here](https://github.com/bryanolson/PPACalculator/blob/master/PPA_graph.png?raw=true)

## Authors

* **Hannah Peterson** 
* **Bryan Olson**


## Acknowledgments

* Hat tip to anyone who contributed
* Inspiration
* etc
