# Project Information Bar
<hr/>

The Project Information Bar is a navigation bar which contains the information found on traditional Apache Site Layouts, this includes 'Breadcrumbs', the publish date of the documentation and the version of software published.

![]()

## Breadcrumbs

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

## Last Published Date

### Enable/Disable Last Published Date
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

## Last Published Version

### Enable/Disable Last Published Version
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