# Selecting Devices and OS Versions for Testing

I need to pick 4 devices for testing, with their respective hardware and software versions - model / OS version. Which iOS and Android devices do I choose?

When I start working on a new project, I need to know what I’m testing on. I’m a QA who has to know which devices to order. I’m the one who can tell the person in charge of the expense account in my company which devices my team needs. How to approach the decision of selecting devices for testing?

For this question, there is no right or wrong answer. It’s not accurate to say that a particular device, iPhone 7 for example, should not be tested on because I haven’t seen many people using iPhone 7s around lately. I split my time between San Francisco and Seattle, U.S. My subjective personal environment is not representative of the regional or global market, where the app may be distributed. The answer depends on where the app is used. I stay on top of things and keep track of the statistics data, in order to keep updating the device set consistently and timely.

When selecting devices and OS versions for testing, I ask myself the following questions:
- What are the most used mobile OSs?
- What are the most used mobile OS versions?
- What are the most common screen sizes?
- Who are the leading manufacturers?

<img width="800" alt="image" src="https://user-images.githubusercontent.com/70295997/212569492-e38768cb-a9a9-4712-a123-852ddcaac930.png">

[Strategic Test Coverage](https://www.perfecto.io/blog/strategic-test-coverage-key-considerations) includes:
1. Prioritizing Devices and Browsers for Testing
2. Device Market Share and Demographics
3. Most Popular Devices and Browsers
4. OS Popularity and Adoption
5. Mimicking the User’s Environment

When no [handy research](https://github.com/lana-20/mobile-os-market-share-2022) is available, I track the __Top 10 Mobile Devices__ via the [Test Coverage Guide](https://www.perfecto.io/test-coverage-guide) by region and country. For example:

<img width="800" alt="Screenshot 2023-01-14 at 1 40 38 AM" src="https://user-images.githubusercontent.com/70295997/212465831-e0ef155b-aa25-46c7-b4a5-ed33632634e6.png">
<img width="800" alt="image" src="https://user-images.githubusercontent.com/70295997/212465861-0307e2f8-cc88-4c54-aae3-554f9532ee94.png">
<img width="800" alt="Screenshot 2023-01-14 at 1 42 07 AM" src="https://user-images.githubusercontent.com/70295997/212465888-db57f7d1-08da-474a-befd-01bb9a70f690.png">


----

## [What are the most used mobile OSs?](https://github.com/lana-20/mobile-os-market-share-2022/blob/main/README.md)

I research the mobile OS market shares to find out which devices to pick/order and/or which to retire.

Mobile market [today](https://lana-20.github.io/mobile-os-market-share-2022/) looks much different from [10 years ago](https://lana-20.github.io/mobile-os-market-share-2012/). The market is dominated by two major vendors - Google (Android OS) and Apple (iOS).

## What are the most common screen sizes?

Google provides material.io [device metrics](https://material.io/blog/device-metrics), which includes iOS devices. It's a source of screen sizes, resolutions and other dimensions.

[Android Distribution Dashboard](https://developer.android.com/about/dashboards) provides info on screen sizes and densities. 

<img width="700" alt="Screenshot 2023-01-11 at 7 47 32 PM" src="https://user-images.githubusercontent.com/70295997/211971280-4567df34-6a62-472f-b9b0-738865ad8c3d.png">


The Dashboard also yields instructions on how to look up the Android version distribution info in Android Studio.

## What are the most used mobile OS versions?

### Android

I can find platform version information in Android Studio's __Create New Project wizard__:

<img width="700" alt="Screenshot 2023-01-11 at 1 17 47 PM" src="https://user-images.githubusercontent.com/70295997/211919774-27b870f4-b945-4e7b-acbd-fc19f37ae06d.png">

The Minimum SDK version determines the lowest level of Android that my app will run on. I typically want to target as many users as possible, so I'd ideally support everyone -- with a minSDK version 1. However, that has some disadvantages, such as lack of features, and very few people use such old devices. My choice of minSDK is a tradeoff between the distribution of users I want to target and the features that my app will need.

Click on each Android Version/API level for more information.

Minimum SDK versions for Android 13 (T), aka Tiramisu:
<img width="764" alt="Screenshot 2023-01-11 at 1 19 28 PM" src="https://user-images.githubusercontent.com/70295997/211919974-dea5e6bf-5409-4bce-b659-79c73309ff88.png"><img width="762" alt="Screenshot 2023-01-11 at 1 20 13 PM" src="https://user-images.githubusercontent.com/70295997/211920108-ce43f88f-9596-49e9-aac4-41641d0a8058.png">

Minimum SDK versions for Android 12 and below:
<img width="764" alt="Screenshot 2023-01-11 at 1 20 39 PM" src="https://user-images.githubusercontent.com/70295997/211920162-e2a761be-71ea-4b3d-ae74-e8867f615f1d.png"><img width="765" alt="Screenshot 2023-01-11 at 1 22 19 PM" src="https://user-images.githubusercontent.com/70295997/211920415-2d1dc603-ec39-4ba3-b7c9-fce6808d5652.png"><img width="764" alt="Screenshot 2023-01-11 at 1 23 57 PM" src="https://user-images.githubusercontent.com/70295997/211920733-c8091d97-9717-42e9-815a-042de178ed3f.png"><img width="764" alt="Screenshot 2023-01-11 at 1 25 03 PM" src="https://user-images.githubusercontent.com/70295997/211920941-673c82ad-860f-45c5-819e-c821db503ea6.png">

...

<img width="763" alt="Screenshot 2023-01-11 at 1 28 41 PM" src="https://user-images.githubusercontent.com/70295997/211921588-01ac7a91-1fd1-46fa-bac7-ceaa174caab8.png">

Click on __Help me choose__ under a particular minSDK version to display additional distribution-related info:

<img width="700" alt="Screenshot 2023-01-11 at 1 45 47 PM" src="https://user-images.githubusercontent.com/70295997/211924558-12935186-90f9-49c8-89d2-586b629beae1.png">

[Android Beta](https://www.google.com/android/beta) is the official link to follow for the latest info about Android Beta and its eligible devices. 

### iOS

Apple provides [iOS and iPadOS versions market shares](https://developer.apple.com/support/app-store/).

<img width="384" alt="Screenshot 2023-01-11 at 8 16 05 PM" src="https://user-images.githubusercontent.com/70295997/211974585-6c1d0444-6d9f-4340-8e78-9ac8770ad702.png">

Furthermore, this [source](https://mixpanel.com/trends/) provides iOS devices market share:

<img width="700" alt="Screenshot 2023-01-11 at 8 20 38 PM" src="https://user-images.githubusercontent.com/70295997/211975240-eafaa2bb-4d46-4cdb-a0c6-d7888a6eb08b.png">
<img width="700" alt="Screenshot 2023-01-11 at 8 22 03 PM" src="https://user-images.githubusercontent.com/70295997/211975374-b76a20b6-3cd6-4dc6-8dbb-21d6d304fcdb.png">

[iOS Beta](https://beta.apple.com/sp/betaprogram/) is the official link to sign up a device for running a beta version of iOS
.

----

[As Mobile Screen Size Increases... So Does Activity](https://www.lukew.com/ff/entry.asp?1956)

