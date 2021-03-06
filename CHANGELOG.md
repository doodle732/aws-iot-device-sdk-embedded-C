#Change Log
## [2.0.0](https://github.com/aws/aws-iot-device-sdk-embedded-C/releases/tag/v2.0.0) (April 28, 2016)

New features:

  - Refactored API to make it instance specific. This is a breaking change in the API from 1.x releases because a Client Instance parameter had to be added to all APIs
  - Added Threading library porting layer wrapper
  - Added support for multiple connections from one application
  - Shadows and connections de-linked, connection needs to be set up separately, can be used independently of shadow
  - Added integration tests for testing SDK functionality

Bugfixes/Improvements:

  - Yield cannot be called again while waiting for application callback to return
  - Fixed issue with TLS layer handles not being cleaned up properly on connection failure reported [here](https://github.com/aws/aws-iot-device-sdk-embedded-C/issues/16)
  - Renamed timer_linux.h to timer_platform.h as requested [here](https://github.com/aws/aws-iot-device-sdk-embedded-C/issues/5)
  - Adds support for disconnect handler to shadow. A similar pull request can be found [here](https://github.com/aws/aws-iot-device-sdk-embedded-C/pull/9)
  - New SDK folder structure, cleaned and simplified code structure
  - Removed Paho Wrapper, Merge MQTT into SDK code, added specific error codes
  - Refactored Network and Timer layer wrappers, added specific error codes
  - Refactored samples and makefiles
  
## [1.1.2](https://github.com/aws/aws-iot-device-sdk-embedded-C/releases/tag/v1.1.2) (April 22,  2016)

Bugfixes/Improvements:

  - Signature mismatch in MQTT library file fixed
  - Makefiles have a protective target on the top to prevent accidental execution

## [1.1.1](https://github.com/aws/aws-iot-device-sdk-embedded-C/releases/tag/v1.1.1) (April 1, 2016)

Bugfixes/Improvements:

  - Removing the Executable bit from all the files in the repository. Fixing [this](https://github.com/aws/aws-iot-device-sdk-embedded-C/issues/14) issue
  - Refactoring MQTT client to remove declaration after statement warnings
  - Fixing [this](https://forums.aws.amazon.com/thread.jspa?threadID=222467&tstart=0) bug
 

## [1.1.0](https://github.com/aws/aws-iot-device-sdk-embedded-C/releases/tag/v1.1.0) (February 10, 2016)
Features:

  - Auto Reconnect and Resubscribe
  
Bugfixes/Improvements:

  - MQTT buffer handling incase of bigger message
  - Large timeout values converted to seconds and milliseconds
  - Dynamic loading of Shadow parameters. Client ID and Thing Name are not hard-coded
  - MQTT Library refactored


## [1.0.1](https://github.com/aws/aws-iot-device-sdk-embedded-C/releases/tag/v1.0.1) (October 21, 2015)

Bugfixes/Improvements:

  - Paho name changed to Eclipse Paho
  - Renamed the Makefiles in the samples directory 
  - Device Shadow - Delete functionality macro fixed
  - `subscribe_publish_sample` updated

## [1.0.0](https://github.com/aws/aws-iot-device-sdk-embedded-C/releases/tag/v1.0.0) (October 8, 2015)

Features:

  - Release to github
  - SDK tarballs made available for public download

Bugfixes/Improvements:
  - Updated API documentation
 
## 0.4.0 (October 5, 2015)

Features:

  - Thing Shadow Actions - Update, Delete, Get for any Thing Name
  - aws_iot_config.h file for easy configuration of parameters
  - Sample app for talking with console's Interactive guide
  - disconnect handler for the MQTT client library
  
Bugfixes/Improvements:

  - mbedTLS read times out every 10 ms instead of hanging for ever
  - mbedTLS handshake failure handled

## 0.3.0 (September 14, 2015)

Features:

  - Testing with mbedTLS, prepping for relase

Bugfixes/Improvements:

  - Refactored to break out timer and network interfaces

## 0.2.0 (September 2, 2015)

Features:

  - Added initial Shadow implementation + example
  - Added hostname verification to OpenSSL example
  - Added iot_log interface
  - Initial API Docs (Doxygen)

Bugfixes/Improvements:

  - Fixed yield timeout
  - Refactored APIs to pass by reference vs value

## 0.1.0 (August 12, 2015)

Features:

  - Initial beta release
  - MQTT Publish and Subscribe
  - TLS mutual auth on linux with OpenSSL

Bugfixes/Improvements:
	- N/A
