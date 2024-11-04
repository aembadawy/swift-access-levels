# swift-access-levels


## Private
The most restrictive access. Accessible only within the block of code in which it was declared.
```
private var privateVar: String?
```

## filePrivate
Accessible only within the .swift file in which it was declared. i.e. *ViewController.swift*
```
fileprivate var filePrivateVar: String?
```

## Internal
This is the default access level given when it's not specified. Accessible anywhere inside the current app module.
```
var internalVar: String?  // implicitly internal
```

## Public
Access granted to any source file from their defining module, and also any source file from another module that imports the defining module. 
```
public class SomePublicClass {}
public var somePublicVariable = 0
```

## Open
Open access is the highest (least restrictive) access level. Everything in public + it allows for vars/classes to be subclassed and overridden outside their defining module. Usually useful when working on frameworks and SDKs.
```
open class SomeOpenClass {}
open var someOpenVariable = 0
```

`For standard app development, it's a good practice to start off with the *private* access level, as it makes sure that properties and functions cannot be changes from different class or accidentally modified, leveling the access level only when necessary.`
