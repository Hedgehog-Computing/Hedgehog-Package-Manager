# Hedgehog-Package-Manager

Hedgehog-Package-Manager is the core package manager for Hedgehog Lab. It only contains a single list permanently on Github at

[https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Package-Manager/main/hedgehog-packages.json](https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Package-Manager/main/hedgehog-packages.json)

## A quick tutorial for Hedgehog Lab user

You can use any libraries on Hedgehog Manager by using keyword <code>*import PACKAGE_NAME : FUNCTION_NAME</code>, which PACKAGE_NAME is the package name defined in the JSON list, and FUNCTION_NAME is the actual function defined in the package.

For example, you want to use **magic** and **fibonacci** functions defined at **Hedgehog-Standard-Library**, which is defined in the JSON list as:

```json
{
  "name":"Hedgehog-Standard-Library",
  "alias":"std",
  "location":"https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/",
  "docs":"https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/Readme.md",
  "website": "https://github.com/Hedgehog-Computing/Hedgehog-Standard-Library",
  "author": "lidangzzz"
}
```

Then you don't need to install anything or configurations in your environment, just add the <code>*import</code> macro at the beginning of your script:

```javascript
*import std : magic, fibonacci
```

or 

```javascript
*import Hedgehog-Standard-Library : magic, fibonacci
```

And Hedgehog Lab will help you download and add <code>magic.hss</code> and <code>fibonacci.hss</code> from the package root location, then all functions imported above is ready to use.

The two demos above are exactly the same as importing from URL like:

```javascript
*import https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/magic.hss
*import https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/fibonacci.hss
```

## For Package/Module/Library Developers

- Feel free to add your package into this repo, including the official name, alias and location. It allows users to import your libraries and modules conveniently.
- Please do NOT add malicious codes into your library, such as data theft, back doors, uploading privacy information, cryptocurrency mining or other harmful scripts.
- Please make sure that there aren't any other packages existing that are using your name or alias as names or aliases before submitting pull requests.
- Hedgehog Computing reserves the right to remove any package from the JSON list file.
