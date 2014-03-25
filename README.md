SDL iOS SDK Sample App
======================

This is a sample app outlining the usage of the SDL iOS SDK. 

### Getting Started in 4 Easy Steps

#### STEP 1. Get Your SDL Language Cloud API Key

- [Sign Up Here] (https://languagecloud.sdl.com/translation-api/sign-up) to get a Free API Key

#### STEP 2. Install the SDK

- The SDK is available as a cocoapod and can be installed as follows:
 
```ruby
platform :ios, '7.0'
pod "SDL-iOS-SDK", "~> 0.1.0"
```

#### STEP 3. Import the SDK into your code

```ruby
#import "SDL.h"
```

#### STEP 4. Setup your API Key once

```ruby
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
   [[SDL languageCloud] setup:@"<your api key>"]
   ...
}
```

### Using the SDL Translation API

#### Performing a text translation

```ruby
 [[SDL languageCloud] translateText:@"Good Morning" from:[NSLocale localeWithLocaleIdentifier:@"en"] to:[NSLocale localeWithLocaleIdentifier:@"fr"] success:^(NSString* translation)
    {
        NSLog(@"Successful Translation: %@", translation);
    }
    failure:^(NSString* errorMessage)
    {
        NSLog(@"Error: %@", errorMessage);
    }
];
```

### License

The SDL iOS SDK is made available under the MIT license. Pleace see the LICENSE file 
for more details.

