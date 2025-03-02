# Hai Developer Experience

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

Helpful scripts to commit straight to the trunk.  
See below for references and the contributing docs for more links about TBD.

- Makes sure correct node version is used
   ```shell
   scripts/env-check
   ```
- Git pull rebase running npm ci, calling env-check
   ```shell
   scripts/tbd-pull
   ```
- Git push, calling tbd-pull and env-check
   ```shell
   scripts/tbd-push
   ```

These are not required, but helpful for commit cadence. To use them:
1. Make those scripts executable:
   ```shell
   chmod +x scripts/env-check
   chmod +x scripts/tbd-pull
   chmod +x scripts/tbd-push
   ```
2. Run them from the terminal depending on the situation
   ```shell
   scripts/env-check
   ```
   ```shell
   scripts/tbd-pull
   ```
   ```shell
   scripts/tbd-push
   ```

To make these feel more git-like, you can add them as git [alias] commands
1. Add a `.gitconfig` file at the root folder and chose your own aliases:
   ```txt
   [alias]
   shipit = "!sh scripts/tbd-push"
   ```
2. Configure your local repo copy to use the .gitconfig
   ```shell
   git config --local include.path ../.gitconfig
   ```

#### References
- [Beginners Intro to Trunk Based Development](https://dev.to/jonlauridsen/beginners-intro-to-trunk-based-development-3158)
- [Practical Guide to Trunk Based Development](https://dev.to/jonlauridsen/practical-guide-to-trunk-based-development-1hlj)
