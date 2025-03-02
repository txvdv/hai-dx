# Contributing

## Install

1. Install git
2. [Install nvm](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating)
3. Clone and get into the repo 
   ```
   git clone https://github.com/txvdv/hai-dx
   cd hai-dx
   ```
4. Install/use Node and package dependencies
   ```
   nvm use
   npm install
   ```
   
## Contribute

### Trunk Based Development 

Helpful scripts to [commit straight to the trunk](https://trunkbaseddevelopment.com/styles/#committing-straight-to-the-trunk).

- Makes sure correct node version is used
   ```shell
   bin/env-check
   ```
- Git pull rebase running npm ci, calling env-check
   ```shell
   bin/tbd-pull
   ```
- Git push, calling tbd-pull and env-check
   ```shell
   bin/tbd-push
   ```

These are not required, but helpful for commit cadence. To use them:
1. Make those scripts executable:
   ```shell
   chmod +x bin/env-check
   chmod +x bin/tbd-pull
   chmod +x bin/tbd-push
   ```
2. Run them from the terminal depending on the situation
   ```shell
   bin/env-check
   ```
   ```shell
   bin/tbd-pull
   ```
   ```shell
   bin/tbd-push
   ```

To make these feel more git-like, you can add them as git [alias] commands
1. Add a `.gitconfig` file at the root folder and chose your own aliases:
   ```txt
   [alias]
   shipit = "!sh bin/tbd-push"
   ```
2. Configure your local repo copy to use the .gitconfig
   ```shell
   git config --local include.path ../.gitconfig
   ```

## References
- [Beginners Intro to Trunk Based Development](https://dev.to/jonlauridsen/beginners-intro-to-trunk-based-development-3158)
- [Practical Guide to Trunk Based Development](https://dev.to/jonlauridsen/practical-guide-to-trunk-based-development-1hlj)

## Resources
- [Trunk Based Development](https://trunkbaseddevelopment.com/)
- [Git Alias](https://github.com/GitAlias/gitalias) for some other helpful git aliases
