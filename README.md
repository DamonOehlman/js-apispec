# js-apispec

This is a work in progress attempt at creating a DSL that can be used to describe the exposed surface of a Javascript API.

## Key Concepts

- Whitespace sensitive DSL (blocks are space / tab indented)
- Various (overloaded) function forms are indicated with a `>` character.
- Function arguments are space delimited, and are described in `name:type` form.  General thinking is that the `name` part is optional but better for generated documentation.
- If not otherwise specified (e.g. function form character) then an indented section is markdown content.
- No autolinking.  Linking to defined types and methods can be done using a `<syntax>`.
- Function macros can be defined through the `!macro` syntax, and then used with the `fn!macro` syntax.  This is useful for efficiently describing multiple functions that use a similar format without having to repeat yourself.  In the case where a macro is used, then the macro content will be appended to any defined for the specific case.

## Working Example

As a working example, I have begun attempting to describe the surface of my simple [matchme](https://github.com/DamonOehlman/matchme) library.  The in-progress definition, and a copy of the raw source can be found in the [samples directory](https://github.com/DamonOehlman/js-apispec/tree/master/samples).
