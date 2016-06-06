# Suggestions:
- If using SublimeText, install the [SublimeLinter package](http://www.sublimelinter.com/en/latest/) and then:
    - [PHP Linter](https://github.com/SublimeLinter/SublimeLinter-php)
    - [PHP CodeSniffer](https://github.com/SublimeLinter/SublimeLinter-phpcs)
    - [PHP MessDetector](https://github.com/SublimeLinter/SublimeLinter-phpmd)
- For unit testing, rely on [PHP Unit](https://github.com/sebastianbergmann/phpunit)
- For automated syntax fixes, use [PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer).

## PHP Linter Configuration
```json
"php": {
    "@disable": false,
    "args": [],
    "excludes": []
}
```

## PHP CodeSniffer Configuration
```json
"phpcs": {
    "@disable": false,
    "args": [],
    "cmd": "${project}/vendor/bin/phpcs",
    "excludes": [],
    "standard": "${project}/VeriduRuleset.xml"
}
```

## PHP MessDetector Configuration
```json
"phpmd": {
    "@disable": false,
    "args": [],
    "cmd": "${project}/vendor/bin/phpmd",
    "excludes": [],
    "rulesets": "cleancode,codesize,controversial,design,naming,unusedcode"
}
```

## List of Automated Fixes for PHP-CS-Fixer

- encoding
- short_tag
- elseif
- eof_ending
- function_call_space
- function_declaration
- indentation
- line_after_namespace
- linefeed
- lowercase_constants
- lowercase_keywords
- method_argument_space
- multiple_use
- parenthesis
- php_closing_tag
- single_line_after_imports
- trailing_spaces
- visibility
- array_element_no_space_before_comma
- array_element_white_space_after_comma
- blankline_after_open_tag
- duplicate_semicolon
- empty_return
- extra_empty_lines
- function_typehint_space
- include
- join_function
- list_commas
- namespace_no_leading_whitespace
- new_with_braces
- no_blank_lines_after_class_opening
- no_empty_lines_after_phpdocs
- object_operator
- operators_spaces
- phpdoc_indent
- phpdoc_inline_tag
- phpdoc_no_access
- phpdoc_no_package
- phpdoc_params
- phpdoc_scalar
- phpdoc_separation
- phpdoc_short_description
- phpdoc_trim
- phpdoc_type_to_var
- phpdoc_types
- phpdoc_var_without_name
- print_to_echo
- remove_leading_slash_use
- remove_lines_between_uses
- return
- self_accessor
- short_bool_cast
- single_array_no_trailing_comma
- single_blank_line_before_namespace
- single_quote
- spaces_before_semicolon
- spaces_cast
- standardize_not_equal
- ternary_spaces
- trim_array_spaces
- unary_operators_spaces
- unneeded_control_parentheses
- unused_use
- whitespacy_lines
- align_double_arrow
- align_equals
- concat_with_spaces
- logical_not_operators_with_successor_space
- ordered_use
- phpdoc_order
- short_array_syntax

## Side Notes

1. On linux, `${project}` doesn't seem to work, so install `phpcs` and `phpmd` globally and add the install path to `paths.linux`.
2. The above is also valid for the language standard.
3. `VeriduRuleset.xml` is available [here](VeriduRuleset.xml).
