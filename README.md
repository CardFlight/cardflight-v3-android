# CardFlight's Android SDK Library

## Introduction

The CardFlight Android SDK is used to process card present and card not-present transactions in your Android application.

CardFlight's SDK is based around keeping it as simple as possible while keeping the highest level of [security](https://developers.cardflight.com/help/security) at the forefront of all that we do. Take out the pain of PCI-compliance when building your app.

Authentication is done through your API Keys and processing is done through the Account Tokens. All connections to CardFlight's API are done through HTTPS over HSTS.

Documentation for our Android SDK can be found on cardflight.com, or by clicking [here](https://cardflight.com/docs/api/#android).

## Change Log

#### v3.6.1
* Bug fixes

#### v3.6
* Support for FDO Pre-Authorizations with Restaurant Merchant Accounts
* Bug fixes

#### v3.5.5
* Bug fixes

#### v3.5.4
* Bug fixes

#### v3.5.3
* Bug fixes

#### v3.5.2
* Bug fixes

#### v3.5.1
* Bug fixes

#### v3.5
* Added new Bluetooth Readers
* More reliable network calls
* Added vaulting during an EMV transaction
* Bug fixes

#### v3.2.7
* Bug fixes

#### v3.2.6
* Bug fixes

#### v3.2.5
* Bug fixes

#### v3.2.4
* Bug fixes

#### v3.2.3
* Improve reader connection reliability
* Bug fixes

#### v3.2.2
* Improve reader connection times
* Fix A100 reader connection problems
* Bug fixes

#### v3.2
* Add callback to receive more information about a card before charging
* Add method to charge a vaulted card
* Add Constants class to easily access keys used by various methods
* Improve connectivity issues and messaging
* Add method to disable reader timeouts
* Add callback when setting API Key and Account Token
* Improve reader connection times
* Bug fixes

#### v3.1.1
* Allow library to work with Proguard

#### v3.1
* Improve reader connection times
* Deprecate use of the readerIsConnecting callback in CardFlightDeviceHandler
* Fix tokenization and vaulting methods
* Bug fixes

#### v3.0.7
* New CardFlightError class
* Bug fixes

#### v3.0.6
* Increased Android M support
* Added serializable interface support for Card object

#### v3.0.5
* Bug fixes

#### v3.0.4
* Added EMV support.
* Update external libs.
* Bug fixes and improved stability.

#### v2.26
* Fix missing card holder name in Rambler reader.
* Update external libs.

#### v2.24

* New RestartReader API to restart reader while it connected.
* Fix crash when performing swipe related operations on reader which lost connection. DeviceDisconnected callback would be called on that occasion.
* Fix bug in auto config process.
* Improve stability of Payment View

#### v2.23
* Better Walker reader swipe detection.

#### v2.21
* Update more devices with the Walker reader.

#### v2.20
* Update more devices with the Walker reader.
* Improved messages.

#### v2.18
* Fix bug with failty swipe which causes another swipe attemp instead of failing.

#### v2.17
* New initializer for single device mode. SDK would try to connect only to overriden reader type.
* Fix bug while using initializer with overriden reader type.

#### v2.13
* Fix crash when setting custom swipetime before connecting reader.
* Improve support for custom swipe timeout.
* New StopSwipe API to cancel swipe operation.

#### v2.11
* New StopReader API to stop any pending operations.

#### v2.10
* Support Android 5+ devices.
* Remember last used reader type.
* Improved error handler.

#### v1.6:
* Updated methods for Void and Refund.
* New methods for Authorizing a charge and Capturing a charge.
* New Autoconfig handler for configuring devices that may not be compatibile on initial connection with reader.
* New zip code text field option in PaymentView.
* Ability to add metadata hashmap on Charge and Authorize methods.

## Setup

Import the cardflight-android folder as a library project into your application. Once the library project has been added, add the required permissions in the AndroidManifest.xml file.

### Installation

```
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.RECORD_AUDIO" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.BLUETOOTH" />
<uses-permission android:name="android.permission.BLUETOOTH_ADMIN" />
```

### Initialize

To access your CardFlight account you will need to set your Developer API key and the associated Merchant Account Token that you wish to connect to when making payments.

#### Example

```
CardFlight.getInstance()
		.setApiTokenAndAccountToken("e9cb15260f08e738b782952895d4ba4f",
				"acc_04ff8bf650afb268", null);
```

The CardFlight SDK is broken into easy-to-manage components. You just include the ones that you want to use in the header files of the classes that need to access those components.


##Supported Platforms

Our SDK supports a wide array of Android platforms. Click [here](https://developers.cardflight.com/docs/android) to view an updated list.


##Looking for iOS?

We've got you covered. Click [here](https://github.com/CardFlight/cardflight-ios) to learn more about our CardFlight iOS SDK.
