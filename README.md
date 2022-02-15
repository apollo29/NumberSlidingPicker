# Material Number Sliding Picker (Fork)

A widget that enables the user to select a number from a predefined range.
Progress value can be changed using the up and down arrows, click and edit the editable text or swiping up/down or left/right.

<img src="./art/video.gif" alt="Screen shot" width="50%"/>

# Installation

## Maven

```gradle
implementation 'it.sephiroth.android.library:number-sliding-picker:**version**'
```	
	
## JitPack

### Step 1. Add the JitPack repository to your build file:

```gradle
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```

### Step 2. Add the dependency

```gradle
dependencies {
    implementation 'com.github.apollo29:NumberSlidingPicker:Tag'
}
```

Get the latest version  on [![](https://jitpack.io/v/apollo29/NumberSlidingPicker.svg)](https://jitpack.io/#apollo29/NumberSlidingPicker)

# Usage

```xml
    <it.sephiroth.android.library.numberpicker.NumberPicker
        style="@style/NumberPicker.Filled"
        app:picker_max="100"
        app:picker_min="0"
        android:progress="50"
        app:picker_stepSize="2"
        app:picker_tracker="exponential"
        app:picker_orientation="vertical"
        android:id="@+id/numberPicker"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        ... />
```

> See [attrs.xml](./numberpicker/src/main/res/values/attrs.xml) for a complete list of attributes

## Listener

```kotlin
        numberPicker.doOnProgressChanged { numberPicker, progress, formUser ->
            // progress changed
        }
        
        numberPicker.doOnStartTrackingTouch { numberPicker -> 
            // tracking started
        }
        
        numberPicker.doOnStopTrackingTouch { numberPicker -> 
            // tracking ended
        }
```