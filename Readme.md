# deployment to github pages with custom domain name
- create empty repo in your github account
- clone repo from github with git url (to use ssh keys)
- cd newRepo


# Hugo (https://gohugo.io/getting-started/quick-start/)
- create new hugo site in current dir
`hugo new site .`
. add theme 
`git submodule add https://github.com/janraasch/hugo-scroll.git themes/hugo-scroll`
- cp example content
`cp -r themes/hugo-scroll/exampleSite/* .`
- start hugo server on all interfaces
`hugo serve -D --bind 0.0.0.0`