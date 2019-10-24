# List a Project

This document outlines the process of submitting a project to be listed on Up
for Grabs.

## Criteria

We are interested in active open source projects that meet this criteria:

- available maintainers who are interested in guiding new contributors
- the project curates a list of small tasks which are ideal for new contributors
- maintainers are happy and willing to review and work with new contributors to
  help them learn more about open source

If your project does not satisfy all of this criteria, it may be declined at the
review process. We'll provide suggestions to help address these things so that
it may be listed in the future.

## Using the GitHub web editor

The simplest way to add your project is to use the GitHub web editor. If you are
signed into GitHub, simply navigate to [this link](https://github.com/up-for-grabs/up-for-grabs.net/tree/gh-pages/_data/projects)
to view the list of projects.

<img width="1013" src="https://user-images.githubusercontent.com/359239/67146649-90691280-f263-11e9-9d3f-d63c79f8e872.png">

In the header click the "Create new file" link in the header to start the
process, which will open the web editor with an empty file:

<img width="1009" src="https://user-images.githubusercontent.com/359239/67146648-90691280-f263-11e9-9599-8bd50ff8769b.png">

Ensure that you name the file after your project, and that the file extension is
`.yml`.

<img width="582" src="https://user-images.githubusercontent.com/359239/67146647-8fd07c00-f263-11e9-97f0-3ecd71521903.png">

Copy and paste this template as the contents of the file, and then change the
default values to add details specific to the project:

```yaml
name: Your Project Name Here
desc: A brief description of the project
site: https://example.org/your-project-link-here
tags:
  - tags
  - relevant
  - to
  - the
  - project
upforgrabs:
  name: up for grabs
  link: https://github.com/username/project/labels/up%20for%20grabs
```

Ensure that your `tags` entries are all lower-case, do not contain spaces, and
use this subset of characters: `a-z`,`0-9`,`+`,`#`,`.`,`-`, This will be checked
as part of the pull request review, so don't stress too much about it here.

The `upforgrabs` section may be unfamiliar to you, but it's the important part
of what gets shown on our site. This consists of two entries which are relevant
to the list of issues the project has available for new contributors:

- the `name` being the label assigned to these issues
- the `link` is the URL to navigate to that list of issues

We leverage GitHub integration on the site to provide more information about the
project leveraging the GitHub API, but we accept any link here as long as it
points to a list of issues.

If you're not sure what to provide, here are some examples of other projects
that are listed:

- [Giraffe](https://github.com/up-for-grabs/up-for-grabs.net/blob/gh-pages/_data/projects/Giraffe.yml)
- [.NET Core CLR](https://github.com/up-for-grabs/up-for-grabs.net/blob/gh-pages/_data/projects/dotnet-core-clr.yml)
- [Rust](https://github.com/up-for-grabs/up-for-grabs.net/blob/gh-pages/_data/projects/rust.yml)
- [the Up for Grabs project itself](https://github.com/up-for-grabs/up-for-grabs.net/blob/gh-pages/_data/projects/up-for-grabs.net.yml)

You might have noticed the `stats` fields in the links above. Those are not
included in the template because they are generated by automated tooling which
queries the GitHub API - you don't need to include this when first submitting
the project.

When you have completed the project details, use the form at the bottom of the
page to create the commit:

<img width="1016" src="https://user-images.githubusercontent.com/359239/67146646-8fd07c00-f263-11e9-8330-4ddb7b036e1d.png">

The next page will show you the changes made - click "Create pull request" to
start creating the pull request:

<img width="1015" src="https://user-images.githubusercontent.com/359239/67146645-8fd07c00-f263-11e9-8bcb-bf9b2640bb53.png">

Fill out the Pull request template to add anything else, and then click
"Create pull request" to submit it for review:

<img width="1027" src="https://user-images.githubusercontent.com/359239/67146644-8fd07c00-f263-11e9-9615-b2e6665d3018.png">

## Use the Yeoman Generator

If you'd like to use a generator to create the project's file, you can certainly
do so!

Install the generator, then run it and walk through the steps:

```
npm install -g generator-up-for-grabs
yo up-for-grabs
```

## Pull Request Reviews

We aim to be responsive when a pull request is open, but if a pull request
remains idle for 2 weeks with feedback that prevents us from merging it we will
close the pull request. You are welcome to resubmit the project and address the
feedback provided.