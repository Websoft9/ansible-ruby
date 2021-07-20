# Install website

To install a website on the ruby runtime environment is generally based on the existing rails environment configuration.  

The main steps is:

```
# Install app package
gem install yourapp

# Creating application scaffolding based on rails
rail new yourapp

# Install dependency package
cd yourapp
bundle install

# Automatic configuration
bin/rake ..

# Run
rails s -b 0.0.0.0
```