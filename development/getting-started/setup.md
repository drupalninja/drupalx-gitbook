# Setup

The steps below will guide you through setting up your project using the DrupalX project template.

### **Export Your Configuration**

One of the first steps is to export your configuration to the `./config/sync` directory. Run the following command:

```bash
ddev . drush cex -y
```

From this point, you own all the configuration. To install your site with this configuration, run:

```bash
ddev . drush si -y minimal --existing-config
```

Feel free to update the ddev install command at ./ddev/commands/host/install if you wish to continue using this command to install the site with your custom configuration.

### **Composer Dependencies**

The DrupalX Composer setup includes several dependencies, which can be easily changed or removed. The general workflow is to first uninstall a module and then remove the corresponding dependency from your project's `composer.json` file.

### Next Steps

Now that you have completed the setup of your DrupalX project, it's time to review the DrupalX approach to theming.
