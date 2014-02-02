## Modules Rationale

The Extended Library is split into several distinct modules to group
related code and also reduce the final size. Because of the way the
Extended Library is built only what is used will be included by the
linker in the final executable file.

## Modules by Category

### Data Interchange Formats

* [JSON](modules/json)
* [XML](modules/xml)

### User Interface

* [Application Configuration](modules/config)
* [Commandline Options](modules/options)
* [Input Handling](modules/input)
* [Logging](modules/logging)

### Graphics

* [Image Loading](modules/graphics/loading)
* [Image Manipulation](modules/graphics/manipulation)

### Program Correctness

* [Debugging](modules/debug)
* [Error Handling](modules/error)
* [Unit Testing](modules/testly)

### String Functions

* [String Manipulation](modules/strings)
* [String Replacement Class](modules/xstring)

