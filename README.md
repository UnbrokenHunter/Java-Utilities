## Overview

- **[Java-Vector2](#java-vector2)**
  - **Description**: Represents a 2D vector with `x` and `y` coordinates using `ints`. Provides operations for creating, manipulating, and querying 2D vectors. [Details](#java-vector2)
  
- **[Java-TextUtilities](#java-textutilities)**
  - **Description**: A collection of utility methods for text rendering, measurement, and manipulation. Useful for developers aiming for high-quality and consistent text presentation across platforms. [Details](#java-textutilities)
  
- **[Java-Looper](#java-looper)**
  - **Description**: A utility for creating game loops or any loop that requires a method to run at a fixed frame rate. Uses Java's reflection capabilities for its operation. [Details](#java-looper)

# Java-Vector2
### **Utilities.Vector2**

## `public class Vector2`

**Represents a 2D vector with `x` and `y` coordinates using `ints`.**

### Class Overview

The `Vector2` class provides operations for creating, manipulating, and querying 2D vectors. The class supports basic vector operations such as addition, subtraction, multiplication, and division. It also provides utility methods to calculate the magnitude and distance between two vectors.

### Field Summary

- **`public static final Vector2 one`**  
    A constant vector with values `(1, 1)`.

- **`public static final Vector2 zero`**  
    A constant vector with values `(0, 0)`.

- **`public static final Vector2 up`**  
    A constant vector pointing upwards, with values `(0, 1)`.

- **`public static final Vector2 down`**  
    A constant vector pointing downwards, with values `(0, -1)`.

- **`public static final Vector2 left`**  
    A constant vector pointing left, with values `(-1, 0)`.

- **`public static final Vector2 right`**  
    A constant vector pointing right, with values `(1, 0)`.

- **`public int x`**  
    The `x`-coordinate of the vector.

- **`public int y`**  
    The `y`-coordinate of the vector.

### Constructor Summary

- **`public Vector2()`**  
    Default constructor. Initializes the vector to `(0, 0)`.

- **`public Vector2(int x, int y)`**  
    Initializes the vector with the given `x` and `y` coordinates.

### Method Summary

- **`public static Vector2 add(Vector2 vector1, Vector2 vector2)`**  
    Returns a new vector resulting from the addition of two vectors.

- **`public static Vector2 subtract(Vector2 vector1, Vector2 vector2)`**  
    Returns a new vector resulting from subtracting the second vector from the first one.

- **`public static Vector2 multiply(Vector2 vector, int scalar)`**  
    Returns a new vector by multiplying the vector by the given scalar.

- **`public static Vector2 divide(Vector2 vector, int scalar)`**  
    Returns a new vector by dividing the vector by the given scalar.

- **`public Vector2 plus(Vector2 vector2)`**  
    Returns a new vector by adding the given vector to the current one.

- **`public Vector2 minus(Vector2 vector2)`**  
    Returns a new vector by subtracting the given vector from the current one.

- **`public Vector2 mult(int num)`**  
    Multiplies the components of the vector by the given number.

- **`public Vector2 div(int num)`**  
    Divides the components of the vector by the given number.

- **`public double magnitude()`**  
    Computes the magnitude (length) of the vector.

- **`public static double distance(Vector2 start, Vector2 end)`**  
    Calculates the Euclidean distance between two vectors.

- **`public Vector2 binarize()`**  
    Binarizes the components of the vector.

- **`public int hashCode()`**
    Returns a hash code value for the vector.

- **`public boolean equals(Object obj)`**  
    Compares the vector with another object for equality.

- **`public String toString()`**  
    Returns a string representation of the vector.

### Notes

The `Vector2` class does not handle floating point inaccuracies and might not be suitable for high precision requirements. Also, the division method does not handle division by zero.

### Exceptions

Various methods throw exceptions based on the following conditions:

- **`IllegalArgumentException`**: If the vectors provided are null where they shouldn't be, or if scalar value is zero during division.


# Java-TextUtilities
### **Utilities.TextUtilities**

## `public class TextUtilities`

**Provides a collection of utility methods for text rendering, measurement, and manipulation.**

### Class Overview

The `TextUtilities` class offers an array of methods for enhancing text-related operations. This encompasses tasks like calculating font sizes, aligning text, adding graphical effects, and optimizing rendering. Developers can leverage this utility to ensure text fits designated areas, is aesthetically pleasing, and retains high-quality across various display settings.

### Field Summary

*(For the sake of the example, I'm adding hypothetical fields. Adjust as needed.)*

- **`public static final Font DEFAULT_FONT`**  
    The default font used when no specific font is provided.

- **`public static final int MAX_FONT_SIZE`**  
    The maximum allowable font size.

- **`public static final int MIN_FONT_SIZE`**  
    The minimum allowable font size.

### Method Summary

- **`public static int calcFontSize(String text, Rectangle area)`**  
    Determines the maximum possible font size for a given text to fit within a specified area.

- **`public static Point calcMidText(String text, Rectangle area)`**  
    Calculates the center position for the given text.

- **`public static String[] wrapText(String text, int maxWidth)`**  
    Breaks text into lines that fit within a given maximum width.

- **`public static boolean isTextVisible(String text, Rectangle area, Font font)`**  
    Checks if a text can be fully displayed within the given area for a specified font size.

- **`public static String adjustTextToFit(String text, Rectangle area, Font font)`**  
    Adjusts the text by changing its font size or truncating it to fit within a specified area.

- **`public static void alignTextLeft(String text, Rectangle area)`**  
    Aligns text to the left of a given area.

- **`public static void alignTextRight(String text, Rectangle area)`**  
    Aligns text to the right of a given area.

- **`public static void alignTextCenter(String text, Rectangle area)`**  
    Aligns text to the center of a given area.

- **`public static int getHeightOfMultilineText(String[] lines, Font font)`**  
    Calculates the total height required for multiple lines of text.

- **`public static int getOptimalFontSizeForMultiline(String text, Rectangle area)`**  
    Finds the optimal font size for multiple lines of text.

- **`public static void rotateText(String text, int angle)`**  
    Renders text at a specified rotation angle.

- **`public static void addShadowToText(String text, ShadowProperties properties)`**  
    Adds a shadow effect to the text.

- **`public static void addOutlineToText(String text, OutlineProperties properties)`**  
    Outlines the text.

- **`public static void setHighQualityRendering(GraphicsContext context)`**  
    Improves the text rendering quality.

- **`public static void setAlpha(GraphicsContext context, double alpha)`**  
    Sets the transparency level for the graphics context.

- **`public static void setGradientFill(GraphicsContext context, GradientProperties gradient)`**  
    Sets a gradient fill for the graphics context.

### Notes

Utilizing the `TextUtilities` class can aid in delivering a consistent and professional visual experience for end-users. Always consider device resolutions and display settings when using text utilities to ensure optimal presentation across platforms.

### Exceptions

Several methods might throw exceptions based on given conditions:

- **`IllegalArgumentException`**: If the provided text, properties, or dimensions are null or if certain constraints are violated (e.g., negative font size, invalid gradient specifications, etc.).


# Java-Looper

### Looper - Game Loop Utility

The `Looper` class facilitates the creation of game loops or any other loop that requires running a method at a fixed frame rate. It wraps the loop logic inside a dedicated thread, ensuring that the target frame rate is achieved as closely as possible.

**Usage:**  
To utilize the `Looper`, instantiate it with the method of the class you want to call continuously. The Looper will automatically begin executing the loop upon instantiation.

**Example:**  
```java
Looper myLooper = new Looper(this, "myUpdateMethod", 60);
```
This will call `myUpdateMethod` in the current object at approximately 60 frames per second.

**Note:**  
This class leverages Java's reflection capabilities to call the desired method. While powerful, reflection introduces some runtime overhead. Therefore, performance-critical applications might require an alternative implementation approach.

- [Reflection in Java](https://www.oracle.com/technical-resources/articles/java/javareflection.html)
- [Runnable Interfaces in Java](https://docs.oracle.com/javase/8/docs/api/java/lang/Runnable.html)

**Author:** Hunter  
**Version:** 1.0  
**Since:** 2022-12-3
