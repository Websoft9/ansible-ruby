# CLI

## gem

```text
gem -h

RubyGems is a sophisticated package manager for Ruby.  This is a
basic help message containing pointers to more information.

  Usage:
    gem -h/--help
    gem -v/--version
    gem command [arguments...] [options...]

  Examples:
    gem install rake
    gem list --local
    gem build package.gemspec
    gem help install

  Further help:
    gem help commands            list all 'gem' commands
    gem help examples            show some examples of usage
    gem help gem_dependencies    gem dependencies file guide
    gem help platforms           gem platforms guide
    gem help <COMMAND>           show help on COMMAND
                                   (e.g. 'gem help install')
    gem server                   present a web page at
                                 http://localhost:8808/
                                 with info about installed gems
  Further information:
    http://guides.rubygems.org
```

## bundler

```text
bundle -h

       bundle outdated(1) bundle-outdated.1.html
              Show all of the outdated gems in the current bundle

       bundle console(1)
              Start an IRB session in the current bundle

       bundle open(1) bundle-open.1.html
              Open an installed gem in the editor

       bundle lock(1) bundle-lock.1.html
              Generate a lockfile for your dependencies

       bundle viz(1) bundle-viz.1.html
              Generate a visual representation of your dependencies

       bundle init(1) bundle-init.1.html
              Generate a simple Gemfile, placed in the current directory

       bundle gem(1) bundle-gem.1.html
              Create a simple gem, suitable for development with Bundler

       bundle platform(1) bundle-platform.1.html
              Display platform compatibility information

       bundle clean(1) bundle-clean.1.html
              Clean up unused gems in your Bundler directory

       bundle doctor(1) bundle-doctor.1.html
              Display warnings about common problems

       bundle remove(1) bundle-remove.1.html
              Removes gems from the Gemfile

PLUGINS
       When  running  a command that isn´t listed in PRIMARY COMMANDS or UTILITIES, Bundler will try to find an executable on your path named bundler-<command> and execute it, passing down
       any extra arguments to it.

OBSOLETE
       These commands are obsolete and should no longer be used:

       ·   bundle cache(1)

       ·   bundle show(1)
```

## rvm

