# What is code coverage?

In software engineering, code coverage, also called test coverage, is a percentage measure of the degree to which the source code of a program is executed when a particular test suite is run. A program with high code coverage has more of its source code executed during testing, which suggests it has a lower chance of containing undetected software bugs compared to a program with low code coverage.[1][2] Many different metrics can be used to calculate test coverage. (According to wiki)

What is Code Coverage?
Code coverage measures how much of your code is tested when you run your tests. It tells you if all parts of your code are checked to make sure they work correctly. High code coverage means most of your code is tested, so there are fewer chances of bugs.

Example:
Suppose you have a Kotlin function to check if a number is positive or negative:

```
fun checkNumber(n: Int): String {
    return if (n >= 0) "Positive" else "Negative"
}
```

You write a test to check if this function works:

```
import org.junit.Test
import kotlin.test.assertEquals

class NumberTest {
    @Test
    fun testPositiveNumber() {
        assertEquals("Positive", checkNumber(4))
    }
}
```

This test checks if checkNumber(4) returns "Positive". However, you didn't write a test to check if the function correctly identifies negative numbers. This means only part of your code is tested.

Code Coverage Report:

Green: Code that is tested (e.g., the positive number check).
Red: Code that is not tested (e.g., the negative number check).
Since you only tested one part of the function, your code coverage is 50%.

Why is Code Coverage Important?
High code coverage ensures most of your code is tested, reducing the chances of bugs. It helps keep your code stable, even as you make changes, making it easier to release updates automatically. The goal is to achieve 100% code coverage, meaning every part of your code is tested.