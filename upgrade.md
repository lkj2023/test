# Upgrade Guide

- [Upgrading To 11.0 From 10.x](#upgrade-11.0)

<a name="high-impact-changes"></a>
## High Impact Changes

<div class="content-list" markdown="1">

- [Updating Dependencies](#updating-dependencies)
- [Updating Minimum Stability](#updating-minimum-stability)

</div>

<a name="low-impact-changes"></a>
## Low Impact Changes

<div class="content-list" markdown="1">

- [The `Enumerable` Contract](#the-enumerable-contract)

</div>

<a name="upgrade-11.0"></a>
## Upgrading To 11.0 From 10.x

<a name="estimated-upgrade-time-??-minutes"></a>
#### Estimated Upgrade Time: ?? Minutes

> **Note**  
> We attempt to document every possible breaking change. Since some of these breaking changes are in obscure parts of the framework only a portion of these changes may actually affect your application. Want to save time? You can use [Laravel Shift](https://laravelshift.com/) to help automate your application upgrades.

<a name="updating-dependencies"></a>
### Updating Dependencies

**Likelihood Of Impact: High**

#### PHP 8.2.0 Required

Laravel now requires PHP 8.2.0 or greater.

#### Composer Dependencies

You should update the following dependencies in your application's `composer.json` file:

<div class="content-list" markdown="1">

- `laravel/framework` to `^11.0`

</div>

<a name="collections"></a>
### Collections

<a name="the-enumerable-contract"></a>
#### The `Enumerable` Contract

**Likelihood Of Impact: Low**

The `dump` method of the `Illuminate\Support\Enumerable` contract has been updated to accept a variadic `...$args` argument. If you are implementing this interface you should update your implementation accordingly:

```php
public function dump(...$args);
```
