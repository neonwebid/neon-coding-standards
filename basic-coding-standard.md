# Basic Coding Standard

## 1. Overview
- Files MUST use only ``<?php`` tags.
- Class constants MUST be declared in all upper case with underscore separators.
- Method names MUST be declared in ``camelCase``.

## 2. Namespace and Class Names
NameSpace and ClassName MUST use ``StudlyCaps``

```php
<?php
namespace Vendor\Model;

class NeonClassName {

}

```
## 3. Class Constants, Properties, and Methods
- Class Constants MUST use CAPITAL & UNDERSCORE for replacing space.
- Properties and Methods MUST declare prefixing keyword Visibility `public`, `protected`, & `private`. 
- Property names MUST use ``snake_case``.
- Methods names MUST use ``camelCase``.

```php
<?php
namespace Vendor\Model;

class NeonClassName {
    
    const NEON_VERSION_NUMBER = 1.2;
    
    private $neon_property;
    
    public function getProperty() {
        return $this->neon_property;
    }
    
    public function getVersion() {
        return NEON_VERSION_NUMBER;
    }
    
}
```

## 4. Variable & Function Name
- Variable & Function names MUST reflection the function. 
- OPTIONAL. Use prefix ``the_`` for void result or ``get_`` for return result.
- Variable & Function names MUST use ``snake_case``
- For Function MUST be checking for making sure function not exists

```php

$neon_variations = true;

if ( ! function_exists('get_neon_vatiations') {
    function get_neon_vatiations() {
        global $neon_variantions;
        
        return $neon_variations;
    }
}

```

## 5. Include & Required Class
- Even use include or Required for class MUST check ``class_exists``

```php

if ( ! class_exists('\Vendor\Model\NeonClassName') ) {
    require_once __DIR__ . '/class.neon-name.php';
}

```

## 6. Files
- File names MUST use `lowercase` and dash for replacing space.
- Class File MUST be prefixed by ``class.``

```

index.php
home-page.php
class.personal-menu.php

```