This example should enable all possible options and configure them on a single page, it also includes the [United Bootswatch theme](https://bootswatch.com/united/). The [Maven Default Skin](https://maven.apache.org/skins/maven-default-skin/sample/) link has been provided to compare with this skin.

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
    <href>https://stevecrox.github.io/io.github.stevecrox.maven.skins/bootstrap-site-skin-parent/bootstrap-site-skin-example-parent/boostrap-site-skin-all-options/index.html</href>
    <src>image/example-logo.png</src>
  </icon>
  <menuOrientation>left</menuOrientation>
</navbar>
```

### Project Bar
The following secctions turn of all elements found within the 'project bar' this means no bread crumb release version or publish date is displayed. This should make the project bar invisible. 
```xml
  <projectbar>
    <skipBreadcrumb>true</skipBreadcrumb>
    <skipGenerationDate>true</skipGenerationDate>
    <skipGenerationVersion>true</skipGenerationVersion>
  </projectbar>
```

### Github
I have added a Github element to ensure the footer has some content and the icon should appear on the right side of the footer.
```xml
  <gitHub>
    <projectId>stevecrox/maven-site-bootstrap-skin</projectId>
  </gitHub>
```

### Twitter
I have added a Twitter element to ensure the footer has some content and the icon should appear on the right side of the footer.
```xml
  <twitter>
    <accountId>stevecrox0914</accountId>
  </twitter>
```