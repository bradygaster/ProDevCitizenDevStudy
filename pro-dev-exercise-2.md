# Pro Dev Exercise 2

This entire exercise will be performed within the Microsoft Edge browser, which is available via an icon on the virtual machine's desktop.

## Exercise 2: Import the API into Azure API Management

1. Copy the URL from the `swagger.json` browser tab to the clipboard (https://study-baseline-app.azurewebsites.net/swagger/v1/swagger.json, in case you closed it).
1. Click the **Microsoft Azure** favorite button on the browser toolbar.
1. Click the **study-apis** API Management service link in the Azure portal.
1. Click the **APIs** navigation bar item.
1. Click the **Add API* button.
1. Click the **OpenAPI** button. This will launch the Open API (Swagger) import process.
1. Paste the URL you copied in step 1 into the **OpenAPI specification** textbox.
1. Type `weather/v1` into the **API URL suffix** textbox.

    > One benefit of Azure API Management is being able to specify a version for an API, then to leave that underlying API alone as you extend the HTTP API. As updates are deployed, additional versions can be imported into API Management and provided to your API's customers via versioned URLs.

1. Click the **Create** button.
1. In the **All operations** list, click the `/WeatherForecast - GET` operation.
1. Click the **Settings** navigation menu item.
1. Paste in the Base URL for the Swagger URL you copied earlier, https://study-baseline-app.azurewebsites.net, into the **Web service URL** textbox.

    > This sets the Weather API's Base URL property. Since API Management serves as a front-end to any multiple back-end HTTP APIs, you may hit multiple back-end services that are proxied by a single API Management front end. For this reason you need to configure API Management to know how to find your back-end service.

1. Click the **Save** button to save the change.
1. Click the **Test** navigation link.
1. Click the `/WeatherForecast - GET` operation.
1. Click the **Send** button to test the API responds through the API Management proxy.
1. Leave the browser open on the API test page.

---

Continue on to [Exercise 2 Discussion](pro-dev-exercise-2-discussion.md)