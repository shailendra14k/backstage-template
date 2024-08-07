# Instructions

## Update the DevSpace plugin

```yaml
pluginRegistry:
  openVSXURL: 'https://open-vsx.org'
```

## Module 2

### Update Expression of SetBody
```json
{"FlightID": "${random(1000)}","Airline": "Indigo","FlightNumber": "6E2286","OperatedBy": "IndiGo Airlines","From": "Ranchi","To": "Delhi"}
```

## Module 3

1. Click on the 3 dot of the log component and select append
2. Select the xj component

### Update below for the xj component 
- Resource Uri  --> json2xml.xsl
- Transform Direction ---> JSON2XML

## Module 4

1. Add the kafka component after the XJ component

### Update below for the Kafka component 
- Topic  --> {{topicName.json}}

## Module 5

1. Create a new route and read the data from the topic

### Update below for the Kafka component 
- Topic  --> {{topicName.json}}

2. Click on Kafka component on the design screen
3. Update the log component 
   - Message --> ${body}                                                                                 
4. Click on the 3 dot of the log component and select append 
5. Select the azure-storage-blob component

### Update below for the azure-storage-blob component
- Container Name ---> /azuredemoshsingh/test
- Blob Name ---> {{blobName}}
- Operation ---> uploadBlockBlob
```
