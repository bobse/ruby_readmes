# Rubocop yaml

Set .rubocop.yml in the root folder of the project

```yaml
# AllCops:
#     NewCops: enable
#     Exclude:
#         - "bin/**/*"
#         - "vendor/**/*"
#         - "db/**/*"
#         - "config/**/*"
#         - "script/**/*"
#         - "spec/rails_helper.rb"
#         - "ruby/**/*"
# # Trabalhamos bastante com testes como a documentação viva do projeto então
# # desabilitamos a Cop de documentação com comentário
Style/Documentation:
  Enabled: false

Style/FrozenStringLiteralComment:
  Enabled: false

Metrics/MethodLength:
  Max: 50

Metrics/BlockLength:
  Max: 100

# # Costumamos usar o padrão do RuboCop, mas caso queira alterar o tamanho de
# # # caracteres de uma linha, você pode fazê-lo aqui
# Layout/LineLength:
#     Max: 80

# Style/StringLiterals:
#     EnforcedStyle: double_quotes

# FROM PRETTIER
# Disabling all Layout/* rules, as they're unnecessary when the user is using
# Syntax Tree to handle all of the formatting.
Layout:
  Enabled: false

# Re-enable Layout/LineLength because certain cops that most projects use
# (e.g. Style/IfUnlessModifier) require Layout/LineLength to be enabled.
# By leaving it disabled, those rules will mis-fire.
#
# Users can always override these defaults in their own rubocop.yml files.
# https://github.com/prettier/plugin-ruby/issues/825
Layout/LineLength:
  Enabled: true

Style/MultilineIfModifier:
  Enabled: false

# Syntax Tree will expand empty methods to put the end keyword on the subsequent
# line to reduce git diff noise.
Style/EmptyMethod:
  EnforcedStyle: expanded

# lambdas that are constructed with the lambda method call cannot be safely
# turned into lambda literals without removing a method call.
Style/Lambda:
  Enabled: false

# When method chains with multiple blocks are chained together, rubocop will let
# them pass if they're using braces but not if they're using do and end
# keywords. Because we will break individual blocks down to using keywords if
# they are multiline, this conflicts with rubocop.
Style/MultilineBlockChain:
  Enabled: false

# Disable the single- vs double-quotes rules as these depend on whether the user
# has added or not `plugin/single_quotes` for `syntax_tree`
Style/StringLiterals:
  Enabled: false

Style/StringLiteralsInInterpolation:
  Enabled: false

Style/QuotedSymbols:
  Enabled: false

# We let users have a little more freedom with symbol and words arrays. If the
# user only has an individual item like ["value"] then we don't bother
# converting it because it ends up being just noise.
Style/SymbolArray:
  Enabled: false

Style/WordArray:
  Enabled: false

# Disable the trailing-comma rules as these depend on whether the user has added
# or not `plugin/trailing_comma` for `syntax_tree`
Style/TrailingCommaInArguments:
  Enabled: false

Style/TrailingCommaInArrayLiteral:
  Enabled: false

Style/TrailingCommaInHashLiteral:
  Enabled: false
```
