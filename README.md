# Where To Live
## This is the repository for our project.
We are working on a project that will showcase different regional areas in Finland for someone who might be interested in moving. 

## 21.9.2021
Today we began introducing ourselves on how to convert our upcoming data into SQL-format with a converter. We also downloaded MariaDB, as we want to turn the data into more readable format and also look at it in a database.
We also added Google Hybrid -map into GIS, as it gives a more refined UI on our map compared to OpenStreetMap, and it's more user-friendly while looking for a place to live. We looked for more information on our upcoming steps and are trying to figure out how to implement our data on to the map.
We also updated our project plan and returned it once again.

## 24.9.2021
Today we started looking into Python and 'Pandas', in order to import excel files (our data for the project) into python, and from there, to our map.
We downloaded Anaconda and Pandas and used some time to familiarize ourselves with these. We also tried to find some more open data that we could use and implement onto our map. Familiarizing ourselves with new platforms takes surprisingly a lot of time.





## 29.9.2021 

Today we started by checking out the possible functionality of Pandas. In its current state we tried to run the commands on the Anaconda Prompt by using "activate name_of_my_env" but quickly realized that the directory was out of place. We got an error saying that the commands were not recognized as internal or external commands by the prompt. After this we headed over to https://www.geeksforgeeks.org/set-up-virtual-environment-for-python-using-anaconda/ and started to install a new environment into Anaconda Prompt by using the command "conda create -n envname python=x.x anaconda" where we specified the name for our environment as "pandamaailma" and the version as version 3.9.

//Matias comments 

I'm currently stuck at the part after creating the environment. With the Anaconda Prompt it gets stuck after trying to use commands since they are not recognized as internal or external commands. 

//end of comments


//Matias comments

I resolved this by switching over to the Anaconda Navigator and to using Python instead of the prompt. Then after running:

"import pandas as pd"

"df = pd.read_excel (r'Path where the Excel file is stored\File name.xlsx')"
"print (df)"

I was able to get a fairly look at the piece of Excel data we are currently working with.

//end of comments

## 1.10.2021

We continued banging our head against the wall with Pandas, and decided to try directly implementing excel-files into our datamap.

//Jesse comments

Matias was pulling his hair out with excel-files that had coordinates on them as a test. I kept looking for more data on Helsinki that we could use and stumbled upon https://kartta.hel.fi/ws/geoserver/avoindata/wfs. It has almost every possible segmentation of Helsinki we could hope for ready, so we might not even need to add any coordinates on the map ourselves. I might be speaking only for myself, but I feel like now we have a lot better grasp on how to use QGIS.

//end of comments


//Matias comments 

We removed everything extra from the Excel file and we made the Excel file smaller. 

By removing the extras, we were able to get the file onto Pandas and the file looked a lot neater. 

Right now we're figuring out a method of integrating the Excel-files as they are directly onto QGIS without the need for Pandas or any other methods. 

We've tried downloading XYTools plugin onto QGIS but we figured out that the version would have to be 2.18 max. We're currently running 3.16 and would need to downgrade.

I downgraded the version to 2.18 by downloading the QGIS version independently from the internet. Unfortunately I ran into a problem with getting the Google Hybrid environment to work on the older version so I decided that we're gonna go back to using QGIS 3.16.

I then tried to get the Excel into the delimited text format and to get that onto QGIS in its entirety. It showed some dots but the dots were out of place and non-configurable. 

Jesse found out a way to get some data in WFS-format by directly inputting it onto QGIS. This worked out well and we were able to take a look at the data that was there by default. I went ahead and changed the opacity to make it more clear on the viewer. 

// end of comments 

## 8.10.2021

Some great pöhinä was made today. Jesse kept looking for more open data (and looked at licensing of our previous data just to be sure). All of the data this far is under CC BY 4.0. Matias and Santeri gave thought on how to bring the data to the end user. We have a vision on what we want the end product to be like, and we tried to find multiple solutions on how to get to our goal.

We added more data on top of the QGIS environment. Then we stared to think about how we can block out certain areas by making them invisible so that we could highlight the different areas altogether. So far nothing comes to mind since you can't really change the opacity on certain very specific layers, instead you can just zone out the opacity altogether by making it between 0 and 100%. This does not serve our purpose at all since currently there's no way to adjust the opacity of specific layers. 




// Santeri comments 

Data which we want to include in our map:

Train stations
Subway stations
Age
Education
Highways

We looked for more data to our map, like the population information grid, which we are trying to integrate into our map
Matias installed qgis2Web, and now we are trying to get it to work and find out what it does.
The next step is to find out, how to properly implement education levels into our map, and where to get the proper data to do so.


Links for our next step, integrating the qgis to a website, with better User Interface:

https://docs.geoserver.org/latest/en/user/services/wfs/outputformats.html
http://geoserver.org/
http://www.qgistutorials.com/en/docs/3/web_mapping_with_qgis2web.html

Converting excel files into qgis:

https://geospatialro.wordpress.com/2017/07/12/how-to-convert-excel-to-gis-data-in-qgis-using-spreadsheet-layers-plugin/

// Santeri comments 

## 15.10.2021

Today we started by adding some new files to our git. We now have all the needed licenses under their own .md-file.

