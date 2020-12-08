# Hedgehog-Package-Manager

Hedgehog-Package-Manager is the core package manager for Hedgehog Lab. It only contains a single list permanently on Github at

[https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Package-Manager/main/packages.json](https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Package-Manager/main/packages.json)

## A quick tutorial for Hedgehog Lab user

You can use any libraries on Hedgehog Manager by using keyword <code>*import PACKAGE_NAME : FUNCTION_NAME</code>, which PACKAGE_NAME is the package name defined in the JSON list, and FUNCTION_NAME is the actual function defined in the package.

For example, you want to use **magic** and **fibonacci** functions defined at **Hedgehog-Standard-Library**, which is defined in the JSON list as:

```json
{
  name:"Hedgehog-Standard-Library",
  alias:"std",
  location:"https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/"
}
```

Then you don't need to install anything or configurations in your environment, just add the <code>*import</code> macro at the beginning of your script:

```javascript
*import std: magic, fibonacci
```

or 

```javascript
*import Hedgehog-Standard-Library:magic,fibonacci
```

in which is Hedgehog Lab will help you automatically download and add the <code>magic.hss</code> and <code>fibonacci.hss</code> located at <code>https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/</code>, which is exactly the same as

```javascript
*import https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/magic.hss
*import https://raw.githubusercontent.com/Hedgehog-Computing/Hedgehog-Standard-Library/main/fibonacci.hss
```
