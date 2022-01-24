# heroku-buildpack-apt-bins-path
[heroku/heroku-buildpack-apt](https://github.com/heroku/heroku-buildpack-apt) only adds a subset of the `$HOME/.apt/**/bin/` directories to the PATH environment variable. This issue has not been addressed for quite a long time ([heroku/heroku-buildpack-apt#10](https://github.com/heroku/heroku-buildpack-apt/pull/10), [heroku/heroku-buildpack-apt#39](https://github.com/heroku/heroku-buildpack-apt/pull/39)), so here's a separate buildpack you can use in tandem with [heroku/heroku-buildpack-apt](https://github.com/heroku/heroku-buildpack-apt). Add this buildpack to your heroku app with an index larger than the index of heroku-buildpack-apt by 1, and this will detect and add all `$HOME/.apt/**/bin/` directories to your PATH environment variable.

Code for this buildpack is a slightly modified version of the code for this pr: [heroku/heroku-buildpack-apt#39](https://github.com/heroku/heroku-buildpack-apt/pull/39)
