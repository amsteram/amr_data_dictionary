## Git integration with R studio

You can create an instance by using `usethis` package which helps to generate a personalised token that you can use to link your repo to github.
```sh
library("usethis")
usethis::create_github_token() #helps to create a personal access token
```
After running this, you will get a prompt to set the token detail and copy it. Back this up!

- Then run the `gitcreds::gitcreds_set()` in the link provided in the console and provide the necessary token.
- *Note* if there is a problem when you try to do this, try and find where your git.exe file is (run  `where git` for Windows or `which git` for MacOS) to find where your git is running from.
- When you find this, then go to Global Options in R studio and set that as the path for your git. that should fix it

After that, run the `use_github` package to link your repository and that should work
usethis::use_github()
