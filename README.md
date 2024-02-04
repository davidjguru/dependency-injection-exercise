# The Dependency Injection exercise for Drupal
It shows how to approach service implementation and adaptation tasks in the context of the latest major Drupal versions: 8.x, 9.x. 10.x.

## Setup

1. Clone the repository within the `/web/modules/custom/` path.
1. Install this module enabling the resource. Run `drush en dependency_injection_exercise`.
1. Add the new provided custom block 'Rest output block' to a page.

## Exercises

1. We've got a controller and block, both outputting roughly the same thing. Please refactor these so the call to fetch data happens in a service. Then, inject that service in both the controller and block instead of using \Drupal::service()
1. Take over the MailManager service and ensure all mails are redirected to "nope@doesntexist.com"
1. On the path /dropsolid/example/photos the breadcrumb should be Home > Dropsolid > Example > Photos
1. Take over the LanguageManager service in a way that doesn't preclude others from also taking over the LanguageManager service

## Documentation

- [Services and dependency injection in Drupal 8+](https://www.drupal.org/docs/drupal-apis/services-and-dependency-injection/services-and-dependency-injection-in-drupal-8)
- [Altering existing services, providing dynamic services](https://www.drupal.org/docs/drupal-apis/services-and-dependency-injection/altering-existing-services-providing-dynamic-services)
