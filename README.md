# Azure-Functions-for-Salesforce

This project was driven by the desire to extend Salesforce with functions for use cases that the platform Apex language is generally too limited for. Salesforce did release a similar Functions framework in Winter '22, however I was unfortunately unable to get access. Microsoft on the other hand provides free trial to most Azure services just by signing up, and fairly clear pricing as well. So why wait?

Advantages of using Microsoft Azure functions with Salesforce are:


* Available for trial on demand
* Public pricing on website
* Mature cloud platform
* Decoupling

Notes

* This is built in .NET 6 preview, just because the framework is planned for release this November 2021, and the performance aspects will be important for potential comparisons with other providers such as Amazon AWS and Google.
* There is a very specific bug when generating the .NET wrapper around the Salesforce Partner API. The simple fix is here: https://stackoverflow.com/questions/60976792/net-core-3-1-soap-platform-not-supported-error-compiling-jscript-csharp-script
