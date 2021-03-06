# Where the ISS at? Postman Collection Documentation
This repository has a .json(collection) file which can be executed using Postman. 
You can download Postman from the below mentioned location - 
https://www.postman.com/downloads/

Note: The collection file can also be run on the command line with Newman. 
You can follow the instructions from this location - 
https://learning.postman.com/docs/running-collections/using-newman-cli/command-line-integration-with-newman/

# How to import a collection in Postman
1. To open the Postman application, click on its icon on the taskbar. 

![image](https://user-images.githubusercontent.com/54844281/139203535-02fc2a73-46a5-4774-aeeb-f1d21683116a.png)


2. Click on the file tab and then click import.

![image](https://user-images.githubusercontent.com/54844281/139203266-79260641-3657-4b09-a012-dde7527565b7.png)

3. Choose the method you want to import an item.

![image](https://user-images.githubusercontent.com/54844281/139203281-d34c731c-4240-4e2f-888b-8f7f1e34c281.png)

4. Choose the correct item to import and press open. Postman will automatically import the item.

![image](https://user-images.githubusercontent.com/54844281/139203296-5fbf6e3b-80d5-452a-bc9f-5e27d97b13ad.png)

Note: This collection also has a 'Monitor' in place which runs the entire suite at regular intervals to check the health of the APIs(see the below image): 
![image](https://user-images.githubusercontent.com/54844281/139247318-c4b68ff1-719a-48b6-9d2d-a4ed87faadec.png)

# Issues found while using the APIs - 
1. While running the tests multiple times, I found the below intermittent issue: 
![image](https://user-images.githubusercontent.com/54844281/139203914-1b6dbf3a-5afa-43d4-a6a7-16a1583d0000.png)
2. The Health Monitor failed once during the day with the below failure - 
Failed: Verify the content of 'line1'
expected '1 25544U 98067A   21301.00322917  .00003431  00000-0  70877-4 0  9995' 
to equal '1 25544U 98067A   21300.18135819  .00002498  00000-0  53866-4 0  9997'
Failed: Verify the content of 'line2'
expected '2 25544  51.6444  45.9958 0003883 145.6466 188.4099 15.48807975309173' 
to equal '2 25544  51.6441  50.0595 0003895 145.1077 283.4074 15.48797185309057'

Note - When the tests fail in the Health Monitor, an email is shared by Postman with the details of the failures: 
![image](https://user-images.githubusercontent.com/54844281/139249613-3b13bd02-b39d-4be4-8c2d-c0e3a077f10e.png) ![image](https://user-images.githubusercontent.com/54844281/139249681-4b8e870b-4514-4d46-97dc-751890003b68.png)



# Suggestions to improve the APIs - 
1. The APIs should be load tested to understand how the performance of the application can be affected by normal and peak load. 
   Based on the results of the load test, the API servers will have to be upgraded. 
2. The /satellite API should also have an optional parameter, &units=miles, to have the response in Miles instead of Kilometers. 
