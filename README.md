Heroku buildpack: Vendor Binaries
=================================
This is a fork of [peterkeen's buildpack](https://github.com/peterkeen/heroku-buildpack-vendorbinaries) with a few changes.

This fork interprets each line in `.vendor_urls` as a URL pointing to a tarball and an extraction directory separated by a space.

So a valid `.vendor_url` may look like this

```
https://s3.amazonaws.com/my-bucket/foo.tar.gz .heroku/vendor/bin
```

It will also add `/app/.heroku/vendor/bin` to your `$PATH`.
