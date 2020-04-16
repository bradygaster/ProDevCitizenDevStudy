# Citzen Dev Exercise 1

This entire exercise will be performed within the Microsoft Edge browser, which is available via an icon on the virtual machine's desktop.

## Exercise 1: Create a Custom Connector

1. Hold down the CTRL button and click the **Power Apps** favorite icon to open the Microsoft Power Apps portal.
1. Expand the **Data** node in the navigation bar.
1. Click the **Custom Connectors** node in the navigation bar.
1. Click the **New custom connector** menu button.
1. Select the **Import an OpenAPI file** menu option.
1. Type `Weather API` in the **Connector name** textbox.
1. Click the **Import** button.
1. Select the local file in the **Downloads** folder named `Weather API.swagger.json`.
1. Click the **Continue** button.
1. Provide the host name `study-apis.azure-api.net` in the **Host** textbox.

    > The OpenAPI file doesn't contain the host name of the API, to enable multiple environments. In our case, the HTTP API has been imported into Azure API Management, so we'll use the host name of the API Mamangement instance.

1. Click the **Security** link at the bottom of the page.
1. Make sure **API Key** is selected.

    > As mentioned earlier, the HTTP API this Custom Connector will use is managed by Azure API Management. API Management authenticates using a Subscription ID that will be provided to you later in the exercise.

1. Click the **Definition** link at the bottom of the page.
1. Rename the **Operation ID** from `get-weatherforecast` to `GetWeatherForecast`.
1. Click the **Create connector** link at the top of the wizard.
1. Click the **Close** link at the top of the wizard.
1. Verify the **Weather API** Custom Connector has been created and appears in the list.

---

Continue on to [Exercise 1 Discussion](exercise-1-discussion.md)
