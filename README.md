# Hooks

Available hooks:

* post-checkout

## Global installation

If you want to install the hooks for each new git-repo you create you can install them globally:

    git clone https://github.com/sumocoders/hooks.git .
    mv post-checkout .git/hooks/post-checkout
    chmod +x .git/hooks/post-checkout

## Available hooks

### post-checkout

The post-checkout hook will check if you have a Procfile, and if so it will ask
you if the Procfile should be executed. If there is no Procfile it will search 
for compass-files and compile them.

#### Installation

    curl -O https://raw.githubusercontent.com/sumocoders/hooks/master/post-commit
    mv pre-commit .git/hooks/post-commit
    chmod +x .git/hooks/post-commit
