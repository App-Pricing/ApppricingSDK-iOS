![App Pricing](https://dash.apppricing.com/1x.png)

# AppPricing SDK

**AppPricing SDK** is an intelligent pricing optimization tool for mobile applications. It leverages advanced algorithms to analyze user behavior and characteristics, delivering tailored pricing strategies for each individual user. By integrating this SDK, your app can dynamically display the right paywall—whether premium, standard, or basic—based on sophisticated backend analysis.

![App Pricing Dashboard](https://dash.apppricing.com/appricing-main-banner.png)

Visit the [App Pricing](https://apppricing.com) to manage your pricing strategies or more details.

---

## Features

- **Dynamic Pricing**: Adjusts prices in real-time based on user behavior, location, and more.
- **User Segmentation**: Categorizes users into pricing tiers for maximum profitability.
- **Seamless Integration**: Easy-to-use SDK with minimal setup.

![App Pricing](https://dash.apppricing.com/3x.png)

---

## Example App

There's an example app that you can explore for further integration details:

[AppPricing-iOS](https://github.com/apppricingsdk/AppPricing-iOS)

## Getting Started

### 1. Installation

AppPricingSDK-iOS only supports Swift Package Manager.

1. **Add a Swift Package File**
   - In your Xcode project, go to **File** > **Swift Packages** > **Add Package Dependency**.
1. **Enter Package Repository URL**
   - https://github.com/apppricingsdk/ApppricingSDK-iOS
1. **Select fetched package**
1. **Click on the **Next** button to proceed and choose the target, which should be using the dependency**
1. **Integrate package**

### 2. Initialize the SDK

```swift
class AppDelegate: NSObject, UIApplicationDelegate {
    private let apiKey = "YOUR_API_KEY"

    func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) -> Bool {
        AppPricingInstance.initialize(
            apiKey: apiKey, // Required: Your API key from AppPricing Dashboard
            isDebug: true, // Optional: Enable debug mode for development
            errorCallback: { error in // Optional: Handle SDK Errors
                print(error.localizedDescription)
            }, logCallback: { logMessage in // Optional: Handle SDK logs
                print(logMessage)
            }
        )

        return true
    }

```

To obtain your `YOUR_API_KEY`, log in to the [AppPricing Dashboard](https://dash.apppricing.com), navigate to the Apps page, and copy your unique key as shown below:

![How to copy API key](https://dash.apppricing.com/image.png)

## Support

For technical support and inquiries:

- Email: support@apppricing.com
