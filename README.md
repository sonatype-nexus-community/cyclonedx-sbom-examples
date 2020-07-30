# cyclonedx-sbom-examples
This repo has example CycloneDx xml formatted SBOMs for popular components across multiple ecosystems.  Also, instructions for building and generating the sboms in the readme.  If you add or update components, commit back up to the repo.

nodejs/npm

npm install
npx auditjs@latest sbom > audtijs-bom.xml

dotnet

dotnet tool install --global CycloneDX
dotnet CycloneDX <path> -o <OUTPUT_DIRECTORY>
OR
docker run cyclonedx/cyclonedx-dotnet [OPTIONS] <path>


