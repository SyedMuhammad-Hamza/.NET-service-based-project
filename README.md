# .NET-service-based-project


(This project is based upon using windows service to scrap data from website as html, parse it to create .xml files, then using timer based azure function we finally 
combine these xml files to json files.)



Windows service to download webpage:
A Windows Service which downloads a web page after every 5 minutes by using the “Process” class available in Dot Net.



Windows service to parse data and create xml files:
A Windows Service which parses the data from the previous file after every 10 minutes to produce updated xml files.



Timer based azure function to create json files from xml:
A timer based Azure Function which is responsible to combine XML files and generate a JSON file for each of the script. You will have one JSON file output per script. 
The input for this service is the output directory from previous file.
