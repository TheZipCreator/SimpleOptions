# SimpleOptions

A simple args[] parser for D

# Usage:

In your main() function, create a SimpleOptions object with the following arguments:

`new SimpleOptions(args, inputs, flags)`

All arguments are string arrays. The first, `args`, represents the args[] string array passed into your main function. The second, `inputs` represents inputs passed in using a minus. (e.g. `./myapp -input hello.txt`) The third, `flags` represents flags that are passed in using two minuses. (e.g. `./myapp --help --verbose`)

Once done, you can access the result by looking at the SimpleOptions' inputs and flags parameters. Flags is a `bool[string]`, meaning to test a flag, simply do `so.flags["your flag here"]`. Inputs is a `string[][string]`. In order to access its contents, index into it by a string (e.g. `so.inputs["i"]`). This returns an array which can then be looped through or used in other ways.