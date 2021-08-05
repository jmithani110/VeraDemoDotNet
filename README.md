# VeraDemoDotNet

VeraDemoDotNet is a great test application for Veracode IDE Scanner for Visual Studio, Visual Studio Code, and the Veracode Static Pipeline Scanner. 
This example uses Azure Dev Ops to build and test VeraDemoDotNet with the Veracode Static Pipeline scanner.  A Veracode subscription is required.

Clone or connect this repo to Azure Dev Ops. Create a Pipeline using included example azure-pipelines.yml.

Setup API Key in Pipeline Variables 
- VERACODE_API_ID
- VERACODE_API_KEY

Once build completes you can download results.json from build Artifact screen or view them in the console output for the Pipeline scanner step.  

Check the results.json into source code and reference it in the command to break build on new findings. 
Add - bf results.json to string. Remove the || true at the end of the string if you would like the build process to break on new flaws.

Find further options here:https://help.veracode.com/r/r_pipeline_scan_commands
