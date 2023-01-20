# Selecting Devices and OS Versions for Testing
<img width="350" src="https://user-images.githubusercontent.com/70295997/213065698-c72863c5-285c-4681-870b-62d8350501ca.png">

_I need to __pick 4 devices__ for testing, with their respective __hardware and software versions - model / OS version__. Which iOS and Android devices do I choose?_

When I start working on a new project, I need to know what I’m testing on. I’m a QA who has to know which devices to order. I’m the one who can tell the person in charge of the expense account in my company which devices my team needs. How to approach the decision of selecting devices for testing?

For this question, there is no right or wrong answer. It’s not accurate to say that a particular device, iPhone 7 for example, should not be tested on because I haven’t seen many people using iPhone 7s around lately. I split my time between San Francisco and Seattle, U.S. My subjective personal environment is not representative of the regional or global market, where the app may be distributed. While only a few percents of the target demographic use iPhone 7, this small market segment may be essential to your particular company software. 

The answer depends on usage patterns of the app. In the volatile and fast-paced tech industry, I always stay on top of things and keep track of the statistics data, in order to keep updating the device set consistently and timely.

When selecting devices and OS versions for testing, I ask myself the following questions:
- _What are the most used mobile <code>OSs</code>?_
- _What are the most used mobile <code>OS versions</code>?_
- _What are the most common <code>screen sizes</code>?_
- _Who are the leading <code>manufacturers</code>?_

<img width="600" alt="image" src="https://user-images.githubusercontent.com/70295997/212569492-e38768cb-a9a9-4712-a123-852ddcaac930.png">

