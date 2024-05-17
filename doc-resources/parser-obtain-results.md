### Automated import

The easiest approach for importing Debricked results into SSC is through [fcli](https://github.com/fortify-ps/fcli), using the `fcli ssc artifact import-debricked` command. This command will download the Debricked CycloneDX SBOM file using the Debricked REST API, and then upload the SBOM file to SSC for processing by this parser plugin. 

When using fcli, there is no need to manually obtain the SBOM file, preparing a proper SSC third-party results zip-file, and uploading this zip-file to SSC. With this approach, the information in the [Manual import](#manual-import) and [Upload results](#upload-results) sections can be ignored.

### Manual import

The Debricked website allows for generating a report in CycloneDX SBOM format using the following steps:

* Navigate to the repository for which you want to generate the SBOM
* Click on the 'Generate report' button on the top-right
* Select 'SBOM'
* Click the 'Generate' button
* Extract the zip-file that is sent to your registered email address to obtain the raw CycloneDX SBOM file
    * **Note**: The instructions below for uploading the SBOM file to SSC are based on the raw CycloneDX SBOM `.json` file

These steps can also be automated through the Debricked REST API, allowing the generated SBOM either being sent to an email address, or downloaded directly through the REST API.


