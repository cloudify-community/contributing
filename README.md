# Basic Guidelines for Contributing to Cloudify Community

The Cloudify Community Github organization is the home of all user-submitted assets. This includes [example-blueprints](https://github.com/cloudify-community/blueprint-examples) and plugins.

### Guidelines for Blueprints

All example blueprints should be submitted in a PR to the [example-blueprints](https://github.com/cloudify-community/blueprint-examples) repository. See that repo's [README](https://github.com/cloudify-community/blueprint-examples/blob/master/README.md) for more information.

### Guidelines for Plugins

Community plugins should be have its own unique repository in the [cloudify-community](https://github.com/cloudify-community) Github organization.

To submit a new plugin, send an email to [Cloudify Community](mailto:community@cloudify.co) with the following information:

  - Tell us about yourself and your project and if you have permission to distribute the project.
  - Follow the plugin development [best practices](https://cloudify.co/knowledge-base/cloudify-plugin-development-best-practices/) and these conventions:
    - **Naming**: The plugin repository name should start with the prefix `cloudify-` and end with the suffix `-plugin`, for example, `cloudify-kubernetes-plugin`.
    - **Documentation**: Each repo's root directory should contain a README.md with the following sections:
      * Summary of what the example is about
      * Prerequisites
      * Tested Version (Most recent Cloudify version must be among them.)
      * Complete `install` and `uninstall` instructions
      * Additional workflows, for example any supported `execute_operation` workflows, or custom workflows like `rolling_upgrade`.
    - **Directory Structure**: The plugin directory structure should conform to that of standard Python projects, with the addition of a plugin YAML:
      * ./
        * ./setup.py
        * ./my_package
          * ./my_package/__init__.py
          * ./my_package/my_module.py
        * ./plugin.yaml
        * ./README.md
        * ./integration_tests
        * ./integration_tests/__init__.py
        * ./integration_tests/test_my_plugin.py
    - **Integration Tests**: See [cloudify-ecosystem-tests](https://github.com/cloudify-incubator/cloudify-ecosystem-test).

## Examples

The [cloudify-kubernetes-plugin](https://github.com/cloudify-incubator/cloudify-kubernetes-plugin) is an example of a good plugin.

To learn how to write a plugin, see also the read me of this (non-functional) example [requests plugin](https://github.com/EarthmanT/cloudify-requests-plugin).

