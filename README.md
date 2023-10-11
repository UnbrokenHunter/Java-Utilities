Java-Vector2
Utilities.Vector2

public class Vector2
Represents a 2D vector with x and y coordinates using ints.

Class Overview
The Vector2 class provides operations for creating, manipulating, and querying 2D vectors. The class supports basic vector operations such as addition, subtraction, multiplication, and division. It also provides utility methods to calculate the magnitude and distance between two vectors.

Field Summary
public static final Vector2 one
A constant vector with values (1, 1).

public static final Vector2 zero
A constant vector with values (0, 0).

public static final Vector2 up
A constant vector pointing upwards, with values (0, 1).

public static final Vector2 down
A constant vector pointing downwards, with values (0, -1).

public static final Vector2 left
A constant vector pointing left, with values (-1, 0).

public static final Vector2 right
A constant vector pointing right, with values (1, 0).

public int x
The x-coordinate of the vector.

public int y
The y-coordinate of the vector.

Constructor Summary
public Vector2()
Default constructor. Initializes the vector to (0, 0).

public Vector2(int x, int y)
Initializes the vector with the given x and y coordinates.

Method Summary
public static Vector2 add(Vector2 vector1, Vector2 vector2)
Returns a new vector resulting from the addition of two vectors.

public static Vector2 subtract(Vector2 vector1, Vector2 vector2)
Returns a new vector resulting from subtracting the second vector from the first one.

public static Vector2 multiply(Vector2 vector, int scalar)
Returns a new vector by multiplying the vector by the given scalar.

public static Vector2 divide(Vector2 vector, int scalar)
Returns a new vector by dividing the vector by the given scalar.

public Vector2 plus(Vector2 vector2)
Returns a new vector by adding the given vector to the current one.

public Vector2 minus(Vector2 vector2)
Returns a new vector by subtracting the given vector from the current one.

public Vector2 mult(int num)
Multiplies the components of the vector by the given number.

public Vector2 div(int num)
Divides the components of the vector by the given number.

public double magnitude()
Computes the magnitude (length) of the vector.

public static double distance(Vector2 start, Vector2 end)
Calculates the Euclidean distance between two vectors.

public Vector2 binarize()
Binarizes the components of the vector.

public int hashCode()
Returns a hash code value for the vector.

public boolean equals(Object obj)
Compares the vector with another object for equality.

public String toString()
Returns a string representation of the vector.

Notes
The Vector2 class does not handle floating point inaccuracies and might not be suitable for high precision requirements. Also, the division method does not handle division by zero.

Exceptions
Various methods throw exceptions based on the following conditions:

IllegalArgumentException: If the vectors provided are null where they shouldn't be, or if scalar value is zero during division.

