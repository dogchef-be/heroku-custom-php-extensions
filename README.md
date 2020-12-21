# heroku-custom-php-extensions

Additional PHP extensions for Heroku PHP Buildpack

## Extensions
 - [Lpsolve](https://sourceforge.net/projects/lpsolve/): Mixed Integer Linear Programming (MILP) solver
 
## Setup

1. Configure the repository via Heroku CLI (replace APP_NAME):

```bash
heroku config:set --app=APP_NAME HEROKU_PHP_PLATFORM_REPOSITORIES="https://dogchef-be.github.io/heroku-custom-php-extensions/"
```

2. Update project's composer.json:
```json
"require": {
  ...
  "ext-lpsolve": "*",
  ...
}
```

3. Add [heroku-buildpack-apt](https://github.com/heroku/heroku-buildpack-apt) (Heroku > App X > Settings > Buildpacks).
 
4. Add Aptfile to project's root:
```
# heroku-buildpack-apt
lp-solve
```

## License

See the LICENSE file for license rights and limitations (MIT).
