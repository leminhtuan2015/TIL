### R Android

---------------------------

### R Android

* **R** is the dynamically auto generated class
* **R** is created during build process to dynamically identify all assets (from strings to android widgets to layouts)
* Each android module have one **R** class
* **R class** is generated at **build time** at: 
  * [Module-Name]/app/build/generated/source/r/release
  * [Module-Name]/app/build/generated/source/r/debug

```java
import com.fuji.fujisdk.R;

R.menu.search
R.layout.controller_home
R.id.item_search
```

```java
package com.fuji.fujisdk;

public final class R {
    public static final class layout {
        public static int abc_action_bar_title_item=0x7f030000;
    }
    
    public static final class id {
        public static int action0=0x7f0b0094;
    }
    
    public static final class drawable {
        public static int abc_ab_share_pack_mtrl_alpha=0x7f020000;
    }
    
    public static final class color {
        public static int abc_background_cache_hint_selector_material_dark=0x7f0a0046;
    }
    
    public static final class dimen {
        public static int abc_action_bar_content_inset_material=0x7f06000c;
    }
    
    public static final class string {
        public static int abc_action_bar_home_description=0x7f050000;
    }
}
```
