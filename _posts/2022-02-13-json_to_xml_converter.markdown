---
layout: post
title:      "JSON to XML Converter"
date:       2022-02-13 19:18:54 +0000
permalink:  json_to_xml_converter
---


You are likely familiar with JavaScript Object Notation, more commonly known as JSON. JSON is an open standard file format and data interchange format that is used to store and transmit data objects by making use of key:value pairs. While JSON has origins in JavaScript, there is support for JSON is nearly every programming language, as it has become a fairly ubiquitous way to store and transmit data.

However, occasionaly you may find yourself needing the same data to be available in but in a different format. One such format you may come across is XML. Similar to JSON, XML (or Extensible Markup Language) is a markup language and file format for storing and transmitting data. Converting a JSON object or file to XML could be a painstaking process, especially if you are not as familiar with XML as you are with JSON, or perhaps you are not familiar with XML at all. Depending on the size of your data set, manual conversion may be entirely out of the question as it is not a reasonable use of time.

Enter the convenient [JSON to XML Converter](https://www.convertjson.com/json-to-xml.htm). This web based tool makes it simple to convert JSON to XML with just a few quick clicks. Simply paste your JSON into the JSON window, click "Convert JSON to XML", and behold the results. The tool also supports importing a JSON file, downloading the result as an XML file, importing the JSON from a URL, and has a built-in JSON formatter if you would like to clean up your source formatting. The tool also works in the [reverse direction](https://www.convertjson.com/xml-to-json.htm), allowing you to convert XML to JSON. 

Example of the results:

JSON:
```
{
   "id": "0001",
   "type": "donut",
   "name": "Cake",
   "ppu": 0.55,
   "batters": {
      "batter": [
         {
            "id": "1001",
            "type": "Regular"
         },
         {
            "id": "1002",
            "type": "Chocolate"
         },
         {
            "id": "1003",
            "type": "Blueberry"
         },
         {
            "id": "1004",
            "type": "Devil's Food"
         }
      ]
   },
   "topping": [
      {
         "id": "5001",
         "type": "None"
      },
      {
         "id": "5002",
         "type": "Glazed"
      },
      {
         "id": "5005",
         "type": "Sugar"
      },
      {
         "id": "5007",
         "type": "Powdered Sugar"
      },
      {
         "id": "5006",
         "type": "Chocolate with Sprinkles"
      },
      {
         "id": "5003",
         "type": "Chocolate"
      },
      {
         "id": "5004",
         "type": "Maple"
      }
   ]
}
```

XML:
```
<?xml version="1.0" encoding="UTF-8" ?>
<root>
  <id>0001</id>
  <type>donut</type>
  <name>Cake</name>
  <ppu>0.55</ppu>
  <batters>
    <batter>
      <id>1001</id>
      <type>Regular</type>
    </batter>
    <batter>
      <id>1002</id>
      <type>Chocolate</type>
    </batter>
    <batter>
      <id>1003</id>
      <type>Blueberry</type>
    </batter>
    <batter>
      <id>1004</id>
      <type>Devil&#x27;s Food</type>
    </batter>
  </batters>
  <topping>
    <id>5001</id>
    <type>None</type>
  </topping>
  <topping>
    <id>5002</id>
    <type>Glazed</type>
  </topping>
  <topping>
    <id>5005</id>
    <type>Sugar</type>
  </topping>
  <topping>
    <id>5007</id>
    <type>Powdered Sugar</type>
  </topping>
  <topping>
    <id>5006</id>
    <type>Chocolate with Sprinkles</type>
  </topping>
  <topping>
    <id>5003</id>
    <type>Chocolate</type>
  </topping>
  <topping>
    <id>5004</id>
    <type>Maple</type>
  </topping>
</root>
```
