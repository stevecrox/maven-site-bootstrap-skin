# Theming
<hr/>

The Bootstrap default theme is used unless either a Bootswatch theme is specified or a `css/maven-theme.css` file has been included within the site resources. Below is an example of adding the [darkly bootswatch theme](https://bootswatch.com/darkly/) to the site.


## BootSwatch Theming

[Bootswatch](https://bootswatch.com/) is a website which hosts a variety of themes for Bootstrap. To use you need to define the desired style within the custom configuration. The value is based on the name of the theme for example.

```xml
    <project name="xxx">
      [...]
      <custom>
        <bootstrapSkin>
          <bootswatchStyle>darkly</bootswatchStyle>
        </bootstrapSkin>
      </custom>
      [...]
    </project>
```

## CSS

The skin includes a hook for two additional CSS files:
* `css/maven-theme.css`
* `css/site.css`

When building a Maven Site if you place a file with these names under the following folder structure the Maven site Plugin will incorporate them into the result.
```json
+- src/
   +- site/
      +- resources/
         +- css/
            +- maven-theme.css
            +- site.css
```