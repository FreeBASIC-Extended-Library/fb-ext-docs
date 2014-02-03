## Modules Rationale

The Extended Library is split into several distinct modules to group
related code and also reduce the final size. Because of the way the
Extended Library is built only what is used will be included by the
linker in the final executable file.

## Modules by Category

### Data Interchange

* [JSON](modules/json)
* [XML](modules/xml)
* [Relational Database](modules/database)

### File I/O

* [File](modules/file)
* [ZipFile](modules/zipfile)

### Graphics

* [Image Loading](modules/graphics/loading)
* [Image Manipulation](modules/graphics/manipulation)
* [TrueType Fonts](modules/graphics/fonts)

### Program Correctness

* [Debugging](modules/debug)
* [Error Handling](modules/error)
* [Unit Testing](modules/testly)

### String Functions

* [String Manipulation](modules/strings)
* [String Replacement Class](modules/xstring)

### User Interface

* [Application Configuration](modules/config)
* [Commandline Options](modules/options)
* [Input Handling](modules/input)
* [Logging](modules/logging)
