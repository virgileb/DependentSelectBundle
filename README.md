DependentSelectBundle
=====================

This is an improved part of ShtumiUsefulBundle. It discontinues all of its features except the dependent select form.
There are lots of new parameters and features (will be documented soon) implemented in DependentFilteredEntity.

Install using Composer:

```
./composer require evercodelab/dependent-select-bundle
```

### Add the bundle to your AppKernel.php:
This is needed only for Symfony version less than 4
``` php
$bundles = [
    //...
    new Evercode\DependentSelectBundle\DependentSelectBundle(),
];
```

### Import routes

// app/config/routing.yml

//or if using Symfony >= 4 just create the file `route\dependent_select.yaml`
```
dependent_select:
    resource: '@DependentSelectBundle/Resources/config/routing.xml'
```

### Update your configuration

#### Add form theme for twig
```
twig:
    ...
    form:
        resources:
            - DependentSelectBundle::fields.html.twig
```

or if using Symfony > 4 just create a new file in `packages/dependent_selet.yaml` and add
```
twig:
  form_themes:
    - DependentSelectBundle::fields.html.twig
```


### Load jQuery to your views (if not yet)
```
    <script src="http://code.jquery.com/jquery-1.9.1.min.js" type="text/javascript"></script>
```

### Read the documentation

- [How to use](Resources/doc/index.rst)
