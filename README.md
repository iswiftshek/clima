# Clima

![Finished App](https://github.com/londonappbrewery/Images/blob/master/Clima.gif)

## Introduction
> This is an iOS app developed under the `Udacity` iOS Nanodegree. It uses Cocoapods (Alamofire and SwiftyJSON) to display the realtime weather of any city.

## Things To Have
**[Xcode](https://developer.apple.com/xcode/)**

### Libraries/Frameworks used and their documentation

- UIKit [Docs](https://developer.apple.com/documentation/uikit/)
- Alamofire [Docs](http://cocoadocs.org/docsets/Alamofire/1.2.3/)
- SwiftyJSON [Docs](http://cocoadocs.org/docsets/SwiftyJSON/3.0.0/)
- CoreLocation [Docs](https://developer.apple.com/documentation/corelocation)

## Development Setup

Before you begin, you should already have the Xcode downloaded and set up correctly. You can find a guide on how to do this here: [Setting up Xcode](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/Setup/Setup.html)

## Setting up the iOS Project

1. Download the _clima_ project source. You can do this either by forking and cloning the repository (recommended if you plan on pushing changes) or by downloading it as a ZIP file and extracting it.

2. Navigate to the unzipped folder and run pod install.

3. Open `Clima.xcworkspace` from the folder.

4. Build the project (⌘+B) and check for any errors.

5. Run the app (⌘+R) and test it.

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

## Acknowledgments

* This project is a starter project for anyone who wants to get into iOS Application Development
* Clima is a part of [Udacity iOS Nanodegree](https://in.udacity.com/course/ios-developer-nanodegree--nd003) and was developed during the study of the course 
* Credits to [The App Brewery](https://www.londonappbrewery.com/) for the Cocoapods and App Transport Security fixes
* All rights reserved 


