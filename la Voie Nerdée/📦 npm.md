`npm install <package_name>` --- install specific package `npm install <package_name>@<version>` --- update package to the specific version `npm install <package_name>@~X.X` --- update package patches (won't update the minor version) 
`npm install <package_name>@latest` --- update package to the latest version

`npm update` --- update all packages in project
`npm list` --- display list of all installed packages with their dependencies

## Versioning explanation
 
- PATCH --- bug fixes and other slight changes (also backwards compatible)
- MAJOR --- breaking changes
- MINOR --- non-breaking (backwards compatible) changes

^ --- allows patch and minor updates for versions 1.0.0 and above patch updates for versions 0.X >=0.1.0 and no updates for versions 0.0.X 

~ --- allows patch-level changes if a minor version is specified (allows minor-level changes if not)

No symbol before the version means the version of the package must match exactly, and should not be updated.