```text
$rvm -h

Warning! PATH is not properly set up, /usr/local/rvm/gems/ruby-2.4.10/bin is not at first place.
         Usually this is caused by shell initialization files. Search for PATH=... entries.
         You can also re-add RVM to your profile by running: rvm get stable --auto-dotfiles
         To fix it temporarily in this shell session run: rvm use ruby-2.4.10
         To ignore this error add rvm_silence_path_mismatch_check_flag=1 to your ~/.rvmrc file.
Ruby enVironment Manager 1.29.12 (latest) (c) 2009-2020 Michal Papis, Piotr Kuczynski, Wayne E. Seguin

Usage:

    rvm [--debug][--trace][--nice] <command> <options>

  for example:

    rvm list                # list installed interpreters
    rvm list known          # list available interpreters
    rvm install <version>   # install ruby interpreter
    rvm use <version>       # switch to specified ruby interpreter
    rvm remove <version>    # remove ruby interpreter (alias: delete)
    rvm get <version>       # upgrade rvm: stable, master

Available commands:

  rvm has a number of common commands, listed below. Additional information about any command
  can be found by executing `rvm help <command>`.

  ruby installation
      fetch                   # download binary or sources for selected ruby version
      install                 # install ruby interpreter
      list                    # show currently installed ruby interpreters
      list known              # list available interpreters
      mount                   # install ruby from external locations
      patchset                # tools related to managing ruby patchsets
      pkg                     # install a dependency package
      reinstall               # reinstall ruby and run gem pristine on all gems
      remove                  # remove ruby and downloaded sources (alias: delete)
      requirements            # installs dependencies for building ruby
      uninstall               # uninstall ruby, keeping it's sources
      upgrade                 # upgrade to another ruby version, migrating gems

  running different ruby versions
      current                 # print current ruby version and name of used gemsets
      do                      # runs a command against specified and/or all rubies
      gemdir                  # display path to current gem directory ($GEM_HOME)
      use <version>           # switch to given (and already installed) ruby version
      use default             # switch to default ruby, or system if none is set
      use system              # switch to system ruby
      wrapper                 # creates wrapper executables for a given ruby & gemset

  managing gemsets
      gemset                  # manage gemsets
      migrate                 # migrate all gemsets from one ruby to another

  rvm configuration
      alias                   # define aliases for `rvm use`
      autolibs                # tweak settings for installing dependencies automatically
      group                   # tools for managing groups in multiuser installations
      rvmrc                   # tools related to managing .rvmrc trust & loading gemsets

  rvm maintenance
      implode                 # removes the rvm installation completely
      cleanup                 # remove stale source files & data associated with rvm
      cron                    # manage setup for using ruby in cron
      docs                    # tools to make installing ri and rdoc docs easier
      get                     # upgrades RVM to latest head, stable or branched version
      osx-ssl-certs           # helps update OpenSSL certs installed by rvm on OS X
      reload                  # reload rvm source itself
      reset                   # remove all default and system settings
      snapshot                # backup/restore rvm installation

  troubleshooting
      config-get              # display values for RbConfig::CONFIG variables
      debug                   # additional information helping to discover issues
      export                  # set temporary env variable in the current shell
      fix-permissions         # repairs broken permissions
      repair                  # lets you repair parts of your environment, such as
                              # wrappers, env files and similar (general maintenance)
      rubygems                # switches version of rubygems for the current ruby
      tools                   # general information about the ruby env
      unexport                # undo changes made to the environment by `rvm export`
      user                    # tools for managing RVM mixed mode in multiuser installs

   information and documentation
      info                    # show the environment information for current ruby
      disk-usage              # display disk space occupied by rvm
      notes                   # display notes with operating system specifics
      version                 # display rvm version (equal to `rvm -v`)

   additional global options
      --debug                 # toggle debug mode on for very verbose output
      --trace                 # toggle trace mode on to see EVERYTHING rvm is doing
      --nice                  # process niceness (increase the value on slow computers, default 0)

For additional documentation please visit https://rvm.io
```

## rails

