![App Brewery Banner](Documentation/AppBreweryBanner.png)

# Clima

## Our Goal

It’s time to take our app development skills to the next level. We’re going to introduce you to the wonderful world of Cocoapods and open source libraries. These will power your apps to do incredible things without having to spend months coding up the functionality. Additionally, we’ll learn how to call Application Programming Interfaces (APIs) to grab data from websites. If you’re dreaming of making that Twitter-powered stock trading app then you’re about to get a lot closer to your goal!

## What you will create

Clima is a location-aware weather app. It will find out where you are in the world and query an open source weather service to retrieve the temperature and weather conditions. Also, you can change the city at the tap of a button. Want to know what it’s like in Rio? Clima is here to help. Weather apps are so popular that they get their own category in the App Store.

## What you will learn

* How to use CocoaPods to manage and use open source code libraries. 
* How to use the Command Line on Mac with Terminal.
* Learn about Networking calls.
* Use public web-based APIs to fetch data.
* How to parse data organised in JSON format.
* Learn about Core Location and utilising the iPhone’s inbuilt GPS. 
* Learn about navigation between View Controllers using Segues.
* Introduction to Delegates and Protocols.
* How to pass data between View Controllers.
* Learn and use Switch statements



## Fix for Cocoapods v1.0.1 and below

```ruby
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '3.0'
      config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '10.10'
    end
  end
end
```

## Fix for App Transport Security Override

```XML
	<key>NSAppTransportSecurity</key>
	<dict>
		<key>NSExceptionDomains</key>
		<dict>
			<key>openweathermap.org</key>
			<dict>
				<key>NSIncludesSubdomains</key>
				<true/>
				<key>NSTemporaryExceptionAllowsInsecureHTTPLoads</key>
				<true/>
			</dict>
		</dict>
	</dict>
```

>This is a companion project to The App Brewery's Complete App Developement Bootcamp, check out the full course at [www.appbrewery.co](https://www.appbrewery.co/)

![End Banner](Documentation/readme-end-banner.png)

