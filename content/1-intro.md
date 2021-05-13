---
title: Introduction
nav: Intro
---

In this workshop, we intend to familiarized you with three different types of data formats, CSV, XML, and JSON. 

### CSV - Comma Separated Values

The Comma Separated Values (CSV) format is basically, the plain text version of a spreadsheet. The format defines its cells by separating data via commas. 

You might ask, but "what if my data has a comma in it?" -- in that case, we separate the value via quotation marks. 


#### CSV Example


```
title,latlng,latitude,longitude,link 1,link 2
"Basin Butte, aka 'the Best Basin'","-114.97766,44.33853",-114.97766,44.33853,basinbutte.html,http://www.firelookout.com/id/basinbutte.html
Beartrap,"-114.44392,45.39143",-114.44392,45.39143,beartrap.html,http://www.firelookout.com/id/beartrap.html
Bell Mtn.,"-114.11104,43.43099",-114.11104,43.43099,bellmtn.html,http://www.firelookout.com/id/bellmtn.html

```

## XML - Extensible Markup Language

The Extensible Markup Language is a commonly used data format that looks a lot like HTML, the foundational markup language of the internet. XML is, as it's name suggests, quite extensible. It is intended to be a simple, human-readable, and usable format that can be used in a variety of applications and descriptions. 

We are looking at XML because it is the basis for a number of different formats, including 

[Learn More](https://www.w3schools.com/xml/default.asp)

#### XML Example

```
<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<kml xmlns="http://www.opengis.net/kml/2.2">
  <Document>
    <name><![CDATA[GPS data]]></name>
    <visibility>1</visibility>
    <open>0</open>
    <Snippet><![CDATA[created using <A href="http://www.gpsvisualizer.com/?ref=ge&time=20180120185927">GPS Visualizer</A>]]></Snippet>
    <Style id="gv_waypoint_normal">
      <IconStyle>
        <color>ffffffff</color>
        <scale>1</scale>
        <Icon>
          <href>http://maps.google.com/mapfiles/kml/pal4/icon56.png</href>
        </Icon>
        <hotSpot x="0.5" xunits="fraction" y="0.5" yunits="fraction" />
      </IconStyle>
      <LabelStyle>
        <color>ffffffff</color>
        <scale>1</scale>
      </LabelStyle>
      <BalloonStyle>
        <text><![CDATA[<div style="font-family:Arial,sans-serif; min-width:200px;"><h3>$[name]</h3> <div style="margin-top:8px;">$[description]</div></div>]]></text>
      </BalloonStyle>
    </Style>
    <Style id="gv_waypoint_highlight">
      <IconStyle>
        <color>ffffffff</color>
        <scale>1.2</scale>
        <Icon>
          <href>http://maps.google.com/mapfiles/kml/pal4/icon56.png</href>
        </Icon>
        <hotSpot x="0.5" xunits="fraction" y="0.5" yunits="fraction" />
      </IconStyle>
      <LabelStyle>
        <color>ffffffff</color>
        <scale>1</scale>
      </LabelStyle>
      <BalloonStyle>
        <text><![CDATA[<div style="font-family:Arial,sans-serif; min-width:200px;"><h3>$[name]</h3> <div style="margin-top:8px;">$[description]</div></div>]]></text>
      </BalloonStyle>
    </Style>
    <StyleMap id="gv_waypoint">
      <Pair>
        <key>normal</key>
        <styleUrl>#gv_waypoint_normal</styleUrl>
      </Pair>
      <Pair>
        <key>highlight</key>
        <styleUrl>#gv_waypoint_highlight</styleUrl>
      </Pair>
    </StyleMap>
    <Folder id="Waypoints">
      <name>Waypoints</name>
      <visibility>1</visibility>
      <Placemark>
        <name>Basin Butte</name>
        <description><![CDATA[<p>[<a target="_blank" href="http://www.firelookout.com/id/basinbutte.html">http://www.firelookout.com/id/basinbutte.html</a>]</p>]]></description>
        <styleUrl>#gv_waypoint</styleUrl>
        <Style>
          <IconStyle>
            <Icon>
              <href>http://www.firelookout.com/losign.jpg</href>
            </Icon>
          </IconStyle>
        </Style>
        <Point>
          <altitudeMode>clampToGround</altitudeMode>
          <coordinates>-114.97766,44.33853</coordinates>
        </Point>
      </Placemark>
    </Folder>
  </Document>
</kml>
```

## JSON - JavaScript Object Notation

Although its title indicates it's a part of JavaScript, JSON has become so popular it is now language-indepent. It uses key-value pairs and specific formatting to define and next information for use in a variety of applications and software. 


[Learn More](https://www.w3schools.com/js/js_json_intro.asp)

#### JSON Example

```
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 27,
  "address": {
    "streetAddress": "21 2nd Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10021-3100"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "212 555-1234"
    },
    {
      "type": "office",
      "number": "646 555-4567"
    }
  ],
  "children": [],
  "spouse": null
}
```

## JSON vs. XML

[W3Schools](https://www.w3schools.com/js/js_json_xml.asp)