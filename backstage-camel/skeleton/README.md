// 

Module 2

1. Chnage the Timer period to 300000 i.e 5 min
##Update Expression of SetBody
{"FlightID": "${random(1000)}","Airline": "Indigo","FlightNumber": "6E2286","OperatedBy": "IndiGo Airlines","From": "Ranchi","To": "Delhi"}



Module 3

1. Click on the 3 dot of the log component and select append
2. Select the kafka component
  ##Update below for the Kafka component 
    Topic  --> {{topicName.json}}

Module 4

1. Create a new route and read the data from the topoic`qww
  ##Update below for the Kafka component 
    Topic  --> {{topicName.json}}
2. Click on Kafka component on the degisn screen and add xj component
   ##Update below for the Kafka component 
   Resource Uri  --> json2xml.xsl
   Transform Direction ---> JSON2XML
3 Update the the log component 
   Message --> ${body}
                                                                                 
Module 5

1. Click on the 3 dot of the log component and select append 
2. Select the azure-storage-blob component 
  ##Update below for the azure-storage-blob component
    Container Name ---> /azuredemoshsingh/test
    Blob Name ---> {{blobName}}
    Operation ---> uploadBlockBlob

