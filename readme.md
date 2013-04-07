# Heroku Buildpack: C

Use C-Buildpack if you need Heroku to execute a C application.

## Usage

NOTE: The C app being deployed with this buildpack needs a makefile that will specify the build rules of the project.

```
$ heroku create myapp_name -s cedar
$ heroku config:add BUILDPACK_URL=https://github.com/atris/heroku-buildpack-C.git -a myapp_name
```
# create your app, see test-app for an example
```
$ git push heroku master

-----> Heroku receiving push
-----> Fetching custom git buildpack... done
-----> C app detected
-----> makefile found
gcc -o greesc1 greesc1.c
-----> Compilation done
-----> Discovering process types
       Procfile declares types -> (none)
-----> Compiled slug size: 4K
-----> Launching... done, v9
```

