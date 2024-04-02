# Banner Bar
<hr/>
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

### Source Control Management (SCM)

As part of the Social Media bar you are able to include links to the project. The following configurations are supported.

### Git

There are a variety of Git endpoints not currently supported by Bootstrap Icons, for those we expect an 'endpoint' (hostname), the project and the repository.The skin will use this to build the URL with the path `https://bitbucket.com/<project>/<repository>`

```xml
<project name="xxx">
  [...]
  <custom>
    <bootstrapSkin>
        <git>
            <project>stevecrox</project>
            <repository>maven-site-bootstrap-skin</repository>
            <endpoint>http://bitbucket.com</endpoint>
        </git>
    </bootstrapSkin>
  </custom>
  [...]
</project>
```

### GitHub

Github is one of several source control management solutions supported in the media bar, the Github element has 2 attributes, `organisation` and `repository`. `organisation` is the Github user/organisation to whom the repository belongs, while `repository` is the Github repository name. The skin will use this to build the URL with the path `https://github.com/<organisation>/<repository>`

```xml
<project name="xxx">
  [...]
  <custom>
    <bootstrapSkin>
        <gitHub>
            <organisation>stevecrox</organisation>
            <repository>maven-site-bootstrap-skin</repository>
        </gitHub>
    </bootstrapSkin>
  </custom>
  [...]
</project>
```

### GitLab

GitLab is one of several source control management solutions supported in the media bar, the GitLab element has 2 attributes, `project` and `repository`. `GitLab` is the GitLab user/organisation to whom the repository belongs, while `repository` is the GitLab repository name. The skin will use this to build the URL with the path `https://gitlab.com/<project>/<repository>`

```xml
<project name="xxx">
    [...]
    <custom>
        <bootstrapSkin>
            <gitLab>
                <project>stevecrox</project>
                <repository>maven-site-bootstrap-skin</repository>
            </gitLab>
        </bootstrapSkin>
    </custom>
    [...]
</project>
```