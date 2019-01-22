This configuration repository will configure atom to my preferences, including all settings (including those of installed packages), packages and keymaps.

# Usage

Please note that all commands are written for a linux environment, but the vast majority will be consistent with other environments.

## First time use
Install atom as usual and then navigate to the .atom directory and run

```shell
git init .
git remote add origin git@github.com:jwblangley/atom-config.git
git fetch origin
git checkout master
apm install --packages-file packages.txt
```

NB before the `git checkout master` is run, the `.atom` directory must not contain `config.cson` or `keymap.cson`.


## Continued Use

### Updating the repository
To update the repository, navigate to the `.atom` directory and run the following:

```shell
apm list --installed --bare > packages.txt
git add keymap.cson config.cson packages.txt
```

Then commit and push the changes to the repository.

### Updating atom to reflect the repository
Navigate to the `.atom` directory and run

```shell
git pull
apm install --packages-file packages.txt
```

Then restart atom (not strictly necessary).
