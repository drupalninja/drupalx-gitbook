# DrupalX Bootswatch

### DrupalX Bootswatch Module

The DrupalX project template includes an optional module named "DrupalX Bootswatch" to assist in rapid development. This module simplifies the process of integrating Bootswatch themes with your DrupalX project.

For detailed usage instructions, visit the [GitHub project](https://github.com/drupalninja/drupalx\_bootswatch).

### **How to Use the DrupalX Bootswatch Module**

The module guides you through a few prompts to select a Bootswatch theme and apply it to a DrupalX-based theme.

#### **Step 1: Select the Bootswatch Theme**

First, you will be prompted to choose a theme from [Bootswatch](https://bootswatch.com). Incompatible themes will not be listed, ensuring a smooth selection process.

<figure><img src="../../.gitbook/assets/bootswatch theme (2).png" alt="" width="375"><figcaption><p>Select Bootswatch theme prompt screenshot</p></figcaption></figure>

#### **Step 2: Select the Drupal Theme**

Next, select the DrupalX-compatible theme to which you want to apply the Bootswatch styles.

<figure><img src="../../.gitbook/assets/theme to apply (2).png" alt="" width="375"><figcaption><p>Select DrupalX-based theme screenshot</p></figcaption></figure>

#### **Step 3: Testing Your Updates**

After applying the Bootswatch styles, you should see two files modified. To test your updates:

<figure><img src="../../.gitbook/assets/files modified (2).png" alt=""><figcaption><p>DrupalX files modified screenshot</p></figcaption></figure>

1. Compile your CSS (e.g. `$ npm run build`).
2. Test the changes in both Storybook and Drupal (after clearing caches).

If you encounter any errors, please report them on the [GitHub project page](https://github.com/drupalninja/drupalx\_bootswatch/issues).
