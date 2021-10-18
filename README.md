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

<table>
    <thead>
        <tr>
            <th colspan="2">The table header</th>
        </tr>
    </thead>
    <tbody>
        <tr>
          <td>Area</td>
          <td>Salesforce Functions</td>
          <td>Azure Functions</td>
          <td>Comment</td>
        </tr>
        <tr>
          <td>Product access</td>
          <td>Contact your Account Executive</td>
          <td>Signup online anytime</td>
          <td>You can use Microsoft Azure anytime. Salesforce requires an account level conversation.</td>
        </tr>
        <tr>
          <td>Tools</td>
          <td>VS Code + Docker Desktop</td>
          <td>VS Studio or VS Codes</td>
          <td>Salesforce uses Docker Desktop for running Functions locally. This now requires licensing Docker for most customers.</td>
        </tr>
        <tr>
          <td>Usage</td>
          <td>Functions restricted to Salesforce platform (probably)</td>
          <td>Azure Functions can be invoked from anywhere</td>
          <td>It could be an advantage with Azure to abstract your functions from the Salesforce platform and reuse them elsewhere.</td>
        </tr>
        <tr>
          <td>Skills</td>
          <td>Salesforce Functions</td>
          <td>Azure Functions</td>
          <td>Comment</td>
        </tr>
        <tr>
          <td>API</td>
          <td>Salesforce Functions have in-built platform API's</td>
          <td>Azure Functions can access Salesforce using the SOAP or REST API</td>
          <td>Salesforce has the advantage</td>
        </tr>
    </tbody>
</table>
