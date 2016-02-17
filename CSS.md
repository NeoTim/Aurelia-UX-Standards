#Attributes


##Platform Targets

###[show|hide-$platform]

```html

<tag show-ios> <!-- Will show only on iOS -->
<tag show-android> <!-- Will show only on Android -->

<tag hide-ios> <!-- Will hide only on iOS -->
<tag hide-android> <!-- Will hide only on Android -->

```
##Device Targets

> These Are different tahn media queries
> These attributes DO NOT RESPOND TO SCREEN SIZE

###[show|hide-$device]

> Devices <mobile | tablet | desktop>

```html
<tag show-mobile> <!-- Will show only on mobile devices -->
<tag show-tablet> <!-- Will show only on tablet devices -->
<tag show-desktop> <!-- Will show only on desktop devices -->

<tag hide-mobile> <!-- Will hide only on mobile devices -->
<tag hide-tablet> <!-- Will hide only on tablet devices -->
<tag hide-desktop> <!-- Will hide only on desktop devices -->
```

##Screen Targets

> Screen sizes <xs | sm | md | lg | xl>

**Base context is set at 16**
Base context means that `1rem === 16px`

**Sass Breakpoints $variables**

```scss
$screen-xs: 0;     // 0px
$screen-sm: 34rem; // 544px
$screen-md: 48rem; // 768px
$screen-lg: 62rem; // 992px
$screen-xl: 75rem; // 1200px
```

###@mixin breakpoint($screen: String)

> Targeting with SASS

```scss
// for min-width and higher
.className {
  // content

  @include breakpoint(xs) {}

  @include breakpoint(md) {
    // content
  }
}

// for max-width and lower
.className {
  // content
  @include max-breakpoint(xs) {}

  @include max-breakpoint(md) {
    // content
  }
}

```

###[show|hide-$screen]

> Targeting with HTML

```html
<tag show-xs> <!-- Will show only on xs screen -->
<tag show-sm> <!-- Will show only on sm screen -->
<tag show-md> <!-- Will show only on md screen -->
<tag show-lg> <!-- Will show only on lg screen -->
<tag show-xl> <!-- Will show only on xl screen -->

<tag hide-xs> <!-- Will hide only on xs screen -->
<tag hide-sm> <!-- Will hide only on sm screen -->
<tag hide-md> <!-- Will hide only on md screen -->
<tag hide-lg> <!-- Will hide only on lg screen -->
<tag hide-xl> <!-- Will hide only on lg screen -->
```

##Padding

###[pads~=]
```html
<!-- Static Padding -->
<tag pads="a-xs"> <!-- Padding: 16px-->
<tag pads="t-xs | r-xs | b-xs | l-xs"> <!-- Padding-${side}: 16px-->
<tag pads="a-md"> <!-- Padding: 24px-->
<tag pads="t-md | r-md | b-md | l-md"> <!-- Padding-${side}: 24px-->

<!-- Media Query Padding -->
<!-- Mobile -->
<tag pads="a"> <!-- Padding: 16px-->
<tag pads="t | r | b | l"> <!-- Padding-${side}: 16px-->

<!-- Desktop -->
<tag pads="a"> <!-- Padding: 24px-->
<tag pads="t | r | b | l"> <!-- Padding-${side}: 24px-->
```

###[pad~=]
The following Is very similar Except is uses half the padding from the previous Example


```html
<!-- Static Padding -->
<tag pad="a-xs"> <!-- Padding: 8px-->
<tag pad="t-xs | r-xs | b-xs | l-xs"> <!-- Padding-${side}: 8px-->
<tag pad="a-md"> <!-- Padding: 12px-->
<tag pad="t-md | r-md | b-md | l-md"> <!-- Padding-${side}: 12px-->

<!-- Media Query Padding -->
<!-- Mobile -->
<tag pad="a"> <!-- Padding: 8px-->
<tag pad="t | r | b | l"> <!-- Padding-${side}: 8px-->

<!-- Desktop -->
<tag pad="a"> <!-- Padding: 12px-->
<tag pad="t | r | b | l"> <!-- Padding-${side}: 12px-->
```
