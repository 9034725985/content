---
title: Ruby
page: ruby
section: tech-languages
---

## Ruby installation

### CRuby

To install CRuby, simply type:

```
# dnf install ruby
```

Above command will install latest stable CRuby
packages including bundled libraries like RubyGems, Minitest, Rake,
RDoc, JSON, BigDecimal and others. Please note that we have
already unbundled them from Ruby itself, so they come in
their own packages and need a specific dependency requirement
in .gemspec or Gemfile as well as a specific `require()` call
in your Ruby code.

### JRuby

Alternatively Fedora comes with JRuby packages that can be installed via:

```
# dnf install jruby
```

Please note that JRuby packages in Fedora are not yet in the best shape
and things might be broken. If you are not willing to experiment, please use the CRuby packages for now.

### Choosing Ruby with RubyPick

All Rubies come installed with RubyPick, the Fedora Ruby manager. Therefore
CRuby has its executable at `/usr/bin/ruby-mri`, JRuby has its at
`/usr/bin/jruby` and `/usr/bin/ruby` is a RubyPick executable that chooses
the right version of Ruby to run.

You don't need to do anything to set up RubyPick to use CRuby as CRuby
is the default. RubyPick was actually introduced to enable Fedora users run other
Ruby implementations that might make their way into official Fedora repositories
such as JRuby.

To use different Ruby via RubyPick run:

```
ruby _mri_ [params]
ruby _jruby_ [params]
```

Or set the expected environment variables as follows:

```
RUBYPICK=_mri_
RUBYPICK=_jruby_
```

[Read more about RubyPick](https://github.com/fedora-ruby/rubypick).
