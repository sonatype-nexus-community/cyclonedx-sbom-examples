# cyclonedx-sbom-examples
This repo has example CycloneDx xml formatted SBOMs for popular packages across the major ecosystems/package managers.  Also, instructions for building and generating the sboms in the readme.  If you add or update packages, commit the manifest/lockfile and the cycloneDx xml back up to the repo please :)

## Ingestion
Scanning the *-bom.xml files in this repo directly with the CLI will give you a report in IQ.  To work with the manual upload, the xml file(s) have to be in an archive (zip, tarball, etc)

## Export from IQ
Any existing report in IQ can be exported into a CycloneDx formatted xml through an API endpoint (regardless of how the report was initially generated)

Instructions here: https://help.sonatype.com/iqserver/automating/rest-apis/cyclonedx-rest-api---v2

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
To list packages:
```
Everything:
npm ls
Specific:
npm ls <package>
```

## golang
To install:
```
go mod download
```
To add a package:
```
go get github.com/username/repository@vx.x.x
```
To list packages:
```
go list -m all
```

## dotnet
```
dotnet tool install --global CycloneDX
dotnet CycloneDX <path> -o <OUTPUT_DIRECTORY>
OR
docker run cyclonedx/cyclonedx-dotnet [OPTIONS] <path>
```

## gradle
To install:
```
gradle build
OR
./gradlew build
OR
.\gradlew.bat build
```
To scan:
```
gradle nexusIQScan
OR
./gradlew nexusIQScan
OR
.\gradlew.bat nexusIQScan
```

## maven

## python
Before running any of the python commands:
```
python3.7 -m venv .venv
source .venv/bin/activate
```
To install:
```
pip install -r requirements.txt
```
To generate:
```
jake sbom -o jake-bom.xml
```
To list packages:
```
pip freeze
```
To add package:
```
pip install <package>==<version>
pip freeze > requirements.txt
```

## debian