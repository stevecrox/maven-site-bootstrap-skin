# Maven Site Bootstrap Skin

The Maven Site Bootstrap Skin is an Apache Maven site skin built on top of [Bootstrap 5](https://getbootstrap.com/docs/5.0/getting-started/introduction/). It allows you to supply a [Bootswatch Theme](https://bootswatch.com/) as a CSS file as well as other additional CSS.

Skin configurations have been provided to demonstrated the [default navbar layout](https://stevecrox.github.io/io.github.stevecrox/maven-site-bootstrap-skin-parent/boostrap-skin-navbar) and the [Apache standard layout](https://stevecrox.github.io/io.github.stevecrox/maven-site-bootstrap-skin-parent/boostrap-skin-apache-options).

## Usage

To use this skin in your project, use the skin element of the site.xml site descriptor:

```xml
    <project name="xxx">
      [...]
      <skin>
          <groupId>io.github.stevecrox</groupId>
          <artifactId>maven-site-bootstrap-skin-parent</artifactId>
          <version>1.0.0</version>
      </skin>
      [...]
    </project>
```



