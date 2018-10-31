defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true
      
# Issue Description #

"Could not find gem 'tzinfo-data x64-mingw32' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)" error is seen at step4 (<a href="https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-4-build-your-local-jekyll-site/">setting-up-your-github-pages-site-locally-with-jekyll</a>) when building local jekyll site.

{% highlight ruby %}
$ bundle exec jekyll serve
C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/resolver.rb:287:in `block in verify_gemfile_dependencies_are_found!': Could not find gem 'tzinfo-data x64-mingw32' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/resolver.rb:255:in `each'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/resolver.rb:255:in `verify_gemfile_dependencies_are_found!'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/resolver.rb:49:in `start'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/resolver.rb:22:in `resolve'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/definition.rb:258:in `resolve'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/definition.rb:170:in `specs'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/definition.rb:237:in `specs_for'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/definition.rb:226:in `requested_specs'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/runtime.rb:108:in `block in definition_method'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/runtime.rb:20:in `setup'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler.rb:107:in `setup'
        from C:/Ruby25-x64/lib/ruby/gems/2.5.0/gems/bundler-1.17.1/lib/bundler/setup.rb:20:in `<top (required)>'
        from C:/Ruby25-x64/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require'
        from C:/Ruby25-x64/lib/ruby/2.5.0/rubygems/core_ext/kernel_require.rb:59:in `require'

{% endhighlight %}

#### 1. Check Gemfile and ensure tzinfo-data gem is included ####

{% highlight ruby %}
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]
{% endhighlight %}

#### 2. Rerun bundle ####
      
      
