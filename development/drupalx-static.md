# DrupalX Static

### Exporting DrupalX to Static Files with the Tome Module

The Drupal Tome module enables the export of DrupalX sites to static files. Detailed instructions can be found on the [Tome documentation site](https://tome.fyi/docs/).

#### **Example Usage**

Follow these steps to set it up DrupalX with Tome:

1.  **Add Tome to Composer**

    Add the latest development version of Tome (compatible with Drush 12) to your project:

    ```bash
    composer require drupal/tome:1.x-dev
    ```
2.  **Enable the Tome Static Module**

    Enable the Tome static module using Drush:

    ```bash
    ddev drush en -y tome_static
    ```
3.  **Export the Site Using Drush**

    Export your site to static files:

    ```bash
    ddev drush tome:static --uri=https://yourproductionurl --path-count=1 --process-count=1
    ```
4.  **Navigate to the HTML Directory**

    Change to the `/html` directory:

    ```bash
    cd html
    ```
5.  **Deploy to Netlify**

    Deploy the static site to Netlify. For optimal results, set the process count and path count to 1. This avoids issues with the active menu link not appearing correctly:

    ```bash
    netlify deploy --site yoursitename --prod
    ```
6.  **Configure URLs on Netlify**

    Turn off pretty URLs in Netlify under the "Build & Deploy" configuration. This prevents Netlify from adding a trailing '/' character to URLs.

By following these steps, you can effectively export your DrupalX site to static files and deploy them to Netlify, ensuring a fast and reliable static site experience.
