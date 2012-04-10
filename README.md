# js-apispec

This is a work in progress attempt at creating a DSL that can be used to describe the exposed surface of a Javascript API.

## Key Concepts

- Whitespace sensitive DSL (blocks are space / tab indented)
- Various (overloaded) function forms are indicated with a `>` character.
- Function arguments are space delimited, and are described in `name:type` form.  General thinking is that the `name` part is optional but better for generated documentation.
- If not otherwise specified (e.g. function form character) then an indented section is markdown content.
- No autolinking.  Linking to defined types and methods can be done using a `<syntax>`.
- Function macros can be defined through the `!macro` syntax, and then used with the `fn!macro` syntax.  This is useful for efficiently describing multiple functions that use a similar format without having to repeat yourself.
