# Usage

## First time use
Install atom as usual and then navigate to the .atom directory and run

git init .
git remote add origin git@github.com:jwblangley/atom-config.git
git fetch origin
git checkout master

NB before the final line is run, the .atom directory must not contain config.cson or keymap.cson


## Continued Use
Navigate to the .atom directory and run

git pull
apm install --packages-file packages.txt

Then restart atom (not strictly necessary).
