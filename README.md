# Instructions

## Background Information

When logged in as the administrator, the "Site Information" form can be found at the path /admin/config/system/site-information. This module adds a site api key textfield here which can be used to get nodes in JSON format.

## Features

This module alters the existing Drupal "Site Information" form.

* Add a API key.
* Use the API key to get JSON for a node object.

## Example URL

http://example.com/page_json/FOOBAR12345/17

* Argument 1 = FOOBAR12345 = Site API Key
* Argument 2 = 17          = Node ID

## Usage
* Install the module.
* Go to Site Information page and set a Site API Key.
* Use the API Key as argument 1 to get JSON response for a node of type page.

## Response Codes

###Success
* 20001 - Success

###Error
* 10001 - Site API key is not set or is invalid.
* 10002 - Node ID passed is not a numeric value or is not greater than 0.
* 10003 - Node ID doesnot exist or is not of type page.

## Reference links used

https://api.drupal.org/api/drupal/modules%21system%21system.api.php/function/hook_form_FORM_ID_alter/7.x
https://api.drupal.org/api/drupal/developer!topics!forms_api_reference.html/7.x/
https://api.drupal.org/api/drupal/includes!common.inc/function/drupal_json_output/7.x
https://api.drupal.org/api/drupal/core%21lib%21Drupal%21Component%21Render%21FormattableMarkup.php/function/FormattableMarkup%3A%3AplaceholderFormat/8.2.x
