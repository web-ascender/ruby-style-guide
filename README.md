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

If you are using VS Code with the [ruby extension](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby), the following settings can be used to have rubocop auto-format files whenever you save them:

```
"[ruby]": {
  "editor.formatOnSaveTimeout": 2000,
  "editor.formatOnSave": true
},
"ruby.format": "rubocop"
```
