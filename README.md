# cyclonedx-sbom-examples
This repo has example CycloneDx xml formatted SBOMs for popular packages across the major ecosystems/package managers.  Also, instructions for building and generating the sboms in the readme.  If you add or update packages, commit the manifest/lockfile and the cycloneDx xml back up to the repo please :)

## node/npm
To install:
```
npm install
```
To generate:
```
npx auditjs@latest sbom > audtijs-bom.xml
```
To add a package:
```
npm install <package>@<version>
```

## golang
To add a package:
```
go get github.com/username/repository@vx.x.x
```

## dotnet
```
dotnet tool install --global CycloneDX
dotnet CycloneDX <path> -o <OUTPUT_DIRECTORY>
OR
docker run cyclonedx/cyclonedx-dotnet [OPTIONS] <path>
```

## gradle

## maven

## debian