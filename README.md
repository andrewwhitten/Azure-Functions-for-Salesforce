# Azure-Functions-for-Salesforce

This project was driven by the desire to extend Salesforce with functions for use cases that the platform Apex language is generally too limited for. Salesforce did release a similar Functions framework in Winter '22, however I was unfortunately unable to get access. Microsoft on the other hand provides free trial to most Azure services just by signing up, and fairly clear pricing as well. So why wait?

I implemented the Quickstart Salesforce Function walkthrough in Microsoft Azure Functions instead, which you can deploy to Azure and insert an Account into Salesforce. This project will be regulary updated with new utilities than leverage the benefits of Functions in Salesforce:

<img width="962" alt="Screen Shot 2021-10-18 at 8 16 58 pm" src="https://user-images.githubusercontent.com/41508645/137705068-33accd28-32b2-4c92-9062-f82d94ab8e5c.png">


Comparing Microsoft Azure functions with Salesforce you can see multiple benefits that are worth considering:


<table>
    <thead>
        <tr>
          <th>Area</th>
          <th>Salesforce Functions (Winter '22)</th>
          <th>Azure Functions (4.x)</th>
          <th>Comments</th>
        </tr>
    </thead>
    <tbody>
        <tr>
          <td>Product access</td>
          <td>Contact your Account Executive</td>
          <td>Signup online anytime</td>
          <td>You can use Microsoft Azure anytime. Salesforce requires an account level conversation.</td>
        </tr>
        <tr>
          <td>Pricing</td>
          <td>Unknown. Contact your Account Executive</td>
          <td>Public calculator. First 1M executions free</td>
          <td>Azure pricing is known to be quite low, and dedicated plans can also be discussed with Microsoft. No public pricing from Salesforce to compare to.                </td>
        </tr>
        <tr>
          <td>Development Tools</td>
          <td>VS Code + Docker Desktop</td>
          <td>VS Studio or VS Code</td>
          <td>Salesforce uses Docker Desktop for running Functions locally. This now requires licensing Docker for most customers.</td>
        </tr>
        <tr>
          <td>Usage</td>
          <td>Functions restricted to Salesforce platform (probably)</td>
          <td>Azure Functions can be invoked from anywhere</td>
          <td>It could be an advantage with Azure to abstract your functions from the Salesforce platform and reuse them elsewhere.</td>
        </tr>
        <tr>
          <td>Languages</td>
          <td>Java, Typescript/Javascript</td>
          <td>C#, F#, Python, Java, Typescript/Javascript, Powershell</td>
          <td>Azure offers the widest range of options</td>
        </tr>
        <tr>
          <td>Skills</td>
          <td>New technology in the Salesforce suite, but training will be targeted at existing Salesforce developers</td>
          <td>Developers will need to pickup new Microsoft Azure skills.</td>
          <td>Salesforce has the advantage of having everything on one vendor platform.</td>
        </tr>
        <tr>
          <td>Salesforce API</td>
          <td>Salesforce Functions have in-built platform API's</td>
          <td>Azure Functions can access Salesforce using the SOAP or REST API</td>
          <td>Salesforce has the advantage of having an API tightly integrated with the Salesforce platform</td>
        </tr>
        <tr>
          <td>Platform maturity</td>
          <td>GA in 2021</td>
          <td>GA in 2007 - on version 4</td>
          <td>Microsoft functions is now quite a mature product, and the </td>
        </tr>
    </tbody>
</table>



Notes

* This is built in .NET 6 preview, just because the framework is planned for release this November 2021, and the performance aspects will be important for potential comparisons with other providers such as Amazon AWS and Google.
* There is a very specific bug when generating the .NET wrapper around the Salesforce Partner API. The simple fix is here: https://stackoverflow.com/questions/60976792/net-core-3-1-soap-platform-not-supported-error-compiling-jscript-csharp-script

