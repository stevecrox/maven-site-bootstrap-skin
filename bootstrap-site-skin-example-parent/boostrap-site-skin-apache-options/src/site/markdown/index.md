This example disabled the project information bar and aligns the Navbar links to the left to mimic a MkDocs layout, it also includes the ['SuperHero' Bootswatch theme](https://bootswatch.com/superhero/). The [Maven Default Skin](https://maven.apache.org/skins/maven-default-skin/sample/) link has been provided to compare with this skin.

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

### Footer Elements

The sections below relate to configuration of the page footer.

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