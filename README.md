# Johnny.Decimal syntax definition

This file is the authoritative source for the approved JD syntax.

> Status: draft.

# Goals

The goals of the JD syntax are:

1. To be a common machine-parsable format that anyone may use to build a JD application.
    - i.e. to enable trivial portability of one's data from any given JD app to any other JD app, or
    - to allow the creation of a central database which presents an API that any app may consume.
2. To be human-readable in the same way that [Markdown](https://daringfireball.net/projects/markdown/syntax#philosophy) is.
3. To specify a common set of errors which result from the incorrect parsing of a JD file.

# Syntax

## Projects, Areas, Categories, IDs

The system is made up of projects (which are optional), areas, categories, and IDs. They are defined as:

- Project: three digits in the range `000` - `999`.
- Area: a range of numbers that follows the format `x0-x9`, e.g. `30-39`.
    - The separator is a Unicode HYPHEN-MINUS (U+002D).
- Category: two digits in the range `00` - `99`.
- ID: two digits in the range `00` - `99`.

A full Johnny.Decimal number may take two forms:

1. In a standard system, the `a`rea-`c`ategory-`ID` number is in the range `00.00` - `99.99`. 
    - The separator is a Unicode FULL STOP (U+002E).
    - In the abstract case we refer to this number as `AC.ID`.
2. In an extended [multiple projects](https://johnnydecimal.com/concepts/multiple-projects/) system, the `pro`ject-`a`rea-`c`ategory-`ID` number is in the range `000.00.00` - `999.99.99`.
    - The separator is a Unicode FULL STOP (U+002E).
    - In the abstract case we refer to this number as `PRO.AC.ID`.

