# Depedencies Resolving

**Implement the solution in a language of your choice.**

You are implementing a package manager for the new hot language - Java.JS. This is a Java language that compiles to JavaScript.

There are 3rd party packages that can be installed. All packages are described in `all_packages.json`.

Each package is described as a key-value unit, where the key is the name of the pacakge and the value is a list of packages that should be installed first as dependencies.

Here is an example `all_packages.json`

```json
{
  "backbone": ["jQuery", "underscore"],
  "jQuery": ["queryJ"],
  "underscore": ["lodash"],
  "queryJ": [],
  "lodash": []
}
```

In your project, there are local dependencies, described in a simple `dependencies.json` file. Here is an example one:

```json
{
  "projectName": "Test0000",
  "dependencies": ["backbone"]
}
```

Your job is to implement a simple command-line tool that reads `dependencies.json` file and outputs what else should be installed in order for everything to work.

There can be already installed packages, which are going to be located in a folder, called `installed_modules`, where each dependency is a separate folder, which name is the name of the package.

Here is an example directory:

```
├── all_packages.json
├── dependencies.json
├── installed_modules
│   └── lodash
└── README.md
```

Your tool should read the `dependencies.json` and `all_packages.json` and output that the following libraries are going to be installed:

```
Installing backbone.
In order to install backbone, we need jQuery and underscore.
Installing jQuery.
In order to install jQuery, we need queryJ.
Installing queryJ.
Installing underscore.
In order to install underscore, we need lodash. Lodash is already installed.
All done.
```

Afer running the script, your `installed_modules` folder should looke like that:

```
installed_modules/
├── backbone
├── jQuery
├── lodash
├── queryJ
└── underscore
```

**This is an open problem and it is up to your interpretation for the details**
