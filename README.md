# crickets
Converts C# DTO's to TypeScript interfaces via Reflection
## Goals
- Produce output ,ts flies in a hierarchy, one class per file, so that they can participate in tree shaking. 
- Allow traversing of complex types. i.e., if property `Foo` is of type `bar`, then provide a conversion of `bar`.
- Provide core functionality as a library which can be reused in multiple places eg, both MSBuild task and console app
- Identify candidate POCO DTOs with attribute/s.
- Allow overriding of custom property types with custom TypeScript type implementation. 
- Construct tool with an Assembly[] which is scanned for candidate DTOs. 



# Inspiration
I got the idea for this from [MTT](https://github.com/CodySchrank/MTT).

I really liked how he created a MSBuild task which could be dropped into a csproj file via Nuget. 

I thought that I'd have a shot at creating a (more robust?) reflection based TypeScript generator as well