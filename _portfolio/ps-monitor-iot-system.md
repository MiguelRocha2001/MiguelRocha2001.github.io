---
title: "PS-Monitor-IoT-System"
excerpt: "Insert here a descrioption."
header:
  image: /assets/images/o-que-e-hardware-ram-1-.jpg
  teaser: assets/images/o-que-e-hardware-ram-1-.jpg
sidebar:
  - title: "Responsibilities"
    text: "Developer, Designer"
  - title: "Co-Author"
    text: "Pedro Silva, Psilva20019@gmail.com"
  - title: "Advisor"
    text: "Rui Duarte, rui.duarte@isel.pt"
---

This project consists in the creation of a smart and automated system, using IoT technology, to enhance theefficiency, accuracy and safety in the pH industrial control process. By incorporating sensors, we can detectproblems before they lead to costly downtime or safety hazards.The sensors collect data relative to the neutralization system’s environment. All this data is sent to a centralserver, and through real-time data analysis, it identifies if the neutralization system is not working optimally.
{: style="text-align: justify;"}

- [Final report](https://github.com/MiguelRocha2001/PS-Monitor-IoT-System/blob/main/Documentation/Report/IoT_System_for_pH_Monitoring_in_Industrial_Facilities.pdf)

## System Overview

The system is composed of the following components:
  - IoT Sensor Node: collects the data from the neutralization device;
  - Backend: receives and processes the data emitted by all the registered MCUs;
  - Web Application: allows the user to register devices and analyse device-collected data.

<figure>
  <img src="/assets/images/System architecture.png" alt="System Overview">
  <figcaption style="font-style: italic;">System Overview Diagram</figcaption>
</figure>

**Notice:** This project was evaluated as 18/20.
{: .notice--success}

[See on github](https://github.com/MiguelRocha2001/PS-Monitor-IoT-System){: .btn .btn--info}

## Hardware

The system uses a built in Android app to configure the ESP-32, which is the microcontroller used in the IoT sensor node. The app allows the user to configure the WiFi network. The ESP-32 is connected to a pH sensor, a temperature sensor, and more.

<figure class="half">
    <img src="/assets/images/screen_shot_2016-04-27_at_1.30.27_pm_0.png">
    <img src="/assets/images/ESP32-S2-Assembly_bb.png">
    <figcaption>Configuration App and ESP-32</figcaption>
</figure>

## Website

The website is the main interface for the user to interact with the system. The user can register devices, see the data collected by the devices, and analyse the data.

<figure>
    <img src="/assets/images/Website.png">
    <figcaption>Website Data Analysis page</figcaption>
</figure>

## Deploy

The system uses Docker technology to deploy the backend and the web application. The server, which also serves the static content, the PostgreSQL database, and the InfluxDB, are all deployed in separate containers. This allows to scale all components independently.

<figure>
    <img src="/assets/images/GCP VM Arquitecture.png">
    <figcaption>Deploy Diagram</figcaption>
</figure>

### Demo
{% include video id="3nySVzwPdcc" provider="youtube" %}