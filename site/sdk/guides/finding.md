---
layout: sdk
title: Finding
pagination:
  prev:
    url: configuring
    title: Configuring the SDK
  next:
    url: trading
    title: Trading
---
This guide provides details for using the eBay SDK for PHP with the [Finding](http://developer.ebay.com/Devzone/finding/Concepts/FindingAPIGuide.html) service in your projects.

## Installation

As mentioned in the [installation guide](/sdk/guides/installation.html), Composer is used to install the SDK and so you need to add `dts/ebay-sdk-finding` as a dependency in your project's composer.json file.

```javascript
{
    "require": {
        "dts/ebay-sdk-finding": "~0.0.0"
    }
}
```

### Versions

The SDK uses its own [Semantic Versioning](http://semver.org/) number, and it should be noted that it does not follow the numbers used by the service as they are maintained separately by eBay.

Using the above method will install a version of the SDK that is compatiable with the current API version. If you need to support a different version of the API there is a [list of SDK versions, and the API version they support](/sdk/guides/versions.html#finding) available. If during the development of your project you want to keep up with the latest changes you can specify `dev-master` as the version.

```javascript
{
    "require": {
        "dts/ebay-sdk-finding": "dev-master"
    }
}
```

## Namespaces

## Configuration

| Option     | Required | Description |
|:-----------|:--------:|:------------|
| apiVersion | No       | The API version supported by your application. A list of API version numbers can be found in the [release notes](http://developer.ebay.com/DevZone/finding/ReleaseNotes.html) for the Finding service. |
| appId      | Yes      | Your application ID, as explained in the [application keys guide](/sdk/guides/application_keys.html). |
| globalId   | No       | The unique string identifier for the eBay site your API requests are to be sent to. For example, you would pass the value EBAY-US to specify the eBay US site. A [complete list of eBay global IDs](http://developer.ebay.com/devzone/finding/Concepts/SiteIDToGlobalID.html) is available. |