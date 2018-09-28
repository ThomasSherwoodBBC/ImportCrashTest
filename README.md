# ImportCrashTest
Demos a crash within Xcode 10

Filed as radar 44861954.

**Summary**

Xcode 10 crashes when attempting to import a header from an Objective-C implementation file where the autocomplete popup is summoned while typing while the "User Header Search Paths" build option is non-empty.

**Steps to Reproduce**

1. Create a new Xcode project and add a Cocoa Touch class (can be named anything, so long as it's part of the target)
2. Change the "User Header Search Paths" build option to '.', or to a directory.
3. From main.m, type '#import "', then either begin typing the name of the Cocoa Touch class you created or summon autocomplete using your shortcut

**Expected Results**

Autocomplete suggests the name of the class you were typing, or its standard list of suggestions.

**Actual Results**

Xcode crashes.

**Version/Build**

Version 10.0 (10A255)

**Configuration**

Stock Xcode 10.
