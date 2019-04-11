# NASA-Data-Analysis
I scraped data from SpaceWeatherLive.com to get the top 50 solar flares recorded so far and compare it with NASA's available data. 

This project does the following:

 - Scrape and prepare each of the two datasets
 - Integrate the two datasets (including some Entity Resolution)
 - Exploratory Analysis
 
 
## Part 1: Data scraping and preparation

* Step 1: I scraped the HTML data from SpaceWeatherLive.com and converted it to a tibble.
* Step 2: I added a few columns (for later usage) and tidy the data using the ```dplyr``` and ```tidyr``` packages.
* Step 3: I scraped the same data from NASA and converted it to a tibble.
* Step 4: I added the same columns as above, and tidied the data.
 
### Part 2: Analysis
 
#### Is it possible to replicate the top 50 solar flare table in SpaceWeatherLive.com exactly using the data obtained from NASA? That is, if we get the top 50 solar flares from the NASA table based on their classification (e.g., X28 is the highest), can we get data for the same 50 solar flare events in the SpaceWeatherLive page? If not, why not?
 
I cannot replicate the top 50 solar flare table in SpaceWeatherLive.com exactly as they have more flare datapoints than in the NASA dataset.
My code replicates it as closely as possible and even orders it in the same manner as the SpaceWeatherLive.com data table. The only limitation is the data itself that was provided to me. Also, they SpaceWeatherLive.com use maximum_time but since the NASA dataset didn't have maximum_time, I used the cme_time to approximate the maximum_time.
