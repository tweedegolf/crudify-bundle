# Bravesheep Crudify bundle

## Documentation
Read more about the bundle here:

* [Introduction][doc_introduction]
* [Permissions][doc_permissions]
* [Templates][doc_templates]
* [Modify the query used for index pages][doc_modify_index_query]
* [Modify the way objects are retrieved on edit and delete pages][doc_custom_object_retriever]
* [Modify the options array for building the form][doc_custom_form_options]
* [Use a custom controller][doc_custom_controller]
* [Default configuration][doc_config]

## Installation and configuration
Using [Composer][composer] add the bundle to your requirements:

```json
{
    "require": {
        "bravesheep/crudify-bundle": "dev-master"
    }
}
```

Then run `composer update bravesheep/crudify-bundle`

### Basic configuration
Define mappings in your configuration file `app/config/config.yml`:

```yaml
bs_crudify:
    mappings: ~
```

A [full listing of the default config][doc_config] is available in the documentation.

### Add routes to your routing file
In `app/config/routing.yml`, add the routes for the crudify administrator interface:

```yaml
crudify_admin:
    prefix: /admin/
    type: crudify
    resource: .
```

### Add the bundle to your AppKernel
Finally add the bundle in `app/AppKernel.php`:

```php
public function registerBundles()
{
    return array(
        // ...
        new Bs\CrudifyBundle\BsCrudifyBundle(),
        // ...
    );
}
```

[doc_introduction]: src/Bs/CrudifyBundle/Resources/introduction.md
[doc_permissions]: src/Bs/CrudifyBundle/Resources/permissions.md
[doc_templates]: src/Bs/CrudifyBundle/Resources/templates.md
[doc_modify_index_query]: src/Bs/CrudifyBundle/Resources/modify_index_query.md
[doc_custom_object_retriever]: src/Bs/CrudifyBundle/Resources/custom_object_retriever.md
[doc_custom_form_options]: src/Bs/CrudifyBundle/Resources/custom_form_options.md
[doc_custom_controller]: src/Bs/CrudifyBundle/Resources/custom_controller.md
[doc_config]: src/Bs/CrudifyBundle/Resources/doc/config.md
[composer]: https://getcomposer.org/
