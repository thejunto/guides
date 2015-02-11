Ruby
====

[Sample](sample.rb)

* Avoid multiple assignments per line (`one, two = 1, 2`).
* Avoid ternary operators (`boolean ? true : false`). Use multi-line `if`
  instead to emphasize code branches.
* Avoid explicit return statements.
* Avoid using semicolons.
* Prefer double quotes for strings.
* Prefer `&:method_name` to `{ |item| item.method_name }` for simple method
  calls.
* Prefer `if` over `unless`.
* Use `%{}` for single-line strings needing interpolation and double-quotes.
* Use `{...}` for single-line blocks. Use `do..end` for multi-line blocks.
* Use `?` suffix for methods that return `true` or `false`.
* Use `CamelCase` for classes and modules, `snake_case` for variables and
  methods, `SCREAMING_SNAKE_CASE` for constants.
* Use `def self.method`, not `def Class.method` or `class << self`.
* Use `each`, not `for`, for iteration.
* Use a trailing comma after each item in a multi-line list, including the last
  item. [Example][trailing comma example]

[trailing comma example]: /style/ruby/sample.rb#L49
