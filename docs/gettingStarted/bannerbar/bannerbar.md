# Banner Bar

Most Apache Maven sites have a 'banner' along the top this typically contains two icons referencing the Apache project and a proejct logo as shown below.
![](bannerbar.png)

The maven-site-plugin supports the definition of the icons using 'bannerLeft' and 'bannerRight' elements. Below is an example of these sections being defined within a `site.xml` file.

```xml
<project name="xxx">
    [...]
    <bannerLeft>
        <href>https://github.com/stevecrox/maven-site-bootstrap-skin</href>
        <border>0</border>
        <width>328px</width>
        <height>116px</height>
        <src>image/example-banner-left.png</src>
    </bannerLeft>

    <bannerRight>
        <href>https://github.com/stevecrox/maven-site-bootstrap-skin</href>
        <border>0</border>
        <width>256px</width>
        <height>125px</height>
        <src>image/example-banner-right.png</src>
    </bannerRight>
    [...]
</project>
```

The attributes of these elements should match the attributes of an `<img>` element within HTML. The skin will extract these values and create a floating container at the top of the page and populate images with the information provided. 

If these sections are left blank then no banner is added to the page, as a minimum the banner requires a `alt` or `src` attribute for something to be displayed. 