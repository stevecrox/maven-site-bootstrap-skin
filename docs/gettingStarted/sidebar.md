#Side Bar
<hr/>
By default the [sidebar](https://getbootstrap.com/docs/5.2/examples/sidebars/) is disabled, it is included as one of the goals of the skin was to support the Maven 2 general layout which placed the navigation menu on the screen as a sidebar. This section will outline the configuration options offered by the sidebar.

## Enable/Disable the side bar
The skin allows you to disable or enable the sidebar by setting a custom element, as shown below:
```xml
<project name="xxx">
    [...]
    <custom>
      <bootstrapSkin>
        <sidebar>
          <enabled>true</enabled>
        </sidebar>
      </bootstrapSkin>
    </custom>
    [...]
</project>
```

## Sidebar Bar Style
You can configure the CSS classes used on the sidebar. Bootstrap 5 contains a number of classes for common colouring, by default 'navbar-dark bg-dark' has been set as this provides a clear contrast between the banner and the main text.
```xml
<project name="xxx">
    [...]
    <custom>
      <bootstrapSkin>
        <sidebar>
          <style>navbar-light bg-light</style>
        </sidebar>
      </bootstrapSkin>
    </custom>
    [...]
</project>
```
The above configuration would change the NavBar to look like the following