This page tries to mimic the look and feel of the MKDocs homepage, 

## 

The purpose of this theme is to allow us to demonstrate various capabilities of the skin to confirm nothing is obviously broken (and to also demonstrate what the skin can deliver.)

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

### Navbar

The Navbar is enabled should contain a logo next to the brand which includes alternative text and links back to this page. You will notice that the menu links in the Navbar are normally weighted to the right of the Navbar the `menuOrientation` field here should move the menu so it sits next to the brand. Sub menu overlays should be adjusted to appear on the right on the menu dropdown.
```xml
<navbar>
  <enabled>true</enabled>
  <icon>
    <alt>alt text for example logo (for testing)</alt>
    <href>https://stevecrox.github.io/io.github.stevecrox.maven.skins/bootstrap-site-skin-parent</href>
    <src>image/example-logo.png</src>
  </icon>
  <menuOrientation>left</menuOrientation>
</navbar>
```

### Project Bar
The following configuration turns of the publish date and  publish version but allows the breadcrumbs to be displayed, this means we expect a project bar to be placed under the navigation bar. 
```xml
  <projectbar>
    <skipBreadcrumb>false</skipBreadcrumb>
    <skipGenerationDate>true</skipGenerationDate>
    <skipGenerationVersion>true</skipGenerationVersion>
  </projectbar>
```

### Side Bar
The page should contain a sidebar, originally this is to mimic the Maven layout, where all menu options should be listed in the sidebar in an expanded fashion.
```xml
  <sidebar>
    <enabled>true</enabled>
  </sidebar>
```

### Footer Elements

The sections below relate to configuration of the page footer.

#### Contact Details

On the left side of the footer we have allowed for contact information to be displayed on the page, we expect to see all of the elements outlined below.

```xml
  <contact>
    <email>bootstrap-skin@maven.sites.uk</email>
    <fax>01752 123456</fax>
    <mobile>07712345678</mobile>
    <landline>01752 987654</landline>
    <address>
      <line1>Postbox</line1>
      <line2>221B Baker Street</line2>
      <city>London</city>
      <county>London</county>
      <country>England</country>
      <post_code>NW1 6XE</post_code>
    </address>
  </contact>
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