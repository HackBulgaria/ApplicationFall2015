# Application problems

## Points

This problems:

* Checks basic programming skills

---

**Implement the solution in a language of your choice.**

You are on a infinite 2D coordinate system.

The only thing you know is that x increases to the right and decreases to the left, while y increases downwards and decreases upwards.

You know your current position: `(current-x, current-y)`.

You are given a string of the form:

`">v<>>>v^~><><~><><"` where each arrow represents a direction.

Your job is to follow the directions of the arrow and output the final position that you have arrived, starting from your own.

There is one special symbol that you should take care of - **the warp symbol `~`**

When you get the warp symbol, the following effect triggers:

* Moving on X axis is reversed. If `x` is increasing to the right, after the warp symbol,`x` starts to increase to the left and decrease to the right. And vice versa.
* Moving on Y axis is reversed. If `y` is increasing downwards, after the warp symbol, `y` starts to increase upwards and decrease downwards. And vice versa.

Here are few examples:

Input:

```
Starting point: (0, 0)
>>><<<~>>>~^^^
```

Output:

```
(-3, -3)
```

## Word Game

This problem:

* Checks handling with larger but not that hard problems
* Checks OOP skills, if any.

---

**Implement the solution in a language of your choice.**

You are given a rectangular table filled with characters and a `word`.
Your task is to count the occurences of the `word` in the table. The word can be found horizontaly, vertically and across both left to right and right to left.

For example, find the word `ivan` in the table:

| i    | v     | a     | n     |
|---   |---    |---    |---    |
| e    | **v** | **n** | h     |
| i    | n     | **a** | v     |
| m    | v     | **v** | **n** |
| q    | r     | **i** | t     |

Result:
```
3
```

## Dependency resolving 

This problem checks:

* Basic recursion skills
* Working with files
* Basic sense of program design

---

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
│   └── lodash
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

