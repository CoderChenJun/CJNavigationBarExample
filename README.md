![smile](https://raw.githubusercontent.com/CoderChenJun/CJColorExample/master/CJLOGO.png "Logo")<br>

# CJNavigationBarExample

_____________________________________________

### Author:CoderChenJun
### Email:Coder.ChenJun@qq.com

____________________________________________

## Catalog
* [Demo](#Demo)
  * [Changing the background color](#Changingthebackgroundcolor)
  * [Making navigation bar scroll along with a scroll view](#Makingnavigationbarscrollalongwithascrollview)
* [Usage](#Usage)

____________________________________________

## <a id="Demo"></a>Demo
#### <a id="Changingthebackgroundcolor"></a>1. Changing the background color:<br>
![CJNavigationBar](https://raw.githubusercontent.com/CoderChenJun/CJNavigationBarExample/master/images/demo.gif)


#### <a id="Makingnavigationbarscrollalongwithascrollview"></a>2. Making navigation bar scroll along with a scroll view:<br>
![CJNavigationBar](https://raw.githubusercontent.com/CoderChenJun/CJNavigationBarExample/master/images/demo2.gif)
____________________________________________


## <a id="Usage"></a>Usage
First, import this lib:

```objective-c
#import "UINavigationBar+CJ.h"
```

The category includes lots of method that helps to change UINavigationBar's appearance dynamically:
```objective-c
@interface UINavigationBar (Awesome)
- (void)cj_setBackgroundColor:(UIColor *)backgroundColor;
- (void)cj_setElementsAlpha:(CGFloat)alpha;
- (void)cj_setTranslationY:(CGFloat)translationY;
- (void)cj_reset;
@end
```

You can call the various setter wherever you want, like:
```objective-c
[self.navigationController.navigationBar cj_setBackgroundColor:[UIColor blueColor]];
```

And usually in `viewWillDisappear`, you should call this method to avoid any side effects:
```objective-c
- (void)viewWillDisappear:(BOOL)animated
{
    [super viewWillDisappear:animated];
    [self.navigationController.navigationBar cj_reset];
}
```
