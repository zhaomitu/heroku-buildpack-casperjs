Heroku buildpack: CasperJS
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of [PhantomJS](http://phantomjs.org) and [CasperJS](http://casperjs.org).

Usage
-----

Example usage:

```shell
$ heroku create --stack cedar --buildpack https://github.com/zhaomitu/heroku-buildpack-casperjs.git

# or if your app is already created:
$ heroku config:add BUILDPACK_URL=https://github.com/zhaomitu/heroku-buildpack-casperjs.git

$ git push heroku master
```

Note
-----

If you're using [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) to include other buildpacks, you should set environment variable by your own to include following paths.

    PATH="/usr/local/bin:/usr/bin:/bin:/app/vendor/phantomjs/bin:/app/vendor/casperjs/bin"
    LD_LIBRARY_PATH="/usr/local/lib:/usr/lib:/lib:/app/vendor/phantomjs/lib"



