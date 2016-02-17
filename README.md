heroku-buildpack-mkdocs
=======================

This is a heroku buildpack for MkDocs (heavily based upon the
[Pelican build-pack](https://github.com/getpelican/heroku-buildpack-pelican)).

```bash
$ heroku config:set BUILDPACK_URL=https://github.com/waldocollective/heroku-buildpack-mkdocs
```

## Configuration

To allow this buildpack to redirect any secondary domains, you can define the
environmental variable `MKDOCS_SITEURL`.

```heroku
$ heroku config:set MKDOCS_SITEURL=http://www.mkdocs.org
```

Now any requests to `http://mkdocs.herokuapp.com` or `http://mkdocs.org` will redirect to the `SITEURL`.
