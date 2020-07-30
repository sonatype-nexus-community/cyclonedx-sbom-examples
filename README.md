# cyclonedx-sbom-examples
This repo has example CycloneDx xml formatted SBOMs for popular packages across the major ecosystems/package managers.  Also, instructions for building and generating the sboms in the readme.  If you add or update packages, commit the manifest/lockfile and the cycloneDx xml back up to the repo please :)

## node/npm
```
npm install
npx auditjs@latest sbom > audtijs-bom.xml
```

## golang

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