# Airship Quickstart
A quickstart overview on Airship with Images! Visual step by step with images to follow along

<img align="center" alt="redesign of thumbnails" width="500px" src="https://vectorlogoseek.com/wp-content/uploads/2019/07/urban-airship-inc-vector-logo.png" />

<img align="center" alt="man spilling chili on the ground" width="500px" src="https://media.giphy.com/media/nuhtVdDkeUmZ2/giphy.gif" />

## Table of Contents
1. [Create a new message](#development-setup)
1. [Adding images to a Message](#development-setup)
1. [Scheduling a Message](#running)
1. [Creating a test group](#dependencies-overview)
1. [Sending a message to an exclusive group](#workflow)

## For Developers
1. [API Overview](#api-overview)
1. [Getting Ready for an API](#api-setup)
3. [API Requests](#api-requests)


## GET Schedule

jQuery
```
var settings = {
  "url": "https://go.urbanairship.com/api/schedules",
  "method": "GET",
  "timeout": 0,
  "headers": {
    "Accept": "{{airshipAccept}}"
  },
};

$.ajax(settings).done(function (response) {
  console.log(response);
});
```

Javascript Fetch
```
var myHeaders = new Headers();
myHeaders.append("Accept", "application/vnd.urbanairship+json; version=3");

var requestOptions = {
  method: 'GET',
  headers: myHeaders,
  redirect: 'follow'
};

fetch("https://go.urbanairship.com/api/schedules", requestOptions)
  .then(response => response.text())
  .then(result => console.log(result))
  .catch(error => console.log('error', error));
```

CURL
```
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => 'https://go.urbanairship.com/api/schedules',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'GET',
  CURLOPT_HTTPHEADER => array(
    'Accept: application/vnd.urbanairship+json; version=3'
  ),
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
```