Furthermore, I care for providing adequate/strategic [Test Coverage](https://github.com/lana-20/test-coverage). My strategy typically includes:
1. Prioritizing Devices and Browsers for Testing
2. Device Market Share and Demographics
3. Most Popular Devices and Browsers
4. OS Popularity and Adoption
5. [Mimicking the User’s Environment](https://github.com/lana-20/emulator-simulator/blob/main/README.md)

When no [handy research](https://github.com/lana-20/mobile-os-market-share-2022) is available, it's rather easy to track the __device and OS combinations__ via the [Test Coverage Guide](https://www.perfecto.io/test-coverage-guide) across 13 different countries.

<img width="800" alt="image" src="https://user-images.githubusercontent.com/70295997/213078533-fc9dad64-7277-497e-905e-19026b7c8ef2.png">

----

## [What are the most used mobile OSs?](https://github.com/lana-20/mobile-os-market-share-2022/blob/main/README.md)

I research the mobile OS market shares to find out which devices to pick/order and/or which to retire.

Mobile market [today](https://lana-20.github.io/mobile-os-market-share-2022/) looks much different from [10 years ago](https://lana-20.github.io/mobile-os-market-share-2012/). The market is dominated by two major vendors - the Big Two - Google (Android OS) and Apple (iOS).

## What are the most common screen sizes?

<img src="https://user-images.githubusercontent.com/70295997/213389292-7d8ab5f4-ba0e-4a52-8a22-69e2508f5ff8.png" width=600>

Google provides material.io [device metrics](https://material.io/blog/device-metrics), which includes iOS devices. It's a source of screen sizes, resolutions and other dimensions.

[Android Distribution Dashboard](https://developer.android.com/about/dashboards) provides info on screen sizes and densities. 

<img width="600" alt="Screenshot 2023-01-11 at 7 47 32 PM" src="https://user-images.githubusercontent.com/70295997/211971280-4567df34-6a62-472f-b9b0-738865ad8c3d.png">

The Dashboard also yields instructions on how to look up the Android version distribution info in Android Studio.

## What are the most used mobile OS versions?

As a Software Quality Engineer, I stay abreast of the various OS versions by following the tech news/blogs/conferences and communicating with IT counterparts. When conducting Mobile testing, as compared to Web, I handle __Compatibility/Interoperability__ Testing not only among platforms/OSs but also among specific versions of these platforms/OSs (aka Cross-Version Testing). This experience/exposure is essential when addressing issues such as:
- [Downgrading from iOS 16.3 to 16.2 while keeping the data on iPhone 14](https://github.com/lana-20/select-devices-for-testing/blob/main/Screenshot%202023-01-17%20at%201.52.12%20PM.png) ➦ iPhone 14 series never had iOS 15.
- [Verifying if iOS 16 can be installed on iPhone 7](https://github.com/lana-20/select-devices-for-testing/blob/main/Screenshot%202023-01-17%20at%204.47.01%20PM.png) ➦ iPhone 7 series doesn't support iOS 16.
- [Checking which Android OS versions support Bluetooth](https://github.com/lana-20/select-devices-for-testing/blob/main/Screenshot%202023-01-17%20at%208.56.06%20PM.png) ➦ Android Jelly Bean v4.3 and above (minSDK/API Level 18+) supports Bluetooth.

Consider a scenario with 4+ billion people accessing the web through combinations of:
- 9000+ distinct devices, shipped with
- 21 different operating systems (vendor + version), along with
- 8 major browser engines that power hundreds of browsers.

Combined, they make at least 63,000 possible browser-platform-device combinations. That’s the scale of fragmentation. [_Fragmentation_](https://github.com/lana-20/mobile-fragmentation) is the sum total of differences—between devices, platforms, browsers, variables like [network providers](https://www.t-mobile.com/news/network/t-mobile-kicks-off-2023-as-ookla-network-leader) and more. Fragmentation is a problem, because the differences between devices, platforms, browsers, and more cannot be abstracted by a single, universally interoperable framework.

<img width="600" alt="Screenshot 2023-01-18 at 10 59 14 PM" src="https://user-images.githubusercontent.com/70295997/213376215-2b9b0cd6-5b11-403a-b6fe-8bc0848347a3.png">

Since a website/app can’t have universal __Interoperability__ on every possible combination of device, operating system, and browser in the market, I have to settle for its watered-down counterpart, __Compatibility__.

<img width="1000" src="https://user-images.githubusercontent.com/70295997/213380399-92acb7a8-f0af-4d86-8e17-d8ce2966dd59.png">

To achieve compatibility, I have to test every bit of code across browsers, platforms, and devices. Or I have to keep your developers busy with an endless barrage of cross-browser and cross-platform bugs that creep into the builds (or worse, production).

### Android

I can find platform version information in Android Studio's __Create New Project wizard__:

<img width="600" alt="Screenshot 2023-01-11 at 1 17 47 PM" src="https://user-images.githubusercontent.com/70295997/211919774-27b870f4-b945-4e7b-acbd-fc19f37ae06d.png">

The Minimum SDK version ([API Level](https://www.youtube.com/watch?v=lmozs_yqLY8&list=PPSV&ab_channel=BandeKhoda)) determines the lowest level of Android that my app will run on. I typically want to target as many users as possible, so I'd ideally support everyone -- with a minSDK version 1. However, that has some disadvantages, such as lack of features, and very few people use such old devices. My choice of minSDK is a tradeoff between the distribution of users I want to target and the features that my app will need.

Click on each Android Version/API level for more information.

<img width="600" alt="image" src="https://user-images.githubusercontent.com/70295997/213084570-7215edf1-96aa-4656-8f5a-11e1595a2b14.png">

Click on __Help me choose__ under a particular minSDK version to display additional distribution-related info:

<img width="700" src="https://user-images.githubusercontent.com/70295997/211924558-12935186-90f9-49c8-89d2-586b629beae1.png">

‼️ The [first update to the Android distribution chart in 2023 ](https://9to5google.com/2023/01/18/android-13-device-distribution/) has been released, showing that devices running Android 13 now make up 5.2% of all devices. This is a significant increase from August's 13.5% figure for Android 12 and 12L. This suggests that Android 13 is being delivered to devices more quickly than previous versions. Notably, while Google’s chart does include details about Android 13, it doesn’t make a distinction between Android 12 and 12L. This means that Android 12 and 12L combined now account for 18.9% of the total.

Additionally, older versions of Android such as Oreo and Jelly Bean have seen a decrease in usage. Usage of Android Oreo has finally dropped below 10%, with similar drops in percentage down the line. Android Jelly Bean, which previously weighed in at 0.3%, is no longer listed, while KitKat has dropped from 0.9% to 0.7%.

No doubt the speed of Android 13’s adoption is thanks in part to the rapid roll out of updates by phone makers including Google, Samsung, OnePlus, Sony, and more. These companies have been pushing out updates quickly to ensure that their customers can access the latest features and security enhancements offered by Android 13.

![image](https://user-images.githubusercontent.com/70295997/213598729-3b41f771-fb05-4b59-ad6a-683d166a77ce.png)
<img width="700" src="https://user-images.githubusercontent.com/70295997/213598647-ac351b77-358c-46fa-899b-e8e148bfff8d.png">

In the past, Google used to share data on its official website, which was based on the number of Android devices that accessed the Google Play Store during a one-week period. Now, this data can be found in Android Studio, and it is likely that the numbers are still based on the same metric.

[Android Beta](https://www.google.com/android/beta) is the official link to follow for the latest info about Android Beta and its eligible devices. 

### iOS

Apple provides [iOS and iPadOS versions market shares](https://developer.apple.com/support/app-store/). Furthermore, this [source](https://mixpanel.com/trends/) provides iOS devices market share.

<img width="1000" alt="Screenshot 2023-01-17 at 6 40 55 PM" src="https://user-images.githubusercontent.com/70295997/213068791-03c82b2a-d16f-4d65-897f-ec572bf46f9d.png">

[iOS Beta](https://beta.apple.com/sp/betaprogram/) is the official link to sign up a device for running a beta version of iOS.

## Who are the leading manufacturers?

<img width="1000" alt="Screenshot 2023-01-17 at 4 40 04 PM" src="https://user-images.githubusercontent.com/70295997/213052412-3e499e11-9f04-4f48-8eb7-126dff620395.png">

<img width="600" src="https://user-images.githubusercontent.com/70295997/213068053-d40d6427-ec3b-4d8a-a00e-cbc3b67c3c0c.png">

----

Extra 📚: 

[As Mobile Screen Size Increases... So Does Activity](https://www.lukew.com/ff/entry.asp?1956)

[Infographic: Fragmentation in OS, browsers, and devices](https://www.browserstack.com/blog/what-is-fragmentation/)

[App Download Data (2023)](https://www.businessofapps.com/data/app-statistics/)

[90% South East Asians connect to internet through smartphones](https://www.businesstimes.com.sg/international/asean/mobile-app-users-sea-cost-less-acquire-report)

