# Adobe Development Utils

This toolkit extension for Visual Studio Code provides several utilities for developing Adobe scripts & extensions and working with After Effects expressions.

If you find it useful and want to support me, you can do it [here](https://www.paypal.com/donate?hosted_button_id=Z8FGYYW9L28YC).

[![Donate](https://img.shields.io/badge/Donate-PayPal-success?style=for-the-badge&link=https://www.paypal.com/donate?hosted_button_id=Z8FGYYW9L28YC)](https://www.paypal.com/donate?hosted_button_id=Z8FGYYW9L28YC)

## Script Build

Pack your script into a single file, with the following options:

- script obfuscation (see [JS Obfuscation](#js-obfuscation))
- script JSXBIN encoding (see [JSXBIN Encoding](#jsxbin-encoding))
- script header (script name, description, version, build date, license, author, author webpage)

Check the extension's settings (`adobeDevUtils.build`) for more.

### Script Build - Notes

This feature does not replace a proper building tool such as gulp, grunt etc.
It's just a quick way of delivering your scripts.

## After Effects Expressions

Send and receive After Effects expressions to / from the selected properties.

### SEND

From VS Code

![AE expression - send (VS Code)](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_ae_expression_01.gif?token=ACS446GMOMTSSQ3HBL4XX4TABGAXO)

To After Effects

![AE expression - send (AE)](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_ae_expression_02.gif?token=ACS446CGAH5ZNZ6BPQH5C5DABGA5A)

#### After Effects Expressions \| Send \- Usage

- In After Effects, select the properties on which you want to apply the expression.
- In VS Code, select the JS lines you want to apply as an `AE expression` (the entire lines will be selected automatically); if no code is selected the entire document will be sent to After Effects.
- Then do one of the following:
  - Press `Alt + E`.
  - Right-click and choose `Adobe Dev Utils: Send AE expression`.

#### After Effects Expressions \| Send \- Notes

- In Windows: make sure the After Effects installation path is correctly set-up in the extension's settings `adobeDevUtils.ae.expression.aePath`.

### RECEIVE

![AE expression - receive](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_ae_expression_receive.gif?token=ACS446GPALAFBPU6NR4N5T3ABGFZ6)

#### After Effects Expressions \| Receive \- Usage

- In After Effects, select the properties having the expressions you want to send to VS Code.
- In VS Code do one of the following:
  - Press `Alt + I`.
  - Right-click and choose `Adobe Dev Utils: Receive AE expressions`.

#### After Effects Expressions \| Receive \- Notes

- In Windows: make sure the After Effects installation path is correctly set-up in the extension's settings `adobeDevUtils.ae.expression.aePath`.

## JS selection to String

Converts the selected lines to JS string (single-line / concatenated / multi-line).

Single-line

![JS to String - single line](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_js_to_string_01.gif?token=ACS446GHOFRQHT36KVW6KLTABG3H2)

Concatenated

![JS to String - concatenated](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_js_to_string_02.gif?token=ACS446AWCHQ6DQHYCUJ223TABHDOY)

Template literal

![JS to String - template literal](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_js_to_string_03.gif?token=ACS446E2CQTTO2KAGHFWAJTABHDSI)

### JS selection to String - Usage

- Make a selection (the entire lines will be selected automatically).
- Then do one of the following:
  - Press `Alt + D`.
  - Right-click and select `Adobe Dev Utils: JS selection to String`.

### JS selection to String - Notes

- If `adobeDevUtils.jsToString.string.stringStyle` is set to `concatenated / multi-line` and `adobeDevUtils.jsToString.string.quotesStyle` is set as `template literal`, the extension will generate a multi-line template literal.
- Check the extension's settings for other options.

## JS Obfuscation

Obfuscate and protect the selected JS lines. Uses [javascript-obfuscator](https://github.com/javascript-obfuscator/javascript-obfuscator).

![JS Obfuscation](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_obfuscate.gif?token=ACS446A477US3PO3UBWLPLDABHFKO)

### JS Obfuscation - Usage

- Make a selection (the entire lines will be selected automatically).
- Then do one of the following:
  - Press `Shift + Alt + D`.
  - Right-click and select `Adobe Dev Utils: obfuscate JS selection`.

### JS Obfuscation - Notes

- Check the extension's settings to modify the obfuscator's options.

## JSXBIN Encoding

Encodes the selected JSX lines to JSXBIN. it uses the `@esdebug` module from [ExtendScript Debugger](https://marketplace.visualstudio.com/items?itemName=Adobe.extendscript-debug).

![JSXBIN Encoding](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_encode.gif?token=ACS446G2AH4A34QYZDYU5T3ABHGGM)

### JSXBIN Encoding - Usage

- Make a selection (the entire lines will be selected automatically).
- Then do one of the following:
  - Press `Ctrl + Shift + Alt + E` on Windows or `Cmd + Shift + Alt + E` on Mac.
  - Right-click and select `Adobe Dev Utils: encode JS selection to JSXBIN`.

### JSXBIN Encoding - Notes

- Check the extension's settings.
- The JS lines can be obfuscated first before they are encoded to JSXBIN by doing one of the following:
  - Press `Ctrl + Shift + Tab` on Windows or `Cmd + Shift + Tab` on Mac.
  - Right-click and select `Adobe Dev Utils: obfuscate + encode JS selection to JSXBIN`.

## Conversion

### HEX

![Convert HEX](https://raw.githubusercontent.com/alexmunteanu/VS-Code-Adobe-Development-Utils/master/images/vscode-adobe-dev-utils_convert_hex.gif)

- Escape (shortcut `Alt + H`)
- Unescape (shortcut `Alt + U`)

## Installation

- From VS Code
  - Open Extensions and type `adobe-dev-utils`.
  - Click `Install` and reload window.
- From GitHub
  - Download the repository and unzip the package.
  - Copy `VS-Code-Adobe-Development-Utils-master` to `/Users/YOURUSER/.vscode/extensions` folder.
  - Run `npm install`.
  - Reload VS Code.

## Donate

[![Donate](https://img.shields.io/badge/Donate-PayPal-success?style=for-the-badge&link=https://www.paypal.com/donate?hosted_button_id=Z8FGYYW9L28YC)](https://www.paypal.com/donate?hosted_button_id=Z8FGYYW9L28YC)
