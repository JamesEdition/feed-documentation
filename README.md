# JamesEdition Feed Guidelines

Version 3.2

Description of the feed formats for [JamesEdition - The world's largest luxury marketplace](http://www.jamesedition.com)

For Automobiles, Motorcycles, Real estates, Vacation rentals, Yachts and Jewellery listings.

Contact us in case of questions: support@jamesedition.com

## Change History

**3.2 June 22, 2015**
Added the new contact person tag “reference” +minor changes

**3.1 January 7, 2015**
Added vacation rental section along with other minor changes

**3.0 October 28, 2014**
Complete rewrite

**2.8 October 13, 2011**
Added contact persons to all categories

**2.7 August 11, 2011**
Minor changes throughout the document

**2.5 May 17, 2011**
Several new field options, some restructuring of the document New field options

**2.4 March 14, 2011**
Some new real estate types, minor corrections, added helicopter category

**2.3 February 10, 2011**
New tags for car category and watch category, new jet types for jet category

**2.2 January 24, 2011**
New Document, added real estate rental and minor changes to all categories

**2.1 November 17, 2010**
Many minor changes, added real estate.

**2.0 February 2, 2010**
Added two new optional Jet specific tags: serial_number and ttaf

## JamesEdition Data format

### Introduction

Please thoroughly read these instructions below to minimize the risk of mistakes or unfinished listings. The usage
of a **bold** font represents **very important information**. The `@` symbol followed by text explains what type of information that needs to be filled in after the equal `=` sign. The `@` symbol must not be included in the finished feed.

These instructions are presented to visually show how the JamesEdition XML feed is built and showcases how the
tags should be designed under their correct parent. his is to ensure all subtitles and optional fields are under their correct headline.

Please be advised that the image URL must be canonical and not change over time. All elements marked as *required* must be present in the feed, though some can be empty-closed. These include for example `<price/>` when `<price_on_request>` is set to `yes`.

Please name your file accordingly:

`JamesEdition_feed_<YOUR DEALER ID>.xml`. The filename must be static and cannot be changed over time.

XML encoded content in strings e.g. `&` should be `&amp;`. If you choose to skip optional tags, or leave them
empty, close them e.g. `<color />`

Dealers with multiple offices are required to supply independent feeds (stand-alone files) for each office. These
feeds will be connected with the unique JamesEdition office ID by the support or your account manager.

### Generic Feed Information

In the table below you can see the standard data entry options for the main feed information and the main dealership information.

```
<jamesedition_feed =”@version”> # Required, version has to be '3.0'
  <feed_information>
    <reference>REFERENCE</reverence> # Required, string (a-z, A-Z, 0-9, _-), your feed reference
    <title>TITLE</title> # Required, string, your feed title
    <description>DESCRIPTION</description> # Required, string, your description for the feed
    <created>TIMESTAMP</created> # Required, date (y-m-d h:i:s), feed creation time
    <updated>TIMESTAMP</updated> # Required, date (y-m-d h:i:s), feed update time
  </feed_information>
  <dealer>
    <reference>REFERENCE</reference> # Optional, string, dealer reference
    <name>NAME</name> # Required, string, dealer name
    <id>ID</id> # Required, integer, the JamesEdition if for the dealer 
  </dealer>
</jamesedition_feed>
```
  
