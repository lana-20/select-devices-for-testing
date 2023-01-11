# Selecting Devices and OS Versions for Testing

I need to pick 4 devices for testing, with their respective hardware and software versions. Which iOS and Android devices do I choose?

When selecting devices and OS versions for testing, I ask myself the following questions:
- What are the most used mobile OSs?
- What are the most used mobile OS versions?
- What are the most common screen sizes?
- Who are the leading manufacturers?

----

## What are the most used mobile OSs?
Mobile market [today](https://lana-20.github.io/mobile-os-market-share-2022/) looks much different from [10 years ago](https://lana-20.github.io/mobile-os-market-share-2012/). The market is dominated by two major vendors - Google (Android OS) and Apple (iOS).

## What are the most common screen sizes?

Google provides material.io [device metrics](https://material.io/blog/device-metrics), which includes iOS devices. It's a source of screen sizes, resolutions and other dimensions.

[Android Distribution Dashboard](https://developer.android.com/about/dashboards) provides info on screen sizes and densities. It also yields instructions on how to look up the Android version distribution info in Android Studio.

## What are the most used mobile OS versions?

I can find platform version information in Android Studio's __Create New Project wizard__:

<img width="700" alt="Screenshot 2023-01-11 at 1 17 47 PM" src="https://user-images.githubusercontent.com/70295997/211919774-27b870f4-b945-4e7b-acbd-fc19f37ae06d.png">

The Minimum SDK version determines the lowest level of Android that my app will run on. I typically want to target as many users as possible, so I'd ideally support everyone -- with a minSDK version 1. However, that has some disadvantages, such as lack of features, and very few people use such old devices. My choice of minSDK is a tradeoff between the ditribution of users I want to target and the features that my app will need.

Click on each Android Version/API level for more information.

Minimum SDK versions for Android 13 (T), aka Tiramisu:
<img width="764" alt="Screenshot 2023-01-11 at 1 19 28 PM" src="https://user-images.githubusercontent.com/70295997/211919974-dea5e6bf-5409-4bce-b659-79c73309ff88.png"><img width="762" alt="Screenshot 2023-01-11 at 1 20 13 PM" src="https://user-images.githubusercontent.com/70295997/211920108-ce43f88f-9596-49e9-aac4-41641d0a8058.png">

Minimum SDK versions for Android 12 and below:
<img width="764" alt="Screenshot 2023-01-11 at 1 20 39 PM" src="https://user-images.githubusercontent.com/70295997/211920162-e2a761be-71ea-4b3d-ae74-e8867f615f1d.png"><img width="765" alt="Screenshot 2023-01-11 at 1 22 19 PM" src="https://user-images.githubusercontent.com/70295997/211920415-2d1dc603-ec39-4ba3-b7c9-fce6808d5652.png"><img width="764" alt="Screenshot 2023-01-11 at 1 23 57 PM" src="https://user-images.githubusercontent.com/70295997/211920733-c8091d97-9717-42e9-815a-042de178ed3f.png"><img width="764" alt="Screenshot 2023-01-11 at 1 25 03 PM" src="https://user-images.githubusercontent.com/70295997/211920941-673c82ad-860f-45c5-819e-c821db503ea6.png">

...

<img width="763" alt="Screenshot 2023-01-11 at 1 28 41 PM" src="https://user-images.githubusercontent.com/70295997/211921588-01ac7a91-1fd1-46fa-bac7-ceaa174caab8.png">

Click on __Help me choose__ under a particular minSDK version to display additional distribution-related info:

<img width="700" alt="Screenshot 2023-01-11 at 1 45 47 PM" src="https://user-images.githubusercontent.com/70295997/211924558-12935186-90f9-49c8-89d2-586b629beae1.png">



