### Class
### Instance vs Class Methods

----------------------------------------------------------------

### Class
* **Class = header.h + implementation.m**
* Class in Objective C have 2 part 
  * Header file (.h)
    * The header file (with the file extension .h) **defines the class and everything about it** for the world to know
    * The header file acts as the interface, used just for **defines (Without implement)**
  * Implementation file (.m)
    * (.m files) The other half of a class is the implementation file,
    * Implementation files implement all those things that we declare to be available in the header files
    * Every method that we say a class has must be defined with all its necessary code in the implementation file

* The class is defined in two different sections namely **@interface** and **@implementation**
  * Interface : 
    * **@interface ...  @end**
  * Implementation : 
    * **@implementation ... @end**
  * Properties: 
    * **@property ... @end**
 
* The **instance variables are private** and are only accessible inside the class implementation.
* Properties are introduced in Objective-C to ensure that the instance variable of the class can be accessed outside the class


* **Interface** `Box.h`

```objc
#import <Foundation/Foundation.h>

@interface Box:NSObject
{
//Instance variables
double length;   // Length of a box
double breadth;  // Breadth of a box

//Instance method
- ( void )sayHello;

//Class method
+ (void)connect;
}
@end
```

* **Implementation** `Box.m`

```objc
#import "Box.h"

@implementation Box
- ( void )sayHello
{
    NSLog( @" static lib Hello" );
}

+ ( void )connect
{
    NSLog( @" static lib connect" );
}

@end
```


### Instance vs Class Methods

* Method declarations begin with either a minus (-) or a plus sign (+).
* **Class methods** (beginning with the plus sign) (+)
* **Nnstance method** (beginning with the minus sign) (-)

















