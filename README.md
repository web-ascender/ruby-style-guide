# Usage

Copy the following to `.rubocop.yml`
```yaml
inherit_from:
  # For a rails project
  - https://raw.githubusercontent.com/jmschneider/ruby-style-guide/master/rails.yml
  # For a non-rails project
  # - https://raw.githubusercontent.com/jmschneider/ruby-style-guide/master/ruby.yml
  # For a project using rspec
  - https://raw.githubusercontent.com/jmschneider/ruby-style-guide/master/rspec.yml 
```

## Other Recommendations

- Add `.rubocop-*` to your `.gitignore` file
- Set up [overcommit](https://github.com/brigade/overcommit) with a [pre-commit-hook](http://rubocop.readthedocs.io/en/latest/integration_with_other_tools/#git-pre-commit-hook-integration) for rubocop