# Heavily Configured Example

This example should enable all possible options and configure them on a single page, it also includes the ['Litera' Bootswatch theme](https://bootswatch.com/litera/).

The purpose of this theme is to allow us to demonstrate various capabilities of the skin to confirm nothing is obviously broken (and to also demonstrate what the skin can deliver.)

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