## `1.2.2`

- Update of the libraries
- Added support for Zowe V2 configuration

## `1.2.1`

- Major upgrade of libraries

## `1.2.0`

- Telemetry added
- Details updated

## `1.1.2`

- Edit step snippet so that `condition` is before `variable values`.

## `1.1.1`

- Remove error message `No workflow found with the specified name`, which stopped workflow creation when  overwrite option was selected and no workfow with that name was found on the system.
- When the user tries to `List workflow steps` or `Start a workflow` and no z/OSMF workflows were found with the specified criteria
an empty imput box is no longer shown, instead an informative message `No workflows found` appears.

## `1.1.0`

- Add Zowe CLI integration using default z/OSMF profile.
- Prefix `w4z` for all commands provided by the extention.
- New commands :
    - Create a z/OSMF workflow on a z/OS system
    - Start an already created workflow in z/OSMF
    - List workflow steps
    - Download validation schemas
- Introduced new *Settings* option `List Workflows` for default zowe zosmf profile user ID only.

## `1.0.0`
- Initial release 11/12/2019
