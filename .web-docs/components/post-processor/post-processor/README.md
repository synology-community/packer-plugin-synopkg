Include a short description about the post-processor. This is a good place
to call out what the post-processor does, and any additional text that might
be helpful to a user. See https://www.packer.io/docs/provisioner/null
-->

The synopkg post-processor is used to export Packer Scaffolding builds.

<!-- Post-Processor Configuration Fields -->

**Required**

- `mock` (string) - The output path where to save exported build to.

<!--
  Optional Configuration Fields

  Configuration options that are not required or have reasonable defaults
  should be listed under the optionals section. Defaults values should be
  noted in the description of the field
-->

**Optional**

<!--
  A basic example on the usage of the post-processor. Multiple examples
  can be provided to highlight various configurations.

-->

### Example Usage

```hcl
 source "synopkg" "example" {
   mock = "jay"
 }

 build {
   sources = ["source.synopkg.example"]

   post-processor "synopkg" {
     mock = "builds/synopkg.box"
   }
 }
```
