Herein lies some conventions used throughout the OpenEmu codebase.

This list is by no means exhaustive and quite prototypal as of yet.

## Whitespace
* Braces on their own line
```objective-c
- (void)method
{
}
```

* Pointer declaration
```objective-c
NSString *myString;
```

* Block argument list and types on their own line
```objective-c
int (^blk1)(int) =
^ int (int v)
{
};

[someDictionary enumerateKeysAndObjectsUsingBlock:
 ^ (id key, id obj, BOOL *stop)
 {
 }];
```

* Caret and curly brace on previous line when there is no block parameters
```objective-c
dispatch_async(^{
    // My code
});
```

* Use 4 spaces instead of tabs
```objective-c
@interface SomeClass
{
    int ivar;
}
```

* Class ivars and properties should be aligned
```objective-c
@interface SomeClass
{
    int       someValue;
    BOOL      shouldCloseFile;
    NSString *description;
}

@property(strong) IBOutlet OELibraryController *libraryController;

@property(nonatomic, strong) NSViewController  *currentContentController;
@property(nonatomic, strong) NSViewController  *defaultContentController;
@property                    BOOL               allowWindowResizing;

@property(copy) NSArray *deviceHandlers;
@property(copy) NSArray *coreList;

@end
```

* `NSArray` and `NSSet` variadic list, put each vlaue on its own line
```objective-c
NSArray *someArray = [NSArray arrayWithObjects:
                      @"value1",
                      @"value2",
                      nil];

NSSet *someSet = [NSSet setWithObjects:
                  @"value1",
                  @"value2",
                  nil];
```

* `NSDictionary` put each value and key pair on the same line
```objective-c
NSDictionary *someArray = [NSDictionary dictionaryWithObjectsAndKeys:
                           @"value1", @"key1",
                           @"value2", @"key2",
                           nil];
```

## Naming conventions
* Class names are CamelCased
```objective-c
@implementation SomeClass
```

* Private categories described by empty category, implementation methods placed within main `@implementation` block
```objective-c
@interface SomeClass()
@end
```

* Private methods prefixed with **OE_**
```objective-c
- (void)OE_privateMethod:(BOOL)value;
```

* Use YES and NO

## Ordering

* Implementation classes should follow this general ordering guideline:
    1. `@synthesize`
	2. `+initialize`
	3. `-init`
	4. `-dealloc`
	5. Class Methods (`+someMethod`)
	6. Instance Methods (`-someMethod`)
	7. Delegate Implementation
	6. Setters / Getters

* Order methods by tasks

* Private methods should be close to the public methods that call them

## Objective-C 2.0

* avoid 'dot-syntax'

## Miscellaneous

* Perfer `MAX` and `MIN` macros over if statements. for example: 
```objective-c
value = MAX(someCalculations, someValue);
```
instead of 
```objective-c
value = someCalculations;
if(value < someValue) value = someValue;
```

* There is no need to use conversion functions like `NSRectFromCGRect` or `NSPointToCGPoint` to convert NS-datatypes to CG-datatypes and vice versa.

## Code sample

Here you can see a sample class:
```objective-c
#import "someheader.h"

@interface SomeClass
{
    int ivar;
}

- (void)method;

@end

@interface SomeClass ()

- (void)OE_privateMethod;

@end

@implementation SomeClass

- (void)OE_privateMethod
{
    // do things
}

- (void)method
{
    if(booleanValue && obj != nil)
    {
        do
        {
            [self OE_privateMethod];
        } while(value > 0);
    }

    while(value < 10)
    {
    }
    
    void (^blk)(void) =
    ^{
        // do things
    };
    
    int (^blk1)(int) =
    ^ int (int v)
    {
        // do things
    };
}

@end
```

## More

For more information read Apple's [Coding Guidelines for Cocoa](http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/CodingGuidelines/CodingGuidelines.html), since the project adheres to these.