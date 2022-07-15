# Getting Started

The aim of this skin is to make each aspect of the layout configuration but provide sane defaults so you can minimise the amount of configuration you need to provide

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

## Site Configuration

This skin supports a number of configuration options, allowing you to enable various Bootstrap components and configure them to meet your needs. The configuration is specified within the [`site.xml`](https://maven.apache.org/doxia/doxia-sitetools/doxia-decoration-model/decoration.html) using the `<custom><bootstrapSkin>` element. The following links provide information on various aspects of the skins.

* [Banner Bar Configuration](bannerbar/bannerbar.md)
* [Navbar Configuration](navbar/navbar.md)
* [Footer Configuration](footer.md)
* [Project Info Bar Configuration](projectinfobar.md)
* [Sidebar Configuration](sidebar.md)

## Theming
By default no theming is applied


## Responsive Design
All elements within the skin should follow responsive design using Bootstraps inherit Responsive design elements. The site layout is tested using the test widths the [bootstrap grid system](https://getbootstrap.com/docs/5.0/layout/grid/) specifies to confirm it scales correctly.

## Examples

The layout options are sites using different `site.xml` configurations, these are provided for testing purposes but should also be useful in identifying how you can use the tool. The Source code can be [found on github](https://github.com/stevecrox/maven-site-bootstrap-skin), you can find the site.xml files here:
* [Default Example](https://github.com/stevecrox/maven-site-bootstrap-skin/blob/main/bootstrap-site-skin-example-parent/boostrap-site-skin-navbar/src/site/site.xml)
* [Apache Image Layout Example](https://github.com/stevecrox/maven-site-bootstrap-skin/blob/main/bootstrap-site-skin-example-parent/boostrap-site-skin-apache-options/src/site/site.xml)
* [Kitchen Sink Example](https://github.com/stevecrox/maven-site-bootstrap-skin/blob/main/bootstrap-site-skin-example-parent/boostrap-site-skin-all-options/src/site/site.xml)
