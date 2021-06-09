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