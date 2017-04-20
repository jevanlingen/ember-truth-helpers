# Ember Truth Helpers [![Build Status](https://travis-ci.org/jmurphyau/ember-truth-helpers.svg?branch=master)](https://travis-ci.org/jmurphyau/ember-truth-helpers)

HTMLBars template helpers for additional truth logic in `if` and `unless` statements.

## Usage

Helper   | JavaScript                           | HTMLBars                | More than two arguments allowed |
---------|--------------------------------------|-------------------------|---------------------------------|
eq       | `if (a === b)`                       | `{{if (eq a b)}}`       | No                              |
not-eq   | `if (a !== b)`                       | `{{if (not-eq a b)}}`   | No                              |
not      | `if (!a)`                            | `{{if (not a)}}`        | Yes                             |
and      | `if (a && b)`                        | `{{if (and a b)}}`      | Yes                             |
or       | `if (a || b)`                        | `{{if (or a b)}}`       | Yes                             |
xor      | `if (a && !b || !a && b)`            | `{{if (xor a b)}}`      | No                              |
gt       | `if (a > b)`                         | `{{if (gt a b)}}`       | No                              |
gte      | `if (a >= b)`                        | `{{if (gte a b)}}`      | No                              |
lt       | `if (a < b)`                         | `{{if (lt a b)}}`       | No                              |
lte      | `if (a <= b)`                        | `{{if (lte a b)}}`      | No                              |
is-array | `if (Ember.isArray(a))`              | `{{if (is-array a)}}`   | Yes                             |
is-equal | `if (Ember.isEqual(a, b))`           | `{{if (is-equal a b)}}` | No                              |

### API

## is-equal

`is-equal` uses [`Ember.isEqual`](http://emberjs.com/api/#method_isEqual) helper to evaluate equality of two values.
 `eq` should be sufficient for most applications. `is-equal` is necessary when trying to compare a complex object to
 a primitive value.

## Install

* `ember install ember-truth-helpers`

## Other Helpers

* [ember-get-helper](https://github.com/jmurphyau/ember-get-helper)
* [ember-composable-helpers](https://github.com/DockYard/ember-composable-helpers)

## Development

* `git clone https://github.com/jmurphyau/ember-truth-helpers.git`
* `npm install`
* `bower install`
* `ember server`
* Visit your app at http://localhost:4200.

## Running Tests

* `npm test` (Runs `ember try:testall` to test your addon against multiple Ember versions)
* `ember test`
* `ember test --server`

## Building

* `ember build`

For more information on using ember-cli, visit [http://www.ember-cli.com/](http://www.ember-cli.com/).
