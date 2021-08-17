# VKP App

## Introduction
There are many arcade machines which operate on insering the money in order to play arcade games. But with increase in usage of digital payment It is required to digitalise the machines to keep up with the current technology.

Solution was required to automatically credit the coins in game on succesful payment from UPI or other payment method.

This project was to build an android Application to credit coins for arcade machine through digital payment. 

<img src="https://i5.walmartimages.com/asr/03d65942-394b-4ad4-8ca1-8a193eef66e2_1.b92b219dfbb8d44c915da9809383d3d1.jpeg" alt="drawing" width="200"/>

## Project Implementation

We designed an Android mobile application using Java for user to interact with the machines using their mobile phone with multi role authentication using firebase.

We implemented payment gateway using razorpay API to recieve payment and on succesfull payment amount was credited to machine using NodeMCU and firebase realtime DB.


## Working

- A user pays the specified amount through a mobile or a web application.

- This payment is validated and processed by the Razorpay API and a feedback is sent to the web or mobile application.

- The app on receiving the payment authentication posts a http request to update a payment table in the firebase cloud. 

- The Nodemcu on the other hand which will be continuously querying for data from the cloud will now recognise the updated payment value.

- It will process the data and produce necessary electronic pulses for triggering the relay/LED or any electronic device.


<img src="/_static/projects/VKPApp/arch.png" alt="drawing" width="600"/>


## Tech Stack
Java, Android, Firebase, NodeMCU


## Github

``` {raw} html
    <a href="https://github.com/Gr8ayu/VKP_App" rel="some text"><img src="https://friconix.com/png/fi-xnsuxm-github.png" alt="github link" width=30px /></a>
```