# Footer
<hr/>
The footer allows you to insert various kinds of contact information.

![](footer.png)

Each element within the footer requires user information to be included within the custom element of the `site.xml`. This page will outline each option. The current design splits the footer into two vertical columns. The left side contains contact information, while the right contains social media, copyright and powered by sections.

## Contact Section

The Contact section, allows you to define various electronic and physical contact methods.  Not all sections need to be completed, the system will simply skip empty blocks. Below is an example 

```xml
<project name="xxx">
  [...]
  <custom>
    <bootstrapSkin>
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
    </bootstrapSkin>
  </custom>
  [...]
</project>
```

## Social Media

The Social Media bar places the brand icon (from bootstrap-icons) into a singular line with a link to the supplied account, allowing organisations to provide this information in a way which does not link information to external services.

### Bitbucket

Bitbucket is one of several source control management solutions supported in the media bar, the Bitbucket element has 2 attributes, `project` and `repository`. `project` is the Bitbucket user/organisation to whom the repository belongs, while `repository` is the Bitbucket repository name. The skin will use this to build

```xml
<project name="xxx">
  [...]
  <custom>
    <bootstrapSkin>
        <gitHub>
            <project>stevecrox</project>
            <repository>maven-site-bootstrap-skin</repository>
        </gitHub>
    </bootstrapSkin>
  </custom>
  [...]
</project>
```

### GitHub

Github is one of several source control management solutions supported in the media bar, the Github element has 2 attributes, `organisation` and `repository`. `organisation` is the Github user/organisation to whom the repository belongs, while `repository` is the Github repository name. The skin will use this to build

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

GitLab is one of several source control management solutions supported in the media bar, the GitLab element has 2 attributes, `project` and `repository`. `GitLab` is the GitLab user/organisation to whom the repository belongs, while `repository` is the GitLab repository name. The skin will use this to build

```xml
<project name="xxx">
    [...]
    <custom>
        <bootstrapSkin>
            <gitHub>
                <project>stevecrox</project>
                <repository>maven-site-bootstrap-skin</repository>
            </gitHub>
        </bootstrapSkin>
    </custom>
    [...]
</project>
```