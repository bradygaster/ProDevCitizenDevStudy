# Citizen Dev Exercise 2

This entire exercise will be performed within the Microsoft Edge browser, which is available via an icon on the virtual machine's desktop.

## Exercise 2: Build a Power App with the Custom Connector

1. Hold down the CTRL button and click the **Power Apps** favorite icon to open the Microsoft Power Apps portal.
1. Click the **Apps** navigation item.
1. Click the **New app** menu and select **Canvas** from the menu.
1. Select the **Phone layout** from the **Blank app** template.
1. Click the **Insert** menu item and add a **Gallery** component to the form, selecting the **Vertical** option from the fly-out menu.
1. Align the Gallery near the top of the form, with some room below it.
1. Click the **Insert** menu item and add a **Button** component to the form. Change the text of the Button to be **Refresh** and move the button below the Gallery.
1. Click the **Data sources** item in the app explorer on the left side of the designer.
1. Search for `Weather API` in the search box.
1. Select the `Weather API` Custom connector.
1. When asked for the API key, obtain it from the employees driving the study.
1. Paste in the API key and click the **Connect** button.
1. Click the Button and select the `OnSelect` property in the top-left portion of the designer.
1. Type the following formula into the formula bar:

    ```
    ClearCollect(ForecaseData,WeatherAPI.GetWeatherForecast())
    ```

    > This will result in a new Collection being created in your app named `ForecastData` to which the Gallery can be data-bound. It will then call the HTTP API and fill the entity with the results.

1. Validate that you have no errors and that the Data Sources in your app now contain a new Collection named `ForecastData`.
1. Click the Gallery in the designer.
1. When the **Select a data source** window appears, select the `ForecastData` Collection.
1. Change the **Layout** property to be **Title and subtitle** in the designer.
1. Click the **Edit** link to edit the **Fields** property in the designer.
1. Change the **subtitle** menu to select **temperatureC**.
1. Change the **title** menu to select **date**.
1. Run the Power App.
1. Click the Refresh button.
1. Validate that the form refreshes with data each time you click the Refresh button.

---

Continue on to [Exercise 2 Discussion](exercise-2-discussion.md)