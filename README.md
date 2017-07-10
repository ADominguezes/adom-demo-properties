# \<adom-demo-properties\>

is a component created for to be used in other demo components with properties

this component uses the structure of your demo for create a menu with the differents demos

## Structure

In all the separate blocks, it is necessary to apply an id for each block, this id must be `view` followed by a number that starts at 0

__example__

```html
<adom-demo-properties>
  <demo-snippet id="view0" toast-events='["click-navigation-button"]' component-name="adom-card-color" properties-setted='[{"label": "color", "value": "#65a5f2", "color": "#65a5f2"}, {"label": "heading", "value": "title"}, {"label": "counter", "value": "4", "type": "number"}, {"label": "units", "value": "components"}, {"label": "icon", "selected": "0", "list": [{"value":"icons:view-module"}, {"value": "icons:view-carousel"}, {"value": "icons:touch-app"}, {"value": "icons:today"}]}, {"label": "reverse", "selected": "1", "list": [{"value": "false"}, {"value": "true"}]}]'>
  </demo-snippet>
</adom-demo-properties>
```

It´s possible to change the id with the property `defaultContentId`, then, every block must have the value of defaultContentId followed by a number that starts at 0

__example__

```html
<adom-demo-properties default-content-id="demo">
  <demo-snippet id="demo0">
  </demo-snippet>
</adom-demo-properties>
```

It´s possible hide the menu with the property `hideMenu`

__example__

```html
<adom-demo-properties default-content-id="demo" hide-menu>
  <demo-snippet id="demo0">
  </demo-snippet>
  <demo-snippet id="demo1">
  </demo-snippet>
</adom-demo-properties>
```

## Menu

For add the menu´s tab, it's neccessary add in each block the attribute `data-heading` so, it´s possible add the attribute `data-description` for add a description

__example__

```html
<adom-demo-properties default-content-id="demo">
  <demo-snippet id="demo0" data-heading="My demo heading" data-description="My demo description">
  </demo-snippet>
  <demo-snippet id="demo1" data-heading="My demo 2 heading" data-description="My demo 2 description">
  </demo-snippet>
</adom-demo-properties>
```

## Styling

The following custom properties and mixins are available for styling:

Custom property                           | Description                                             | Default  |
------------------------------------------|---------------------------------------------------------|----------|
--adom-demo-properties-paper-tabs-bar-color          | color for paper-tabs bar                                | green    |
--adom-demo-properties                               | mixin for host                                          | {}       |
--adom-demo-properties-toast-content-color           | color for contentColor                                  | green    |
--adom-demo-properties-content-page                  | mixin for .contentPage class                            | {}       |
--adom-demo-properties-content-page-info             | mixin for .contentPage__info class                      | {}       |
--adom-demo-properties-content-page-info-heading     | mixin for .contentPage__info__heading class             | {}       |
--adom-demo-properties-content-page-info-description | mixin for .contentPage__info__heading_description class | {}       |

## Serving your Application

You can serve your application with:

    $ gulp serve
