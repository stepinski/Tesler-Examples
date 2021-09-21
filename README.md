# Tesler-Examples
Example Tesler scripts showing how to use Python code to transform your [FlowH2O](https://app.flowh2o.org) data.  
&nbsp;  
&nbsp;  

### 1. Area Velocity Calculation

This is a simple function to calculate the flow in a pipe using the area-velocity method.  It takes 2 channels of input data (flow depth and velocity) as would be measured by an area-velocity meter.  The depth is first converted to flow area, based on the known diameter of the pipe.  This area is then multiplied by the velocity to calculate a time series of flow per the continuity equation Q=VA (where Q=flow, V=velocity, and A=flow area).
&nbsp;  
&nbsp;  

### 2. Pump Station Calculation

This is a simple routine to calculate the average inflow into a duplex sanitary pump station.  It takes 2 channels of input data (pump 1 and 2 status) as would be recorded by a datalogger or SCADA system.  The code detects when a suitable condition occurs to use this method (namely, the start and end of a wet well fill cycle when no pumps are running).  Knowing the volume of the operating range of the wet well and the time each fill cycle takes,  an average inflow rate for each fill cycle can be calculated and written to a time series.
&nbsp;  
&nbsp;  

### 3. Potential Evapotranspiration (PET) Calculation

This routine calculates the potential evapotranspiration (PET) at a location given a set of input data taken from the NASA SOLARMET model (min/avg/max temperature, windspeed, relative humidity, insolation incident on a horizontal surface).  Knowing other information about the chosen location (elevation and latitude), the routine calculates PET as a time series for use in various hydrologic models (such as RAVEN or SWMM).
&nbsp;  
&nbsp;  
