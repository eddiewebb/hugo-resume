# Netlify CMS Support

This folder exposes an `/admin` page in your website that allows a CMS editor experience.

All changes are pushed to the GitHub repository (right to master, or via PR is configurable)

## Using on your site

1) Copy the full admin folder (this folder) from exampleSite within theme to the 'static' folder of you hugo site.
`cp -a PROJECT_DIRECTORY/themes/hugo-resume/admin PROJECT_DIRECTORY/static`
2) Edit `config.yml` (which includes hints) to reflect any changes you made to content structure, and also
	- Github Repository Path
	- Paths to images and content folders
