mkdir my-drupal10-site
cd my-drupal10-site
ddev config --project-type=drupal10 --docroot=web --create-docroot
ddev start
ddev composer create drupal/recommended-project
ddev composer require drush/drush
ddev drush site:install --account-name=admin --account-pass=admin -y
# use the one-time link (CTRL/CMD + Click) from the command below to edit your admin account details.
ddev drush uli
ddev launch