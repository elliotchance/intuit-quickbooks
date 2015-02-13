# PHP SDK for QuickBooks V3

**This is a composer compatible library from the official PHP SDK.**

The PHP SDK for QuickBooks v3 is set of PHP classes that make it easier to call
QuickBooks APIs.  Some of the features included in this SDK are as follows:

* Ability to perform single and batch processing of CRUD operations on all
  supported QuickBooks entities.

* Support for XML Request and Response format.

* Ability to configure app settings in the configuration file requiring no
  additional code change.

* Support for Gzip and Deflate compression formats to improve performance of
  QuickBooks API calls.
  
* Logging mechanisms for trace and request/response.

* Query Filters that enable you to retrieve QuickBooks entities whose properties
  meet specified criteria.

* Sparse Update to update writable properties specified in a request and leave
  the others unchanged.

* Change data that enables you to retrieve a list of entities modified during
  specified time points.

# Installation

Using composer:

```
composer require elliotchance/intuit-quickbooks
```

# Usage

You must use the following line before you can use any of the functionality of
this library:

```php
IntuitQuickbooks::begin();
```

The above line is required to setup the library. Unfortunately the SDK does not
use namespacing and is filled with `require()`s that depend on certain defines
to be set to work which the line above set's up in a sane way. Further more
classes with common/generic names like `Request` may collide with existing
classes and libraries.

None of the code in this repository has been modified except for the few files 
required to make it compatible with composer.

Included are the original samples in the `_Samples` folder which are also
unmodified to take into account the composer loading above.
