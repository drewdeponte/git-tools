# Git Tools

This repository houses random git tools that we have whip'd up over time.

## Hooks

The files in the `hooks` directory are Git hooks. Normally these would get
placed in you `project_dir/.git/hooks` directory with the correct name depending
on the position in the life cycle you want to hook into.

This is great if it is just your own individual standards that you are trying to
enforce. However, if it is a cross-team standard that you are trying to enforce
you need to create a `project_dir/hooks` directory and place the hook files in
that directory with the correct name. This allows you to commit the hooks to
source control so that it is in lock step with standards of the team as they
evolve.

You also need to have each of the team members run the following command after
they do a fresh clone of the repository.

    git config core.hooksPath hooks

The above tells Git to look inside the `hooks` directory within the project for
the hooks rather than the default `.git/hooks` directory.

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
