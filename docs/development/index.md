# Contribute
<hr/>
Contributions via GitHub pull requests are gladly accepted from their original author. Along with any pull requests, please state that the contribution is your original work and that you license the work to the project under the project's open source license. Whether or not you state this explicitly, by submitting any copyrighted material via pull request, email, or other means you agree to license the material under the project's open source license and warrant that you have the legal authority to do so.

## Compiling

You can compile the project with a local instance of Maven (3.x or later) or with Maven Wrapper. You will need Java 1.8 or later to compile the application.

### Maven

```bash
$ mvn clean install site site:stage
```

### Maven Wrapper

```bash
$ ./mvnw clean install site site:stage
```

### Notes

The project `io.github.stevecrox.maven.skins:bootstrap-site-skin-parent` contains the actual skin (under `src/main/resources/META-INF/maven`). The modules under the 'io.github.stevecrox.maven.skins.example:bootstrap-site-skin-example-parent' are used to test various layouts and configurations. For those modules to build you need to have packaged `io.github.stevecrox.maven.skins:bootstrap-site-skin-parent` and installed it into the local repository. This is achieved by the 'clean install' step of the command, the `site` command ensures each module builds its own site, the use of `site:stage' tells Maven to pull in the child module sites into the root parent pom. This allows you to access thc combined results under `target/staging/bootstrap-site-skin-parent' I would then look at each Layout option to gain an understanding of how your change has affected the skin. 

You will note the parent projects `site.xml` uses an older version of the plugin (typically a release). This is because when pacakging a parent POM, maven starts the site phase before it completes the child module package phase, at this point an instance of the skin doesn't exist and so we can't use the current skin version at this level.

## Issues

Please report any bugs found, feature requests or other issues on [maven-site-bootstrap-skin issue tracker](https://github.com/stevecrox/maven-site-bootstrap-skin/issues).

## Submitting Changes

To submit a bug fix, ensure there is an issue raised on the issue track and create a fork of the project, resolve the issue within a branch and then raise a pull request against the project. When submitting a Pull Request please follow these guidelines:

* Create a fork of the [maven-site-bootstrap-skin](https://github.com/stevecrox/maven-site-bootstrap-skin) project
* Create a feature branch associated with an issue on the [maven-site-bootstrap-skin issue tracker](https://github.com/stevecrox/maven-site-bootstrap-skin/issues). 
* Ensure the feature branch is based on `main`. 
* Push your changes to the feature branch in your fork of the repository.
* Respect the original code style: by using the same codestyle, patches should only highlight the actual difference, not being disturbed by any formatting issues:
** Only use spaces for indentation.
** Create minimal diffs - disable on save actions like reformat source code or organize imports. If you feel the source code should be reformatted, create a separate PR for this change.
** Check for unnecessary whitespace with git diff --check before committing.

## License

Licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0) (the "License"); you may not use this work except in compliance with the License. You may obtain a copy of the License in the LICENSE file, or at:

