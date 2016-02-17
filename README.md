buildpack-mkdocs
================

This is a buildpack for MkDocs (heavily based upon the
[Pelican build-pack](https://github.com/getpelican/heroku-buildpack-pelican)).
This buildpack may be used with any supporting platform (Heroku, Flynn, etc).

```bash
# Heroku:
heroku config:set BUILDPACK_URL=https://github.com/waldocollective/buildpack-mkdocs
# Flynn:
flynn env set BUILDPACK_URL=https://github.com/waldocollective/buildpack-pelican
```

## Configuration

To allow this buildpack to redirect any secondary domains, you can define the
environmental variable `MKDOCS_SITEURL`.

```bash
# Heroku:
heroku config:set MKDOCS_SITEURL=http://www.mkdocs.org
# Flynn:
flynn env set MKDOCS_SITEURL=http://www.mkdocs.org
```

Now any requests to `http://mkdocs.herokuapp.com` or `http://mkdocs.org` will redirect to the `SITEURL`.
