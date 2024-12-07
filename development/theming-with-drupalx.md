# Theming with DrupalX

### Approach

DrupalX employs the Drupal "[Starterkit](https://www.drupal.org/docs/core-modules-and-themes/core-themes/starterkit-theme)" approach to theming, which is detailed on Drupal.org.

Instead of using the DrupalX theme as a base theme, it is intended to be used as a starter theme. Detailed instructions on this approach are available in the [DrupalX theme GitHub repository](https://github.com/drupalninja/drupalx_theme).

### Customizing Your Theme

After creating and enabling your theme, you can begin customizing it to suit your needs.

#### **Single Directory Components**

All DrupalX components are organized within the `components` directory using Drupal's [Single Directory Component](https://www.drupal.org/docs/develop/theming-drupal/using-single-directory-components) approach. To compile SASS for a component run npm run watch:components to compile that folder's .scss file into .css.

To compile your SDC components \*.component.yml files automatically from your component's storybook file, run the npm run watch:stories command.

#### Storybook

DrupalX integrates components with [Storybook](https://storybook.js.org/) using[Twig.js](https://github.com/twigjs) to render Twig templates using JavaScript instead of PHP. You can view the official DrupalX storybook at [https://drupalx.netlify.app/](https://drupalx.netlify.app/).&#x20;

To launch your local Storybook, run the following command from the root directory of your theme:

```bash
npm run storybook
```

#### Tailwind CSS

The DrupalX theme starter leverages the [Tailwind CSS framework](https://tailwindcss.com/) to make frontend development for Drupal faster, easier and leaner.

The global.css located at ./src/css/globals.css provides the base CSS styling and tailwind.config.ts provides the base Tailwind configuration for the theme.

#### **Drupal Integration Templates**

DrupalX uses integration templates to pass Drupal content from entities (e.g. paragraphs) to Storybook components. This approach keeps Storybook components agnostic to Drupal, focusing on Tailwind best practices.

#### **Theme npm Commands**

The `package.json` file for the DrupalX theme includes several commands for tasks like compilation and linting. These commands can be customized for any project.

Read the DrupalX project readme for more details on what scripts are available to run from package.json.

{% embed url="https://github.com/drupalninja/drupalx_theme" %}

