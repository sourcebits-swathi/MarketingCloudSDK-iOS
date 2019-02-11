---
layout: page
title: "Personalization Builder and Collect API Integration"
subtitle: "Integrate Personalization Builder and Collect API"
category: analytics
date: 2018-01-10 12:00:00
order: 2
---

### Analytic Attribution

Personalization Builder analytics uses an unique identifier to attribute collected analytics to a specific user. By default, the SDK uses the contact key as this identifier, called the PIID. Your app can explicitly set this value.

The Mobile Push SDK has an optional configuration option called useLegacyPiIdentifier. This option replaces an absent or empty PIID with the MobilePush contact key. If this configuration option is false, the SDK doesn’t replace an absent or empty PIID. Review [Configure the SDK]({{ site.baseurl }}/get-started/apple.html#4-configure-the-sdk) to configure the SDK with pianalytics and useLegacyPiIdentifier.

> **Important:** To ensure future compatibility, we recommend explicitly setting the PIID. The useLegacyPiIdentifier configuration option will be deprecated in a future release.

#### Example: Analytic Attribution
{% include gist.html sectionId="contactkey" names="Obj-C,Swift" gists="https://gist.github.com/sfmc-mobilepushsdk/c8de13c1b560a19def8bc2d63a2f061c.js,https://gist.github.com/8c9d0186ce37fb00aff742880bcbab08.js" %}

### Integration Methods

These methods integrate your mobile app with Personalization Builder. To use the methods, you must have an existing [Personalization Builder](http://help.marketingcloud.com/en/documentation/personalization_builder) deployment, and you must enable the "pianalytics" option when you configure your SDK.

#### Track Cart

To track the contents of an in-app shopping cart, use the method shown in the example. For more information about this method’s general use with Personalization Builder, review [Track Items in Shopping Cart](https://help.salesforce.com/articleView?id=mc_ctc_track_cart.htm&type=5).

{% include gist.html sectionId="trackcart" names="Obj-C,Swift" gists="https://gist.github.com/55cb5aca932689cf9e2935c6980beabe.js,https://gist.github.com/0f6d9da815f4799dccdeb4fce13bf77c.js" %}

#### Track Conversion

To track a purchase made through your mobile app, use the method shown in the example. For more information about this method’s general use with Personalization Builder, review [Track Purchase Details](https://help.salesforce.com/articleView?id=mc_ctc_track_conversion.htm&type=5).

{% include gist.html sectionId="trackconversion" names="Obj-C,Swift" gists="https://gist.github.com/6e9ed834a2645463f267ac1c497bb611.js,https://gist.github.com/2e0a5c806024da20f4b0abfc77d05957.js" %}

#### Track Page Views

To implement page-view analytics in your app, use the method shown in the example. For more information about this method’s general use with Personalization Builder, review [Track Items Viewed](https://help.salesforce.com/articleView?id=mc_ctc_track_page_view.htm&type=5).

{% include gist.html sectionId="trackpageviews" names="Obj-C,Swift" gists="https://gist.github.com/e605564bd235b85255b9c1460f84a8b7.js,https://gist.github.com/63511dd483bd521dbeb3b46fbece001a.js" %}

### Related Items
* _MarketingCloudSDK+Intelligence.h_
