## Wake County Fire Response Time Analysis Forest 

## This project examines the efficiency of emergency response time in Wake County by anayzing fire department dispatch data. Using R, I calculated average response time, identified patterns across stations and times of day.
.



## Dataset Overview

 **Source**: **https://drive.google.com/file/d/1WxSF8QzIRFmixOvIGGDex9XXn7x4mM79/view?usp=sharing**
 **Note**: Hosted externally due to GitHubs size limit.


  
**Scope**: Over 229,000 incident records
 **Fields used**: station, dispatch_date_time, arrive_date_time, incident_type



## Libraries

- tidyverse – Data wrangling
- lubridate – Date-time parsing
- ggplot2 – Data visualization



## Analytical Steps

### 1. Data Preparation
- Parsed date-time fields with ymd_hms()
- Removed records with missing or corrupt timestamps

### 2. Response Time Calculation
- Created a new response_time column (arrival minus dispatch)
- Calculated:
 - Overall average response time
 - Response time by **station**
 - Year-over-year trends

### 3. Fire-Specific Analysis
- Filtered incidents (incident_type between 100–199) to isolate actual fires
- Compared response time for all calls vs. fire-only calls
- Identified fastest and slowest stations for fire responses

### 4. Temporal Patterns
- Analyzed call volume by **hour of day**
- Visualized when fires are most likely to occur



## Key Findings

**Avg. Response Time (All Calls)**: 
- 318.75 seconds
**Fastest Station (All Calls)**:
  - Station 13 – 223 seconds
**Slowest Station (All Calls)** :
- **Station 29 – 495.76 seconds**
**Total Incidents**:
  -  229,047
**Actual Fires**:
-  17,231
**Avg. Response Time (Fires)**:
- 310.98 seconds
**Fastest Station (Fires)**:
  - Station 3 – 232.77 seconds
**Slowest Station (Fires)**:
- Station 23 – 586.37 seconds
**Peak Hours for Fire Calls**:
  - 7PM–11PM
**Trend**:
-Response times are declining, post-2020 (improvements in infrastructure/personnel) 



## Visuals

** Line chart**: 
- Yearly average response time
** Bar chart**: 
- Number of fire calls by hour



## Insight 

Wake County Fire seems to be improving in efficiency, with declining response times offering useful information about how each station is performing. High call volume in evening hours suggests potential need for increased crew size during those windows. The faster response to actual fires compared to general incidents indicates prioritization.
