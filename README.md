# Create a custom Drupal 7 module

## Background Information

When logged in as the administrator, the "Site Information" form can be found at the path /admin/config/system/site-information.

## Requirements

This module needs to alter the existing Drupal "Site Information" form. Specifics:

* A new form text field named "Site API Key" needs to be added to the "Site Information" form with the default value of “No API Key yet”.
* When this form is submitted, the value that the user entered for this field should be saved as the system variable named "siteapikey".
* A Drupal message should inform the user that the Site API Key has been saved with that value.
* When this form is visited after the "Site API Key" is saved, the field should be populated with the correct value.
* The text of the "Save configuration" button should change to "Update Configuration".
* This module also provides a URL that responds with a JSON representation of a given node with the content type "page" only if the previously submitted API Key and a node id (nid) of an appropriate node are present, otherwise it will respond with "access denied".

## Example URL

http://localhost/page_json/FOOBAR12345/17

## Test Evaluation

* Meeting above requirements
* Utilising Drupal-specific solutions (hooks, APIs, etc.))
* Readability of code
* Clear, concise commenting
* List of resources used if any (Internet sites, books, previous knowledge) Total time to complete task

## Test Submission

* Set up your github.com account if you don't already have one.
* Push the module as a public repo in GitHub and submit the link to it below. *

https://api.drupal.org/api/drupal/modules%21system%21system.api.php/function/hook_form_FORM_ID_alter/7.x