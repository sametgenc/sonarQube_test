#### Connecting to your project manually

If you already have a Kentico Kontent account, you can connect this sample application to a project of your own to access its unpublished content items, and track visitors on the site. For example, you can connect the application to your version of the Sample project.

1. In Kentico Kontent, choose Project settings from the app menu.
1. Under Development, choose API keys.

    * You will be copying the Project ID and API key for the Delivery Preview API.

1. Open the `\DancingGoat\Web.config` file.
1. Use the values from your Kentico Kontent project in the `Web.config` file:

    * **Project ID**: Insert your project ID into the `ProjectId` application setting.
    * **Delivery Preview API**: Create a new application setting named `PreviewApiKey` in the `<appSettings>` section, and use the Delivery Preview API key as its value. To enable calls over the Delivery Preview API, you also need to add a setting named `UsePreviewApi` and set it to `true`.

    ```xml
    <appSettings>
        ...
        <add key="ProjectId" value="YOUR_PROJECT_ID" />
        <add key="UsePreviewApi" value="true"/>
        <add key="PreviewApiKey" value="YOUR_DELIVERY_PREVIEW_API_KEY" />
        ...
    </appSettings>
    ```

1. Save the changes.
1. Run the application.

After you run the application, Kentico Kontent will track site visits and create new contacts when visitors submit a form. You will also be able to see all project content including the unpublished version of content items.

