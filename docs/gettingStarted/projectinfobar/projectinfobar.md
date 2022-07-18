# Project Information Bar
<hr/>

The Project Information Bar is a navigation bar which contains the information found on traditional Apache Site Layouts, this includes 'Breadcrumbs', the publish date of the documentation and the version of software published.

![](projectinfobar.png)

## Breadcrumbs

Breadcrumbs will be placed in the Project Bar.

![](breadcrumbs.png)

This can be implemented by adding breadcrumb definitions to the `site.xml`.
```xml
  <project name="xxx">
    <breadcrumbs>
        <item name=.. href=.. img=.. position=.. alt=.. border=.. width=.. height=.. target=.. title=.. />
    </breadcrumbs>
  </project>
```

### Enable/Disable Breadcrumbs

```xml
  <project name="xxx">
    <custom>
      <bootstrapSkin>
        <projectbar>
          <skipBreadcrumb>true</skipBreadcrumb>
        </projectbar>
      </bootstrapSkin>
    </custom>
  </project>
```

### Enable/Disable Last Published Date

You can toggle the display of the Last Publish Date by setting the `skipGenerationDate` value within the configuration.  

```xml
  <project name="xxx">
    <custom>
      <bootstrapSkin>
        <projectbar>
          <skipGenerationDate>true</skipGenerationDate>
        </projectbar>
      </bootstrapSkin>
    </custom>
  </project>
```

### Last Publish Date Format

You are able to modify the display properties for the date publish, the default value is: `yyyy-MM-dd`. 

```xml
  <project name="xxx">
    <publishDate format="" />
  </project>
```

### Enable/Disable Last Published Version
You can toggle the display of the Last Publish Version by setting the `skipGenerationVersion` value within the configuration.

```xml
  <project name="xxx">
    <custom>
      <bootstrapSkin>
        <projectbar>
          <skipGenerationVersion>true</skipGenerationVersion>
        </projectbar>
      </bootstrapSkin>
    </custom>
  </project>
```