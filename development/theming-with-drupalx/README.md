# Theming with DrupalX

### Approach

DrupalX employs the Drupal "[Starterkit](https://www.drupal.org/docs/core-modules-and-themes/core-themes/starterkit-theme)" approach to theming, which is detailed on Drupal.org.

Instead of using the DrupalX theme as a base theme, it is intended to be used as a starter theme. Detailed instructions on this approach are available in the [DrupalX theme GitHub repository](https://github.com/drupalninja/drupalx\_theme).

### Customizing Your Theme

After creating and enabling your theme, you can begin customizing it to suit your needs.

**Storybook**

All DrupalX components are organized within the `src/stories/components` directory, which is loaded into a [Storybook](https://storybook.js.org/) instance. You can view an example at [https://drupalx.netlify.app/](https://drupalx.netlify.app/). Our theme utilizes [Twig.js](https://github.com/twigjs) to render Twig templates using JavaScript instead of PHP.

<div align="left">

<figure><img src="../../.gitbook/assets/component files.png" alt="" width="188"><figcaption><p>DrupalX component files</p></figcaption></figure>

</div>

To launch your local Storybook, run the following command from the root directory of your theme:

```bash
npm run storybook
```

**Bootstrap**

The DrupalX theme starter leverages the [Bootstrap framework](https://getbootstrap.com/) to simplify the theming process. All Bootstrap files are included as source files, allowing you to replace or override any file for maximum flexibility.

Key files for modifying Bootstrap are located in the `./src/stories/global/` directory:

* **\_variables.scss**: Override global variables.
* **\_bootstrap-init.scss**: Necessary for components that use Bootstrap variables or mixins.
* **\_bootstrap.scss**: Includes only the Bootstrap styles used on every page. Dependencies specific to components, like the "Accordion", are included in that component's SCSS file (e.g., `accordion.scss`).

<div align="left">

<figure><img src="../../.gitbook/assets/global files.png" alt="" width="147"><figcaption><p>DrupalX global directory</p></figcaption></figure>

</div>

**Drupal Libraries**

Each component's CSS and JavaScript dependencies are defined in the theme's `.libraries.yml` file in the root directory. This ensures files are only loaded as needed based on the components rendered on the page.

Most libraries are attached within integration templates provided in each component's folder. For example, the accordion component has a "templates" subfolder containing the integration template for the block and paragraph Twig templates.

Libraries point to compiled asset files located in the theme's `dist` folder. These files are updated via:

```bash
npm run build
npm run watch
```

**Drupal Integration Templates**

DrupalX uses integration templates to pass Drupal content from entities (e.g., blocks, paragraphs) to Storybook components. This approach keeps Storybook components agnostic to Drupal, focusing on Bootstrap best practices.

Spacing for blocks within Layout Builder is handled at the integration layer. DrupalX provides default Bootstrap spacing classes for blocks, but there are various methods to manage block spacing.

**Theme npm Commands**

The `package.json` file for the DrupalX theme includes several commands for tasks like compilation and linting. These commands can be customized for any project:

* `npm run watch`: Useful for compiling SASS as files are modified. Note that a Drupal cache clear may be required for updates to appear within Drupal.

**Bootswatch**

DrupalX includes an optional module that integrates with Bootswatch theme templates, helping to jumpstart the theming process. Instructions for leveraging this tool are provided on the next page.
