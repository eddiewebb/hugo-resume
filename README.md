# hugo Resume

Created from [Start Bootstrap - Resume](https://startbootstrap.com/template-overviews/resume/).

This is basically a single-page website with auto-scrolling based on left-hand nav.  Dedicated project pages allowed more detail.

![Sample](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/about.png)

![Sample](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/skills.png)

![Sample](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/projects.png)

See [Eddie's site](https://edwardawebb.com) for a live example.

## Setup & Use

This theme uses a combination of a custom archetype `projects` and some data files to drive content.

You can test the provided [exampleSite](exampleSite) after cloning with the command: `cd exampleSite;hugo -t hugo-resume --themesDir ../.. server` and visiting localhost:1313 on your machine.

### Summary
Edit the main `contents/_index.md with a brief bio/summary`

### Data files
Data files are used for simple content presented on the homepage.

- [data/skills.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/skills.json)
- [data/contributions.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/contributions.json)
- [data/experience.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/experience.json)
- [data/education.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/education.json)
- [data/publications.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/publications.json)

### projects
Initially projects were in their own JSON file too, but I decided I wanted to allow more detail and custom formatting.
Projects are added with `hugo add projects/name-of-project.html`

### Template params

All personal information outside the above details is captured by params in [`config.toml`](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/config.toml)

```
[params]
    firstName = "Eddie"
    lastName = "Webb"
    address = "Rollinsford, NH"
    profileImage = "img/me.png"
    email = "email@domain.com"
    description = "Software Platform Engineer with experience leveraging agile, DevOps, and CI/CD to manage large scale distributed platforms both on prem and in public cloud."
    favicon = "images/favicon.ico"

    # what sections to display.  Setting to false disables navigation and section.
    showSkills = true
    showProjects = true
    showOpenSource = true
    showPublications = true
    showExperience = true
    showEducation = true

    # do you want to show git hash on page footer and link to repo? Add commit URl for repo here.
    gitCommitPrefix = "https://github.com/YOURNAME/REPONAME/commit/"


[[params.handles]]
    name = "LinkedIn"
    link = "https://www.linkedin.com/in/edwardwebb/"

[[params.handles]]
    name = "GitHub"
    link = "https://github.com/eddiewebb/"

[[params.handles]]
    name = "Bitbucket"
    link = "https://bitbucket.org/eddiewebb/"

[[params.handles]]
    name = "Stack Overflow"
    link = "https://stackoverflow.com/users/story/82880"
    icon = "stack-overflow" #optional icon attribute used for Font Awesome icons, otherwise the name is lowercased.

[[params.handles]]
    name = "Keybase"
    link = "https://keybase.io/edwardawebb"
    icon = "key" #optional icon attribute used for Font Awesome icons, otherwise the name is lowercased.

[params.google.analytics]
    trackerID = "XX-123446-01"


```

## Credits

This project ports the Start Bootstrap Resume theme by David Miller to support hugo.

### Start Bootstrap Resume

Start Bootstrap is an open source library of free Bootstrap templates and themes. All of the free templates and themes on Start Bootstrap are released under the MIT license, which means you can use them for any purpose, even for commercial projects.

* https://startbootstrap.com
* https://twitter.com/SBootstrap

Start Bootstrap was created by and is maintained by **[David Miller](http://davidmiller.io/)**, Owner of [Blackrock Digital](http://blackrockdigital.io/).

* http://davidmiller.io
* https://twitter.com/davidmillerskt
* https://github.com/davidtmiller

Start Bootstrap is based on the [Bootstrap](http://getbootstrap.com/) framework created by [Mark Otto](https://twitter.com/mdo) and [Jacob Thorton](https://twitter.com/fat).
