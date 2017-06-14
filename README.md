# Git Tools

This repository houses random git tools that we have whip'd up over time.

## Hooks

Our Git Hooks all live in the `hooks` directory. They are organized by Git
life cycle name that they are intended to work for, ex.
`hooks/prepare-commit-msg` holds all the Git Hooks that are intended to work in
the `prepare-commit-msg` life cycle stage.

The names of the files try to communicate what the hooks do at a high level.

### Installing Hooks

There are two general use cases for installing.

#### Personal Use

In this case simply need to copy the hook file into your projects
`.git/hooks/<stage name>` with the life cycle stage name. For example if you
wanted to install the `require-branch-name-have-jira-issue` hook you would copy
that file into `.git/hooks/prepare-commit-msg`.

#### Team Use

In this case we recommend you create a `hooks` directory at the root of your
project and copy the hook script into that directory with the appropriate life
cycle name. You can then stage and commit this hooks directory so that it stays
in lock step with the code base. This is great because as the hook changes as
the process changes over time it is automatically updated with a developer
pulls.

You also need to have each of the team members run the following command after
they do a fresh clone of the repository.

    git config core.hooksPath hooks

The above tells Git to look inside the `hooks` directory within the project for
the hooks rather than the default `.git/hooks` directory.

We have also provided a script `setup_and_update_hooks` that is intended to be
copied and committed into the root of your project's Git repo, and then executed
to setup the Git hooks and the repositories Git configuration. This is simply a
nice to have to help streamline things a tiny bit more.

## License

These Git tools are Copyright © 2017 UpTech Works, LLC. They are free software,
and may be redistributed under the terms specified in the LICENSE file.

## About ![uptech](http://upte.ch/img/logo.png)

These Git tools are maintained [UpTech Works, LLC][uptech], a software design &
development agency & consultancy.

We love open source software. See [our other projects][community] or
[hire us][hire] to design, develop, and grow your product.

[community]: https://github.com/uptech
[hire]: http://upte.ch
[uptech]: http://upte.ch
