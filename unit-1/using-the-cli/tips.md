# Tips and Tricks

## Getting Help
To see a verbose list of available commands:
```shell
ng help
```

## Autocompletion
You can turn on autocompletion within your shell.  Instructions for bash, zsh, and gitbash:

### bash
```shell
ng completion --bash >> ~/.bashrc
source ~/.bashrc
```
## zsh
```shell
ng completion --zsh >> ~/.zshrc
source ~/.zshr
```
## gitbash
```shell
ng completion --bash >> ~/.bash_profile
source ~/.bash_profile
```

Now, type in `ng` + SPACE, then hit TAB twice to see a quick list of base commands.  
```shell
--version   -v          b           build       completion  doc         e           e2e         eject       g           generate    get         help        l           lint        n           new         s           serve       server      set         t           test        v           version     xi18n
```

For viewing command line options for a given commands, type in `ng g -`, then hit TAB twice to see a quick list of command line options for `generate`:
```shell
--app         --collection  --dry-run     --force       --lint-fix    -a            -c            -d            -f            -lf
```

## Pulling up the Documentation
From the command line, you can pull up the Angular Documentation:
```shell
ng doc KEYWORD
```
This will open the Angular Documentation in a new tab, using the `KEYWORD` to filter the results.

## Autoformat Code
To autoformat your code to fit within the clang-format, simply:
```shell
ng format
```
It would be wise to commit all changes before running this command for easily reversing the formatting.

## Deploy to GitHub Pages
To build the production application, create a github repository, and publish the application:
```shell
ng github-pages:deploy
```

## Version Information
To get the version information of the CLI and the Angular Components (as well as Node, TypeScript, and OS versions):
```shell
ng version
```