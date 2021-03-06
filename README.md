# Microsoft-Azure-Functions-for-Salesforce

This project was driven by the desire to extend Salesforce with scalable functions for use cases that the platform Apex language are generally too limited for. 

![func](https://user-images.githubusercontent.com/41508645/139773892-aedc919d-cacd-4887-ad3c-1a384a38f353.png)

Salesforce has releaseed a <A href="https://developer.salesforce.com/docs/platform/functions/overview">Functions framework in Winter '22</A>, however access to the product is difficult. Microsoft on the other hand provides free trial to most Azure services just by signing up, and with clear pricing as well. 

This is the Quickstart Salesforce Function walkthrough which you can deploy to Azure and:

* Insert an Account into Salesforce. 
* Check if a PDF file in Salesforce is password protected

This project will be regulary updated with new utilities than leverage the benefits of Functions in Salesforce:

<img width="962" alt="Screen Shot 2021-10-18 at 8 16 58 pm" src="https://user-images.githubusercontent.com/41508645/137705068-33accd28-32b2-4c92-9062-f82d94ab8e5c.png">

Comparing Microsoft Azure functions with Salesforce you can see multiple benefits that are worth considering:

<table>
    <thead>
        <tr>
          <th>Area</th>
           <th>Salesforce APEX</th>
          <th>Salesforce Functions (Winter '22)</th>
          <th>Microsoft Azure Functions (4.x)</th>
          <th>Comments</th>
        </tr>
    </thead>
    <tbody>
        <tr>
          <td>Product access</td>
          <td>Part of free Salesforce Developer Org</td>
          <td>Contact your Account Executive</td>
          <td>Signup online anytime</td>
          <td>You can use Microsoft Azure anytime. Salesforce requires an account level conversation.</td>
        </tr>
        <tr>
          <td>Pricing</td>
          <td>None (included with Salesforce ecept for most basic editions)</td>
          <td>Public pricing is USD $2,000 per org per month for 235k API calls, with increments of $45 for additional capacity on top of that.</td>
          <td>Public calculator. First 1M executions free. Salesforce API calls will cost extra if you exceed your standard limit.</td>
          <td>This is a very difficult comparison, and needs more investigation. On the face of it Azure is much cheaper, however you will also need to consider OPEX costs in maintaining it as well and current Salesforce API usage as well. For significant API usage then Salesforce Functions may well work out cheaper.</td>
        </tr>
        <tr>
          <td>Development Tools</td>
          <td>VS Code or Developer Console</td>
          <td>VS Code + Docker Desktop</td>
          <td>VS Studio or VS Code</td>
          <td>Salesforce uses Docker Desktop for running Functions locally. This now requires licensing Docker for most customers.</td>
        </tr>
        <tr>
          <td>Usage</td>
          <td>Anywhere</td>
          <td>Salesforce Functions can likely be invoked from anywhere (TBC)</td>
          <td>Azure Functions can be invoked from anywhere</td>
          <td>It could be an advantage with Azure to abstract your functions from the Salesforce platform and reuse them elsewhere.</td>
        </tr>
        <tr>
          <td>Languages</td>
          <td>Apex ('Java-like')
          <td>Java, Typescript/Javascript</td>
          <td>C#, F#, Python, Java, Typescript/Javascript, Powershell</td>
          <td>Azure offers the widest range of options</td>
        </tr>
        <tr>
          <td>Skills</td>
          <td>Simple Java knowledge</td
          <td>New technology in the Salesforce suite, but training will be targeted at existing Salesforce developers</td>
          <td>Developers will need to pickup new Microsoft Azure skills.</td>
          <td>Salesforce has the advantage of having everything on one vendor platform. It is challenging to find for Salesforce developers with Microsoft Azure skills.</td>
        </tr>
        <tr>
            <td>Memory limit</td>
            <td> 6MB (12 MB in some circumstances)</td>
            <td> 1GB </td>
            <td> 1.5GB (other plans can go up to 14GB) </td>
            <td> If your compute functions really need more than 1GB of memory, then you need to consider another option. I would imagine increasing this ammount is on the Salesforce roadmap. </td>
        <tr>
          <td>Salesforce API</td>
           <td>Built in</td>
          <td>Salesforce Functions have in-built platform API's</td>
          <td>Azure Functions can access Salesforce using the SOAP or REST API</td>
          <td>Salesforce has the advantage of having an API tightly integrated with the Salesforce platform</td>
        </tr>
        <tr>
          <td>Platform maturity</td>
          <td>GA 2006, and reliably used ever since</td>
          <td>GA in 2021 - Winter '22</td>
          <td>GA in 2017 - on version 4</td>
          <td>Microsoft functions is now quite a mature product, and Enterprise ready.</td>
        </tr>
    </tbody>
</table>

# Pre-requisites

* Salesforce Developer account (free) - https://developer.salesforce.com/signup
* Microsoft Visual Studio 2022 Community Edition - Preview (free) - https://visualstudio.microsoft.com/vs/preview/
* Microsoft Azure account (free) - https://azure.microsoft.com/en-us/free/ 

# Optional

* Postman (or similar API tool) - https://www.postman.com/

# Setup Steps

* Publish Function solution to Azure 
* Ensure the following Appliction Configuration settings for your Salesforce org are set:

<img width="913" alt="Screen Shot 2021-10-18 at 9 09 54 pm" src="https://user-images.githubusercontent.com/41508645/137711965-eb006a91-bb97-4331-be8c-6b3a3cf6196c.png">

# Notes

* This is built in .NET 6 preview, just because the framework is planned for release this November 2021, and the performance aspects will be important for potential comparisons with other providers such as Amazon AWS and Google.
* There is a very specific bug when generating the .NET wrapper around the Salesforce Partner API. The simple fix is here: https://stackoverflow.com/questions/60976792/net-core-3-1-soap-platform-not-supported-error-compiling-jscript-csharp-script
* I built this all on Windows 11. It should be possible on Mac OS with the same tools.

