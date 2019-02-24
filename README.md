# Basic Guidelines for Contributing to Cloudify Community

The Cloudify Community Github organization is the home of all user-submitted assets. This includes [example-blueprints](https://github.com/cloudify-community/blueprint-examples) and plugins.

### Guidelines for Blueprints

All example blueprints should be submitted in a PR to the [example-blueprints](https://github.com/cloudify-community/blueprint-examples) repository. See that repo's [README](https://github.com/cloudify-community/blueprint-examples/blob/master/README.md) for more information.

### Guidelines for Plugins

Each community-submitted plugin should have its own unique repository in the [cloudify-community](https://github.com/cloudify-community) Github organization.

To submit a new plugin, send an email to [community@cloudify.co](mailto:community@cloudify.co) with the following information:

  - Tell us about yourself and your project and if you have permission to distribute the project.
  - A link to your plugin's Github repository.

Please be sure to follow the plugin development [best practices](https://cloudify.co/knowledge-base/cloudify-plugin-development-best-practices/) and these conventions:

  - **Naming**: The plugin repository name should start with the prefix `cloudify-` and end with the suffix `-plugin`, for example, `cloudify-kubernetes-plugin`.
  - **Documentation**: Each repo's root directory should contain a README.md with the following sections:
    * Summary of the plugin's purpose.
    * Prerequisites
    * Tested Version (Most recent Cloudify version must be among them.)
    * Complete `install` and `uninstall` instructions
    * Additional workflows, for example any supported `execute_operation` workflows, or custom workflows like `rolling_upgrade`.
  - **Directory Structure**: The plugin directory structure should conform to that of standard Python projects, with the addition of a plugin YAML:
    * ./
      * ./setup.py
      * ./my_package
        * ./my_package/\__init\__.py
        * ./my_package/my_module.py
      * ./plugin.yaml
      * ./README.md

Community-submitted plugins are not required to have tests. However, we highly recommend it as performance of tested plugins is much higher as is adoption within the community. For help with testing, we have the following resources:

  - See [cloudify-plugin-template](https://github.com/cloudify-cosmo/cloudify-plugin-template): A non-functional plugin template that includes example tests.
  - See [cloudify-ecosystem-tests](https://github.com/cloudify-incubator/cloudify-ecosystem-test): A simple framework for testing plugins and blueprints.
  - See [cloudify-manager-integration-tests](https://github.com/cloudify-cosmo/cloudify-manager/blob/4.5.5/tests/integration_tests/tests/test_cases.py#L645): A base class for testing current code on a Cloudify Manager.

__Note: We encourage you to check your plugin against a Python Linter like flake8 or pep8.__


## Examples

The [cloudify-kubernetes-plugin](https://github.com/cloudify-incubator/cloudify-kubernetes-plugin) is an example of a good plugin.

To learn how to write a plugin, see also the read me of this (non-functional) example [requests plugin](https://github.com/EarthmanT/cloudify-requests-plugin).

