# hugo Resume

Created from [Start Bootstrap - Resume](https://startbootstrap.com/template-overviews/resume/).

This is basically a single-page website with auto-scrolling based on left-hand nav.  Dedicated project/publications pages allow more detail.  Includes a client-side search powered by fuse.js at '/search' but currently theme does not link to that anywhere.

<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [hugo Resume](#hugo-resume)
	- [Examples](#examples)
	- [Setup & Use](#setup-use)
		- [Summary](#summary)
		- [Data files](#data-files)
		- [Projects](#projects)
		- [Publications](#publications)
		- [Template params](#template-params)
	- [Credits](#credits)
		- [Start Bootstrap Resume](#start-bootstrap-resume)

<!-- /TOC -->

## Examples

![About You](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/about.png)

![With optional Contact QR Code](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/qrcode.png)

![Highlight skills with dev icons](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/skills.png)

![List featured projects](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/projects.png)

![Searchable content](https://raw.githubusercontent.com/eddiewebb/hugo-resume/master/images/search.png)

See [Eddie's site](https://edwardawebb.com) for a live example.

## Setup & Use

This theme uses a combination of a custom archetype `projects` and some data files to drive content.

You can test the provided [exampleSite](exampleSite) after cloning with the command:
`cd exampleSite;hugo -t hugo-resume --themesDir ../.. server`

### Summary
Edit the main `contents/_index.md with a brief bio/summary`

### Data files
Data files are used for simple content presented on the homepage.

- [data/skills.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/skills.json)
- [data/experience.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/experience.json)
- [data/education.json](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/data/education.json)

### Projects
Initially projects were in their own JSON file too, but I decided I wanted to allow more detail and custom formatting.
Projects are added to one of 2 subfolders of `creations` or `contributions`. The difference indicates your role as originator or colaborator.   Use `hugo add projects/TYPE/name-of-project.md` to leverage the proper archetype.

### Publications
Similar to projects, create them under `publications`. Include any papers, speaking engagements, articles, etc.

### Template params

All personal information outside the above details is captured by params in [`config.toml`](https://github.com/eddiewebb/hugo-resume/blob/master/exampleSite/config.toml)

```
[params]
    firstName = "Eddie"
    lastName = "Webb"
    address = "Rollinsford, NH"
    phone = "1-555-555-1234"
    contactNote = "Dev Tools Engineer" #used in QR code only
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
    showQr = true

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

[outputs] #only required for search
    home = ["HTML", "JSON"]
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
