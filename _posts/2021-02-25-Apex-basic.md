---
layout:     post
title:     Apex Notes 1
subtitle:   BY Guanqiao Huang
date:       2021-02-25
author:     HUANG
header-img: img/post-bg-universe.jpg
catalog: true
tags:
    - Apex
---

# Apex Fundamentals
## Primitive Data Type
```Java
String greeting = 'Hello World';
System.debug(greeting);

Boolean amIAwake = true;
System.debug(amIAwake);

Integer rollNumber = 11008890;
System.debug(rollNumber);

Long worldPopulation = 7000000000L;
System.debug(worldPopulation);

Double lightSpeed = 93000000/186000;
System.debug(lightSpeed);

Date tDay = Date.newInstance(2020, 5, 18);
System.debug(tDay);

Time currentTime = Time.newInstance(3, 25, 0, 0);
System.debug(currentTime);

DateTime currentDateTime = DateTime.newInstance(2020, 5, 18, 3, 25, 0);
System.debug(currentDateTime);




//All null values
String greeting;
System.debug(greeting);

Boolean amIAwake;
System.debug(amIAwake);

Integer rollNumber;
System.debug(rollNumber);

Long worldPopulation;
System.debug(worldPopulation);

Double lightSpeed;
System.debug(lightSpeed);

Date tDay;
System.debug(tDay);

Time currentTime;
System.debug(currentTime);

DateTime currentDateTime;
System.debug(currentDateTime);
```

## String Class Methods
```Java
String str = ' i am a string variable ';
System.debug('Actual String: '+str);

// capitalize string
System.debug('Capitalize String: '+str.capitalize());

// contains example
System.debug('Contains ring? :'+ str.contains('ring'));

// convert to upper case
System.debug('Upper case: '+str.toUpperCase());
// convert to lower case
System.debug('Lower case: '+str.toLowerCase());

// equals
System.debug('Is equal to ring?: '+str.equals('ring'));
String str1 = 'Manish';
String str2 = 'maNish';
System.debug('str1 equals str2: '+str1.equals(str2));
System.debug('str1 equals str2 ignore case: '+str1.toLowerCase().equals(str2.toLowerCase()));

// remove
System.debug('Remove ring: '+str.remove('ring'));

// replace
System.debug('Replace ring: '+str.replace('ring', 'rong'));

// split
System.debug('Split by space: '+str.split(' '));

```
