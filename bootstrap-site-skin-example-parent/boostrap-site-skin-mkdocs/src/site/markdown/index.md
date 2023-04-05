This page tries to mimic the look and feel of the [MKDocs homepage|https://www.mkdocs.org]. Below the render tests are instructions on how this look was created.

## Markdown Render Tests

The below sections are provided to test various Markdown elements have translated correctly into a maven site.

### Code Example
Below is some embedded JSON to confirm the prettify plugin is working as expected.

```json
{  
  "first name": "Joe",
  "surname": "Bloggs",
  "age":  "26"
}
```
### Table Example
A simple table to confirm this is rendering correctly.

| first name | surname | age |
|------------| ------- | --- |
| Joe        | Bloggs  | 26  |

### Emphasis

I just love **bold text** using stars, if we use a single star we create *italic text* and similarly _one underscore_ should work.

When we ***use three stars*** it becomes bold and italic, similarly ___three underscores___ should work

### Blockquotes

Blockquotes can contain multiple paragraphs. Add a > on the blank lines between the paragraphs.

> This skin is the best thing ever invented and I include toast in that statement
> ...
> Well maybe toast is better
>> This line should be nested

### Lists
Below is an ordered list:
1. Bread
2. Toaster
3. Butter

This list is unordered:
* Dance All Night
* To the

  Best Song Ever (Best song ever should be indented and attached to bullet 2)
* And I think it went Oh oh oh!

## Configuration

The following sections identify the various custom settings used within the site.xml and explains what we expect to result on the page.

## CSS Theming

We have added an image (taken from the MKDocs home page) and set the following in the maven-theme.css so the background grid from the MKDocs home page is displayed.

```json
body {
  background: url(../image/grid.png) repeat-x;
}
```

The theme of the site has been set to [Cerulean|https://bootswatch.com/cerulean/] and we have to modify the Navbar style to get a blue theme in the Navbar to replicate the mkdocs look.
```xml
<custom>
  <bootstrapSkin>
    <bootswatchStyle>cerulean</bootswatchStyle>
  </bootstrapSkin>
</custom>
```

### Navbar

The Navbar is enabled links back to this page. You will notice that the menu links in the Navbar are normally weighted to the right of the Navbar the `menuOrientation` field here should move the menu so it sits next to the brand in the center. Sub menu overlays should be adjusted to appear on the right on the menu dropdown.
The theme of the site has been set to [Cerulean|https://bootswatch.com/cerulean/] and we have to modify the Navbar style to get a blue theme in the Navbar to replicate the mkdocs look.

```xml
<custom>
  <bootstrapSkin>
    <navbar>
      <enabled>true</enabled>
      <menuOrientation>center</menuOrientation>
      <style>navbar-dark bg-primary</style>
    </navbar>
  </bootstrapSkin>
</custom>
```

### Project Bar
The following sections turn of all elements found within the 'project bar' this means no bread crumb release version or publish date is displayed. This should make the project bar invisible. 
```xml
<publishDate position="none"/>
<version position="none"/>
<custom>
  <bootstrapSkin>
    <projectbar>
      <skipBreadcrumb>true</skipBreadcrumb>
    </projectbar>
  </bootstrapSkin>
</custom>
```

### Footer Elements

The sections below relate to configuration of the page footer.

#### Theming

We have modified the Bootstrap classes associated with the footer from the default to recreate the look of Mk Docs.

```xml
<project name="xxx">
  [...]
  <custom>
    <bootstrapSkin>
      <footer>
        <style>footer mt-auto py-4 bg-light text-dark</style>
      </footer>
    </bootstrapSkin>
  </custom>
</project>
```

#### GitHub
Github is one of several source control management solutions supported in the media bar, the Github element has 2 attributes, organisation and repository. organisation is the Github user/organisation to whom the repository belongs, while repository is the Github repository name. The skin will use this to build the URL with the path https://github.com/stevecrox/maven-site-bootstrap-skin
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

#### Twitter
I have added a Twitter element to ensure the footer has some content and the icon should appear on the right side of the footer. This will create the url `https://twitter.com/stevecrox0914`

```xml
<project name="xxx">
  [...]
  <custom>
    <bootstrapSkin>
      <twitter>
        <accountId>stevecrox0914</accountId>
      </twitter>
    </bootstrapSkin>
  </custom>
  [...]
</project>
```