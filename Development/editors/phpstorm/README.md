# Suggestions:
- [PHP with XDebug (using PHPBrew)](Development/languages/php/PHPBrew.md)
- [Sublime Text 3 Keymap](Development/editors/phpstorm/keymaps/Sublime.xml)
- [Sublime Text 3 Color Scheme](Development/editors/phpstorm/colors/Sublime.icls)
- [MonacoB Font](https://github.com/vjpr/monaco-bold)

## Configuring XDebug with PHPStorm
- Settings -> Languages & Frameworks -> PHP -> Debug, verify if the debug port is correct (usually 9000) and that the "Can accept external connections" option is checked for XDebug panel
- Settings -> Languages & Frameworks -> PHP -> Servers, configure the HTTP servers which you want to debug PHP code

# Debugging PHP Code
- Before sending the HTTP request which you want to debug, click que "Start listening for PHP Debug Connections" icon (usually in the top right corner of your PHPStorm)
- Also, you need to send the HTTP query param "XDEBUG_SESSION_START=PHPSTORM" in every request you want to debug

## Installing Sublime Text 3 Keymap
- Download the sublime.xml file (link above) and put in ~/.PhpStorm2016.2/config/keymaps/ (create directory if not exists).
- Settings -> Keymap, select "Sublime" option and save

## Installing Sublime Text 3 Color Scheme
- Download the sublime.icls file (link above) and put in ~/.PhpStorm2016.2/config/colors/ (create directory if not exists).
- Settings -> Editor -> Colors & Fonts, click "Import" if "Sublime" option is not already available

## Using MonacoB Font
- Install MonacoB font in your OS
- Settings -> Editor -> Colors & Fonts -> Font, change the "Primary Font" option to "MonacoB"