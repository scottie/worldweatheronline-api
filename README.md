# worldweatheronline-api
[![npm version](https://badge.fury.io/js/worldweatheronline-api.svg)](https://badge.fury.io/js/worldweatheronline-api)
[![Build Status](https://travis-ci.org/Rohithzr/worldweatheronline-api.svg?branch=master)](https://travis-ci.org/Rohithzr/worldweatheronline-api)

[![NPM](https://nodei.co/npm/worldweatheronline-api.png)](https://nodei.co/npm/worldweatheronline-api/)

un-official client for [WorldWeatherOnline's APIs](http://developer.worldweatheronline.com/api/)

## Installation
Install using npm:
```sh
npm install worldweatheronline-api --save
```

## Usage
Require library
```javascript
var WWO = require('worldweatheronline-api');
```
Create client
```javascript
var client = WWO.createClient({
    key: process.env.wwo_key,
    responseType: 'json',
    subscription: 'premium',
    locale: 'EN'
});
```
## Examples
examples based on usage
#### Search API
```javascript
client.searchApi({
    q: "Delhi"
}, function(err, result) {
    if (!err) {
        console.log(result);
    } else {
        console.log(err);
    }
});
```
#### Local Weather API
```javascript
client.localWeatherApi({
    q: "London",
    num_of_days: "3"
}, function(err, result) {
    if (!err) {
        console.log(result);
    } else {
        console.log(err);
    }
});
```
#### Time Zone API
```javascript
client.timeZoneApi({
    q: "208021"
}, function(err, result) {
    if (!err) {
        console.log(result);
    } else {
        console.log(err);
    }
});
```
#### Ski Weather API
```javascript
client.skiWeatherApi({
    q: "London",
    num_of_days: "2"
}, function(err, result) {
    if (!err) {
        console.log(result);
    } else {
        console.log(err);
    }
});
```
#### Marine Weather API
```javascript
client.marineWeatherApi({
    q: "48.834,2.394"
}, function(err, result) {
    if (!err) {
        console.log(result);
    } else {
        console.log(err);
    }
});
```
#### Historical Weather API
```javascript
client.historicalWeatherApi({
    q: "Delhi",
    date: "1995-05-02"
}, function(err, result) {
    if (!err) {
        console.log(result);
    } else {
        console.log(err);
    }
});
```

