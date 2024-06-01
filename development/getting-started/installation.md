# Installation

### Project Codebase

The DrupalX distribution builds upon the popular `drupal-composer/drupal-project` template for Drupal.

### **Getting Started**

Initialize your project using Composer:

```bash
composer create-project drupalninja/drupalx-project:10.x-dev some-dir --no-interaction
```

After running this command, review the generated `composer.json` file to understand the project's organization. All contributed modules and themes are managed through Composer, making them easy to modify.

The custom DrupalX install profile is included directly in the template under the `web/profiles/custom/` directory, allowing for straightforward customization. This profile installs various contributed modules without requiring dependencies, so you can uninstall any module as needed.

### **Quick Install**

Our project template comes with DDEV as the default development environment.

1.  **Configure DDEV**

    Run the DDEV configuration:

    ```bash
    ddev config
    ```
2.  **Install DrupalX**

    Run the custom install command to start DDEV, install Composer dependencies, and install the 'drupalx' profile:

    ```bash
    ddev install
    ```

    After the installation, the application will open in a new browser tab.

### **Problems?**

If you encounter any issues, please file a report on the GitHub project page's issue tracker: [https://github.com/drupalninja/drupalx-project](https://github.com/drupalninja/drupalx-project).

### Next Steps

Congratulations on completing the installation of your DrupalX project! Now that your project is set up, it's time to configure and customize it to suit your needs.
