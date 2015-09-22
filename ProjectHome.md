# Visual Scanner #

The **Visual Scanner** is a Java library visualizing the scanning process realized by the `java.util.Scanner` instances in Java. It can help Java beginners to understand the use of the Scanner and to debug their first programs for reading text files.

## How to use the library ##

  * Add the library (`VisualScanner.jar`) to the class path (the build path of a project).
  * Wherever you want to visualise the scanning, replace Scanner (`java.util.Scanner`) by VisualScanner (`sk.upjs.paz.VisualScanner`). VisualScanner provides all constructors and methods that are provided by the `java.util.Scanner`.

Sample code:

```
VisualScanner scanner = null;
try {
  scanner = new VisualScanner(...);
  // work with scanner
} catch (Exception e) {
  // Handle exception
} finally {
  if (scanner != null) {
    scanner.close();
  }
}
```

## Notes ##

  * VisualScanner is not thread safe (similarly as Scanner).
  * Don't call methods of VisualScanner from the Event Dispatch Thread.
  * Don't use VisualScanner for scanning an input that may block reading (e.g., `System.in`).