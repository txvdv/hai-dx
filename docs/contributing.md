# Contributing documents

## Installation

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

### Helpful scripts
```shell
bin/doctor
```
```shell
bin/update
```
```shell
bin/shipit
```

### Add as git [alias] command
Configure your local git repo to use the .gitconfig
```shell
git config --local include.path ../.gitconfig
```