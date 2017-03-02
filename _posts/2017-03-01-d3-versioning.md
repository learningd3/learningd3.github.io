---
layout: post
title:  "An Introduction to Semantic Versioning"
header-img: "semantic-versioning.jpg"
image: /assets/img/posts/semantic-versioning.jpg
description: "D3 adheres to a convention called semantic versioning"
---

D3 adheres to a convention called [semantic versioning](http://semver.org/). Semantic versioning, or semver for short, consists  of three numbers. Knowing what these numbers mean will help you determine whether or not you can upgrade to a newer version without breaking your project. The version of D3 that I’m currently using is 4.7.0. Let’s break down each number and what it represents.

(**4**.7.0)
The first number in this chain is called the *major* version.

(4.**7**.0)
The second number is called the *minor* version.

(4.7.**0**)
The third number is called the *patch* version.

These versions are incremented when code changes are introduced. Depending on the nature of the change, a different number is incremented.

The **major version** (first number) is incremented when changes that break the api are released. Usually, when major versions are released there’s a guide released with how to update from the old version to the new one.

The **minor version** (second number) is incremented when functionality is added that does not break any existing functionality. These changes are referred to as *backwards compatible* changes.

The **patch version** (third number) is for backwards compatible *bug fixes*. Bug fixes are in contrast here with features (adding functionality). These patches go out when something is wrong with existing functionality or when improvements to existing functionality are implemented.

If you use libraries that follow semver (like D3!) you should be able to update minor and patch changes without worrying about anything breaking.
