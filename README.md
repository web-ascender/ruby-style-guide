# Usage

Copy the following to `.rubocop.yml`
```yaml
inherit_from:
  # For a rails project
  - https://raw.githubusercontent.com/web-ascender/ruby-style-guide/master/rails.yml
  
  # For a non-rails project
  # - https://raw.githubusercontent.com/web-ascender/ruby-style-guide/master/ruby.yml
```

## Other Recommendations

- Add `.rubocop-*` to your `.gitignore` file
- For legacy projects, run `rubocop --auto-gen-config` and add `.rubocop_todo.yml` to the `inherit_from` list in `.rubocop.yml`
- Set up [overcommit](https://github.com/brigade/overcommit) with a [pre-commit-hook](http://rubocop.readthedocs.io/en/latest/integration_with_other_tools/#git-pre-commit-hook-integration) for rubocop
- For projects using rspec, set up [rubocop-rspec](https://github.com/rubocop-hq/rubocop-rspec)

### VS Code

For VS Code, it is strongly recommended to use the [ruby extension](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby).

#### Linter

At a miniumum, I recommend adding the following to your global settings to enable the rubocop linter:

```
"ruby.lint": {
    "rubocop": true,
    "ruby": true
}
```

#### Formatting

The ruby extension can also be configured to have rubocop auto-format files whenever you save them. I recommend enabling this on a project by project basis by adding the following to your workspace settings:

```
"ruby.format": "rubocop",
"[ruby]": {
    "editor.formatOnSaveTimeout": 2000,
    "editor.formatOnSave": true
}
```

#### Intellisense

Ruby intellisense can be enabled by installing the npm `ruby-method-locate` package. You will need to run `npm i -g ruby-method-locate` from the command line and then add the following to your global settings:

```
"ruby.intellisense": "rubyLocate"
```

#### Autocomplete

Ruby autocompletion can be enabled with the `rcodetools` gem. You will need to run `gem install rcodetools` from within the correct version of ruby and add the following to your global settings:

```
"ruby.codeCompletion": "rcodetools"
```