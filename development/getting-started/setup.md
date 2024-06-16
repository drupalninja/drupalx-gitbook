# Setup

### DrupalX General Approach

DrupalX is designed to offer enterprise developers maximum flexibility in creating custom solutions for their organization. The steps below will guide you through setting up your project using the DrupalX project template.

### **Export Your Configuration**

One of the first steps is to export your configuration to the `./config/sync` directory. Run the following command:

```bash
ddev . drush cex -y
```

From this point, you own all the configuration. To install your site with this configuration, run:

```bash
ddev . drush si -y drupalx --existing-config
```

### **Modifying the Install Profile**

The DrupalX install profile includes only configuration and does not add any dependencies. Therefore, it is generally unnecessary to modify it directly. However, if you wish to create a custom profile template for your organization, you have the option to modify the profile.

### **Composer Dependencies**

The DrupalX Composer setup includes several dependencies, which can be easily changed or removed. The general workflow is to first uninstall a module and then remove the corresponding dependency from your project's `composer.json` file.

### Next Steps

Now that you have completed the setup of your DrupalX project, it's time to review the DrupalX approach to theming.
