The Maven Site Bootstrap Skin is an Apache Maven site skin built on top of [Bootstrap 5](https://getbootstrap.com/docs/5.0/getting-started/introduction/). It allows you to supply a [Bootswatch Theme](https://bootswatch.com/) as a CSS file as well as other additional CSS.

Skin configurations have been provided to demonstrated the [default navbar layout](https://stevecrox.github.io/io.github.stevecrox/maven-site-bootstrap-skin-parent/boostrap-skin-navbar) and the [Apache standard layout](https://stevecrox.github.io/io.github.stevecrox/maven-site-bootstrap-skin-parent/boostrap-skin-apache-options).

## HTML Examples

This page is provided as a means to test out the default site layout and check for obvious flaws in layout.

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

## Configuration 

This page has the following sections set within it.

### Navbar

We have limited navbar configuration to the icon elements href field, this should result in the `navbar-brand` element linking to the url within the href element.
```xml
  <navbar>
    <icon>
      <href>https://stevecrox.github.io/${project.groupId}/${project.artifactId}</href>
    </icon>
  </navbar>
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