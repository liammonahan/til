# Bundler

## Regenerating a Gemfile.lock file

1. Update the Gemfile

Ensure your Gemfile specifies the desired Ruby version. Add or update the ruby directive:

```
ruby '<new-ruby-version>'
```

2. Remove the Existing Gemfile.lock

3. Reinstall bundler

Ensure you have the correct version of Bundler installed for the new Ruby version:

```
gem install bundler
```

4. Install Gems and Regenerate the Lock File

Run `bundle install` to install the gems and regenerate the Gemfile.lock.

5. Test the Application
Make sure the app still works

6. Commit changes

Commit the new lockfile to version control.

