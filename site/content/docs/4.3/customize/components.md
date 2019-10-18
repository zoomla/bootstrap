---
layout: docs
title: Components
description: Learn how and why we build nearly all our components responsively and with base and modifier classes.
group: customize
toc: true
---

Many of Bootstrap's components and utilities are built with `@each` loops that iterate over a Sass map. This is especially helpful for generating variants of a component by our `$theme-colors` and creating responsive variants for each breakpoint. As you customize these Sass maps and recompile, you'll automatically see your changes reflected in these loops.

## Modifiers

Many of Bootstrap's components are built with a base-modifier class approach. This means the bulk of the styling is contained to a base class (e.g., `.btn`) while style variations are confined to modifier classes (e.g., `.btn-danger`). These modifier classes are built from the `$theme-colors` map to make customizing the number and name of our modifier classes.

Here are two examples of how we loop over the `$theme-colors` map to generate modifiers to the `.alert` and `.list-group` components.

{{< scss-docs name="alert-modifiers" file="scss/_alert.scss" >}}

{{< scss-docs name="list-group-modifiers" file="scss/_list-group.scss" >}}

## Responsive

These Sass loops aren't limited to color maps, either. You can also generate responsive variations of your components. Take for example our responsive alignment of the dropdowns where we mix an `@each` loop for the `$grid-breakpoints` Sass map with a media query include.

{{< scss-docs name="responsive-breakpoints" file="scss/_dropdown.scss" >}}

Should you need to modify your `$grid-breakpoints`, your changes will apply to all the loops iterating over that map.
