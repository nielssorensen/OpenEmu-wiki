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
int (^blk1)(int) =
^ int (int v)
{
};

* Use 4 spaces instead of tabs
```objective-c
@implementation SomeClass
{
    int ivar;
}
```

## Naming conventions
* Class names are CamelCased
```objective-c
@implementation SomeClass
@end
```

## Objective-C 2.0

* avoid 'dot-syntax'


## Code sample

Here you can see a sample class:
```objective-c
@implementation SomeClass
{
    int ivar;
}

- (void)method
{
    if(booleanValue && obj != nil)
    {
        do
        {
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