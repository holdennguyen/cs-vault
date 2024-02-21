## POST /v4/file
***Timestamp**: 2/13/2024 5:56:00 PM - 2/14/2024 7:40:00 AM (2/14/2024 0:56:30 AM - 2/14/2024 2:05:00 PM)*
***Total request:** 39,705 hits*

- ### Statuscode 429: 35,108 hits (~88%)
	- Analysis: The spike of re
	  Total request was spike ![[Pasted image 20240220134247.png]]
	  Failed request with status code 429 follow up the spike and gone ![[Pasted image 20240220134759.png]]
	- **Rootcause**: Exceed apikey limit
	- **Detail**:
		- What is the apikey limit?
			- Which apikey are they using?
			- Number of request by apikey.
		- What is the nginx proxy limit?

- ### Statuscode 499: 298 (~0.7%)
	- **Rootcause**: 

## GET request status code 404

- Timestamp: 