---
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
title:  "Note for Android Studio"
---

## Creating your new project  ##

- Application Name: Capitalize first letter in each word + Space
- Package Name: all lower case
- Activity Name: Capitalize MainActivity (standard name)

## MainActivity ##
Focus on "Android" (what Android cares about)
1. Manifests (can specify which activity is the starter activity
2. java -> put java code here
3. res (layout/values)

i.e.
- MyFirstApp/app/src/main/res/layout/activity_main.xml
- MyFirstApp/app/java/com/kaopu/myfirstapp/MainActivity.java

## auto import ##

Files -> Settings -> Editor -> General -> auto import 

check "Optimize imports on the fly" and "Add unambiguous imports on the fly"

## Adding a breaking point ##

Run -> debug... 
Run -> Step Over/Step Into/Step Out
"Could not find gem 'tzinfo-data x64-mingw32' in any of the gem sources listed in your Gemfile. (Bundler::GemNotFound)" 

```bash
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
```

#### 1. Check Gemfile and ensure tzinfo-data gem is included ####

```bash
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]
```

#### 2. Rerun bundle ####
      
```bash
$ bundle
Fetching gem metadata from https://rubygems.org/..............
Fetching gem metadata from https://rubygems.org/..
Resolving dependencies....
Using concurrent-ruby 1.0.5
Using i18n 0.9.5
Using minitest 5.11.3
Using thread_safe 0.3.6
Using tzinfo 1.2.5
Using activesupport 4.2.10
Using public_suffix 2.0.5
Using addressable 2.5.2
Using bundler 1.17.1
Using coffee-script-source 1.11.1
Using execjs 2.7.0
Using coffee-script 2.4.1
Using colorator 1.1.0
Using ruby-enum 0.7.2
Using commonmarker 0.17.13
Using dnsruby 1.61.2
Using eventmachine 1.2.7 (x64-mingw32)
Using http_parser.rb 0.6.0
Using em-websocket 0.5.1
Using ffi 1.9.25 (x64-mingw32)
Using ethon 0.11.0
Using multipart-post 2.0.0
Using faraday 0.15.3
Using forwardable-extended 2.6.0
Using gemoji 3.0.0
Using sawyer 0.8.1
Using octokit 4.13.0
Using typhoeus 1.3.0
Using github-pages-health-check 1.8.1
Using rb-fsevent 0.10.3
Using rb-inotify 0.9.10
Using sass-listen 4.0.0
Using sass 3.6.0
Using jekyll-sass-converter 1.5.2
Using ruby_dep 1.5.0
Using listen 3.1.5
Using jekyll-watch 2.1.2
Using kramdown 1.17.0
Using liquid 4.0.0
Using mercenary 0.3.6
Using pathutil 0.16.1
Using rouge 2.2.1
Using safe_yaml 1.0.4
Using jekyll 3.7.4
Using jekyll-avatar 0.6.0
Using jekyll-coffeescript 1.1.1
Using jekyll-commonmark 1.2.0
Using jekyll-commonmark-ghpages 0.1.5
Using jekyll-default-layout 0.1.4
Using jekyll-feed 0.10.0
Using jekyll-gist 1.5.0
Using jekyll-github-metadata 2.9.4
Using mini_portile2 2.3.0
Using nokogiri 1.8.5 (x64-mingw32)
Using html-pipeline 2.8.4
Using jekyll-mentions 1.4.1
Using jekyll-optional-front-matter 0.3.0
Using jekyll-paginate 1.1.0
Using jekyll-readme-index 0.2.0
Using jekyll-redirect-from 0.14.0
Using jekyll-relative-links 0.5.3
Using rubyzip 1.2.2
Using jekyll-remote-theme 0.3.1
Using jekyll-seo-tag 2.5.0
Using jekyll-sitemap 1.2.0
Using jekyll-swiss 0.4.0
Using jekyll-theme-architect 0.1.1
Using jekyll-theme-cayman 0.1.1
Using jekyll-theme-dinky 0.1.1
Using jekyll-theme-hacker 0.1.1
Using jekyll-theme-leap-day 0.1.1
Using jekyll-theme-merlot 0.1.1
Using jekyll-theme-midnight 0.1.1
Using jekyll-theme-minimal 0.1.1
Using jekyll-theme-modernist 0.1.1
Using jekyll-theme-primer 0.5.3
Using jekyll-theme-slate 0.1.1
Using jekyll-theme-tactile 0.1.1
Using jekyll-theme-time-machine 0.1.1
Using jekyll-titles-from-headings 0.5.1
Using jemoji 0.10.1
Using minima 2.5.0
Using unicode-display_width 1.4.0
Using terminal-table 1.8.0
Using github-pages 192
Fetching tzinfo-data 1.2018.7
Installing tzinfo-data 1.2018.7
Fetching wdm 0.1.1
Installing wdm 0.1.1 with native extensions
Bundle complete! 5 Gemfile dependencies, 87 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
```

#### 3. It seems working and problem sloved ####

```bash
$ bundle exec jekyll serve

Configuration file: C:/Users/xxxxx/jekyll-FridayMidnight-repo/jekyll-blog-FriMid-repo/_config.yml
            Source: C:/Users/xxxxx/jekyll-FridayMidnight-repo/jekyll-blog-FriMid-repo
       Destination: C:/Users/xxxxx/jekyll-FridayMidnight-repo/jekyll-blog-FriMid-repo/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.667 seconds.
 Auto-regeneration: enabled for 'C:/Users/xxxxx/jekyll-FridayMidnight-repo/jekyll-blog-FriMid-repo'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

See Also: 

<a href="https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-4-build-your-local-jekyll-site">https://help.github.com/articles/setting-up-your-github-pages-site-locally-with-jekyll/#step-4-build-your-local-jekyll-site</a>

<a href="https://github.com/tzinfo/tzinfo/wiki/Resolving-TZInfo::DataSourceNotFound-Errors">https://github.com/tzinfo/tzinfo/wiki/Resolving-TZInfo::DataSourceNotFound-Errors</a>
       

