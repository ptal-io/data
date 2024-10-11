# Commonly used datasets


### Temporal Signatures
* [Foursquare Popular Times by Category Name [2021]](foursquare_temporal_signatures.zip) *[password protected]*
* [Google Popular Times by Place Type Name [2021]](google_temporal_signatures.zip) *[password protected]*
* [Foursquare Average Open Hours by Category Name [2022]](foursquare_openhours2022.zip) *[password protected]*
* [Foursquare Category/Name Lookup [2021]](fs_categories.csv) 



### Tweets

* [Geotagged Tweets [Count: 24,963,638] [2020-2021]](geotagged_tweets2020-2021/)

Command to rejoin the file splits:

	cat geotagged_tweets2020-2021/geotagged_tweets2020-2021.tar.gz.part* > geotagged_tweets2020-2021/geotagged_tweets2020-2021.tar.gz
	

### Strava Activities
* [Activities, Segments, and Details in Washington, D.C. and Montreal [2023]](strava_activities) *[password protected]*

Command to rejoin the file splits:

	cat strava_activities/strava_activities2023.dump.tar.gz.enc.part* > strava_activities/strava_activities2023.dump.tar.gz.enc
	
	openssl enc -aes-256-cbc -d -in strava_activities/strava_activities2023.dump.tar.gz.enc | tar xzvf
	
### Foursquare Check-ins
* [Check-ins and nearby POI [2023]](foursquare_checkins) *[password protected]*

Command to rejoin the file splits:

	cat foursquare_checkins/foursquare_checkins.dump.tar.gz.enc.part* > foursquare_checkins/foursquare_checkins.dump.tar.gz.enc
	
	openssl enc -aes-256-cbc -d -in foursquare_checkins/foursquare_checkins.dump.tar.gz.enc | tar xzvf	

### TripAdvisor Attractions
* [Trip Advisor Attractions and Details [2020]](tripadvisor_attractions) *[password protected]*

Command to rejoin the file splits:

	cat tripadvisor_attractions/tripadvisor2020.dump.tar.gz.enc.part* > tripadvisor_attractions/tripadvisor2020.dump.tar.gz.enc
	
	openssl enc -aes-256-cbc -d -in tripadvisor_attractions/tripadvisor2020.dump.tar.gz.enc | tar xzvf	
	
### Places of Interest
---

#### Houston
* [Points of Interest from Foursquare [2022]](foursquare_POI_houston2022.zip) *[password protected]*


#### London
* [Points of Interest from Foursquare [2022]](foursquare_POI_london2022.zip) *[password protected]*


#### Los Angeles
* [Points of Interest from Foursquare [2022]](foursquare_POI_losangeles2022.zip) *[password protected]*


#### Montreal
* [Points of Interest from OpenStreetMap [2024]](mtl_poi_osm2024.zip) 
* [Points of Interest from Foursquare [2022]](foursquare_POI_montreal2022.zip) *[password protected]*


#### New York City
* [Points of Interest from Foursquare [2022]](foursquare_POI_newyorkc2022.zip) *[password protected]*

#### Seattle
* [Points of Interest from Foursquare [2022]](foursquare_POI_seattle2022.zip) *[password protected]*



#### Washington, D.C.
* [Points of Interest from Foursquare [2024]](foursquare_POI_washingtondc2024.zip) *[password protected]*



---
Code to encrypt file before splitting:

	openssl enc -aes-256-cbc -pbkdf2 -iter 100000 -e file.tar.gz > file.tar.gz.enc
