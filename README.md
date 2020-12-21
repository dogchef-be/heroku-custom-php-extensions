# heroku-custom-php-extensions

Additional PHP extensions for Heroku PHP Buildpack

## Extensions
 - [Lpsolve](https://sourceforge.net/projects/lpsolve/): Mixed Integer Linear Programming (MILP) solver
 
## Setup

1. Add the repository to the Heroku's app:

```bash
heroku config:set HEROKU_PHP_PLATFORM_REPOSITORIES="https://dogchef-be.github.io/heroku-custom-php-extensions/"
```

2. Add [heroku-buildpack-apt](https://github.com/heroku/heroku-buildpack-apt) (Heroku > App X > Settings > Buildpacks).
 
3. Add Aptfile to project's root:
```
# heroku-buildpack-apt
lp-solve
```

## License

See the LICENSE file for license rights and limitations (MIT).