```
$ rails -h
Usage:
  rails new APP_PATH [options]

Options:
      [--skip-namespace], [--no-skip-namespace]              # Skip namespace (affects only isolated engines)
      [--skip-collision-check], [--no-skip-collision-check]  # Skip collision check
  -r, [--ruby=PATH]                                          # Path to the Ruby binary of your choice
                                                             # Default: /usr/local/rvm/rubies/ruby-2.5.8/bin/ruby
  -m, [--template=TEMPLATE]                                  # Path to some application template (can be a filesystem path or URL)
  -d, [--database=DATABASE]                                  # Preconfigure for selected database (options: mysql/postgresql/sqlite3/oracle/sqlserver/jdbcmysql/jdbcsqlite3/jdbcpostgresql/jdbc)
                                                             # Default: sqlite3
      [--skip-gemfile], [--no-skip-gemfile]                  # Don't create a Gemfile
  -G, [--skip-git], [--no-skip-git]                          # Skip .gitignore file
      [--skip-keeps], [--no-skip-keeps]                      # Skip source control .keep files
  -M, [--skip-action-mailer], [--no-skip-action-mailer]      # Skip Action Mailer files
      [--skip-action-mailbox], [--no-skip-action-mailbox]    # Skip Action Mailbox gem
      [--skip-action-text], [--no-skip-action-text]          # Skip Action Text gem
  -O, [--skip-active-record], [--no-skip-active-record]      # Skip Active Record files
      [--skip-active-job], [--no-skip-active-job]            # Skip Active Job
      [--skip-active-storage], [--no-skip-active-storage]    # Skip Active Storage files
  -P, [--skip-puma], [--no-skip-puma]                        # Skip Puma related files
  -C, [--skip-action-cable], [--no-skip-action-cable]        # Skip Action Cable files
  -S, [--skip-sprockets], [--no-skip-sprockets]              # Skip Sprockets files
      [--skip-spring], [--no-skip-spring]                    # Don't install Spring application preloader
      [--skip-listen], [--no-skip-listen]                    # Don't generate configuration that depends on the listen gem
  -J, [--skip-javascript], [--no-skip-javascript]            # Skip JavaScript files
      [--skip-turbolinks], [--no-skip-turbolinks]            # Skip turbolinks gem
      [--skip-jbuilder], [--no-skip-jbuilder]                # Skip jbuilder gem
  -T, [--skip-test], [--no-skip-test]                        # Skip test files
      [--skip-system-test], [--no-skip-system-test]          # Skip system test files
      [--skip-bootsnap], [--no-skip-bootsnap]                # Skip bootsnap gem
      [--dev], [--no-dev]                                    # Set up the application with Gemfile pointing to your Rails checkout
      [--edge], [--no-edge]                                  # Set up the application with Gemfile pointing to Rails repository
      [--master], [--no-master]                              # Set up the application with Gemfile pointing to Rails repository main branch
      [--rc=RC]                                              # Path to file containing extra configuration options for rails command
      [--no-rc], [--no-no-rc]                                # Skip loading of extra configuration options from .railsrc file
      [--api], [--no-api]                                    # Preconfigure smaller stack for API only apps
      [--minimal], [--no-minimal]                            # Preconfigure a minimal rails app
  -B, [--skip-bundle], [--no-skip-bundle]                    # Don't run bundle install
  --webpacker, [--webpack=WEBPACK]                           # Preconfigure Webpack with a particular framework (options: react, vue, angular, elm, stimulus)
      [--skip-webpack-install], [--no-skip-webpack-install]  # Don't run Webpack install

Runtime options:
  -f, [--force]                    # Overwrite files that already exist
  -p, [--pretend], [--no-pretend]  # Run but do not make any changes
  -q, [--quiet], [--no-quiet]      # Suppress status output
  -s, [--skip], [--no-skip]        # Skip files that already exist

Rails options:
  -h, [--help], [--no-help]        # Show this help message and quit
  -v, [--version], [--no-version]  # Show Rails version number and quit

Description:
    The 'rails new' command creates a new Rails application with a default
    directory structure and configuration at the path you specify.

    You can specify extra command-line arguments to be used every time
    'rails new' runs in the .railsrc configuration file in your home directory,
    or in $XDG_CONFIG_HOME/rails/railsrc if XDG_CONFIG_HOME is set.

    Note that the arguments specified in the .railsrc file don't affect the
    defaults values shown above in this help message.

Example:
    rails new ~/Code/Ruby/weblog

    This generates a skeletal Rails installation in ~/Code/Ruby/weblog.
```

## ruby
```
$ ruby -h
Usage: ruby [switches] [--] [programfile] [arguments]
  -0[octal]       specify record separator (\0, if no argument)
  -a              autosplit mode with -n or -p (splits $_ into $F)
  -c              check syntax only
  -Cdirectory     cd to directory before executing your script
  -d              set debugging flags (set $DEBUG to true)
  -e 'command'    one line of script. Several -e's allowed. Omit [programfile]
  -Eex[:in]       specify the default external and internal character encodings
  -Fpattern       split() pattern for autosplit (-a)
  -i[extension]   edit ARGV files in place (make backup if extension supplied)
  -Idirectory     specify $LOAD_PATH directory (may be used more than once)
  -l              enable line ending processing
  -n              assume 'while gets(); ... end' loop around your script
  -p              assume loop like -n but print line also like sed
  -rlibrary       require the library before executing your script
  -s              enable some switch parsing for switches after script name
  -S              look for the script using PATH environment variable
  -T[level=1]     turn on tainting checks
  -v              print version number, then turn on verbose mode
  -w              turn warnings on for your script
  -W[level=2]     set warning level; 0=silence, 1=medium, 2=verbose
  -x[directory]   strip off text before #!ruby line and perhaps cd to directory
  -h              show this message, --help for more info
```