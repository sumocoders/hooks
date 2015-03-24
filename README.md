# Hooks

Available hooks:

* post-checkout
* pre-commit

## Global installation

If you want to install the hooks for each new git-repo you create you can install them globally:

    git clone https://github.com/sumocoders/hooks.git .
    mv post-checkout ~/.git/hooks/post-checkout
    mv pre-commit ~/.git/hooks/pre-commit
    chmod +x ~/.git/hooks/post-checkout
    chmod +x ~/.git/hooks/pre-commit

## Available hooks

### post-checkout

The post-checkout hook will check if you have a Procfile, and if so it will ask
you if the Procfile should be executed. If there is no Procfile it will search 
for compass-files and compile them.

#### Installation

    curl -O https://raw.githubusercontent.com/sumocoders/hooks/master/post-checkout
    mv pre-commit .git/hooks/post-checkout
    chmod +x .git/hooks/post-checkout

### pre-commit

The pre-commit hook will check the files that will be commited, the checks are 
managed in our `sumo hook check` commando.

#### Dependencies

This hook has some dependencies:

* Make sure sumodev is installed
* Make sure php is available
* Make sure phpcs is installed, see http://pear.php.net/package/PHP_CodeSniffer
* Make sure csslint is installed, see https://github.com/stubbornella/csslint/wiki/Command-line-interface
* Make sure scss-lint is installed, see https://github.com/causes/scss-lint
* Make sure esvalidate is installed, see https://github.com/duereg/esvalidate

#### Installation

    curl -O https://raw.githubusercontent.com/sumocoders/hooks/master/pre-commit
    mv pre-commit .git/hooks/pre-commit
    chmod +x .git/hooks/pre-commit
