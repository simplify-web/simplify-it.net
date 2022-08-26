## deployment to github pages with custom domain name

### prepare github repo
- create empty repo in your github account
- clone repo from github with git url (to use ssh keys)
- cd newRepo


### Hugo (https://gohugo.io/getting-started/quick-start/)
- create new hugo site in current dir
`hugo new site .`
. add theme 
`git submodule add https://github.com/janraasch/hugo-scroll.git themes/hugo-scroll`
- cp example content
`cp -r themes/hugo-scroll/exampleSite/* .`
- start hugo server on all interfaces
`hugo serve -D --bind 0.0.0.0`

### configure github pages
- go to Settings/Pages
- Under “Build and deployment”, under “Source”, select GitHub Actions.
- choose Hugo template
- commit workflow to .github/workflows/pages.yml

### configure DNS
- create CNAME to point to: simplify-web.github.io (NOT the repo path)
- add Custom Domain to github: e.g. test.simplify-it.net
- wait... (could be 1/2 h), leave the github page alone, really
- 

### create favicon
- https://realfavicongenerator.net/
- 