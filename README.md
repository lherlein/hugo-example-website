# bs-dev-space Example

Currently unable to use github actions to host this

## How to run locally

1. Clone into local repo
2. npm i
3. Clone the 'learn' theme into the `themes/hugo-theme-learn` directory
    1. `mkdir themes/hugo-theme-learn`
    2. `git clone git@github.com:matcornic/hugo-theme-learn.git themes/hugo-theme-learn`
4. Copy the `theme-bscolors.css` file into the theme
    1. `cp layouts/css/theme-bscolors.css themes/hugo-theme-learn/static/css`
5. run `hugo server`
6. connect on the localhost port that terminal tells you
    1. most likely `localhost:1313`
