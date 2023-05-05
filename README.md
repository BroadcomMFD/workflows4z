# Workflows4z

Workflows4z is a VS Code extension that lets you create and validate the z/OSMF workflow definition and the action definition files. With the extension, you can generate variable input file based on the variables that are defined in the workflow definition file. With workflow definition file opened in the extension, you can create and start the workflow for a specified z/OS system. 


## Requirements

- [JAVA Development Kit 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) or later be installed on the machine.
- Set up JAVA_HOME path:
    1. Go to **Windows** -> **Edit the System Environment Variables**.
    2. Click **Environment Variables** at the bottom.
    3. Add a new **System Variable** with Variable name **JAVA_HOME** and Value absolute path to the **JAVA Development Kit**.
- Download workflow task schema and Action file task schema to run the validation commands with the following options:
    - <b>Manual download:</b>
        1. Go to **File** -> **Preferences** -> **Settings**.
        2. Select **Extensions** and then **Workflows4z**.
        3. Paste the absolute path of the Workflows task schema.
            - To download a valid Workflows task schema, see IBM document [The workflow task schema](https://www.ibm.com/support/knowledgecenter/en/SSLTBW_2.3.0/com.ibm.zos.v2r3.izua700/izuprog_WorkflowsXML_Schema.htm) or contact your system programmer.
            - The Action file task schema is supplied with z/OSMF in the following location: */usr/lpp/zosmf/workflow/schemas/actions_v1.xsd*. Download it from there or contact your system programmer.
    - <b>Automated download with Workflows4z: </b>
        Run the command `Download validation schemas` download the workflow task schema and action file task schema. To run this command you require Zowe CLI default z/OSMF profile.

- npm [Downloading and installing Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- Zowe CLI (to properly install zowe cli, in command line type: `npm install -g @zowe/cli`)
- Zowe CLI default zosmf profile to create and start the z/OSMF workflow and list the workflow steps. 
    1. check https://github.com/zowe/zowe-cli 
    2. create profile with user credentials (run command:`zowe profiles create zosmf-profile --help`) 
    3. before use of extension features, <br/>
       first check in command line that zowe profile works corectly (either list workflows or run: `zowe zosmf check status`) 

## Features independent on ZOWE CLI

- IntelliSense provides related options for every actions to create and edit the workflow. Type **zosmf** to invoke the context menu.

- Generates a variable input file in the editable format form the workflow definition file.

- Automatically validates workflow definition or action definition files on each save.

## Features dependent on ZOWE CLI
- Download the validation schemas.

- Create a z/OSMF Workflow on a s/OS system.

- Start the Workflow.

- List the Workflow steps.

## Commands
Following are the commands that are available in the extension that help you create a workflow definition file and create a workflow on the z/OS system:

- **Download validation schemas**

    Run the `Download validation schemas` command to download the valid Workflows task schema and the Action file task schema and update the extension configuration.

- **Validate Workflow**

    Run the `Validate Workflow` command to validate z/OSMF Workflow against Workflows task schema.

- **Validate Action definition file**

    Run the `Validate Action File` command to validate the action definition file against the action schema rules.

- **Generate Variable input file**

    Run the `Generate Variable input file` command to generate a variable input file in the editable properties file format.

- **Create a z/OSMF workflow on a z/OS system**

    Open the workflow definition file in the VS code to create a z/OSMF workflow and run the `Create a z/OSMF workflow on a z/OS system` command. Enter the workflow name, owner ID, and the z/OS system where you want to create a workflow.
    Note: To overwrite a workflow with the same name select True.

- **Start an already created workflow in z/OSMF**

    Run the `Start an already created workflow in z/OSMF` command to execute the created workflow on the specified z/OS system.

- **List workflow steps**

    Run the `List workflow steps` command to list the steps of the created workflow.

## Extension Settings

- `Action File Validation Schema` - To enable specify the absolute path to Action file task schema.
- `Workflow Validation Schema` - To enable specify the absolute path to Workflow definition task schema.
- `Auto Validation` - Enables and disables auto validation on each save of the workflow definition file and the action definition file.
- `List Workflows` - Lists the workflows that are created with the User ID of the default Zowe z/OSMF profile. If you do not select the option List Workflows in settings, it shows all the workflows that are created on the z/OSMF system.

Watch the [Workflows4z](https://www.youtube.com/watch?v=diS6_roHvbw)
 video to view the instructions on how to create a workflow definition file and variable input file in the extension.  
