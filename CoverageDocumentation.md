# Writing Effect Tests for Better Code Coverage 
## 1.Boundary Value Testing

**Description:** Ensure your tests cover input values at the boundaries of acceptable ranges to catch edge cases.

**Snippet:**
```kotlin
fun calculate(input: Int): Int {
    return if (input > 0 && input < 100) {
        input * 2
    } else {
        throw IllegalArgumentException("Input must be between 0 and 100")
    }
}
```

**Test:**
```kotlin
@Test
fun testBoundaryValues() {
    assertEquals(0, calculate(0))
    assertEquals(200, calculate(100))
    assertThrows(IllegalArgumentException::class.java) {
        calculate(-1)
    }
    assertThrows(IllegalArgumentException::class.java) {
        calculate(101)
    }
}
```

## 2.Condition Coverage

**Description:** Validate that both true and false conditions in your code are tested thoroughly.

**Snippet:**
```kotlin
fun isValidInput(input: Int): Boolean {
    return input >= 0
}
```

**Test:**
```kotlin
@Test
fun testConditionCoverage() {
    assertTrue(isValidInput(10))
    assertFalse(isValidInput(-5))
}
```

## 3.Decision Coverage

**Description:** Verify that all possible outcomes of conditional statements are tested.

**Snippet:**
```kotlin
fun isValidRange(number: Int): Boolean {
    return number in 1..10
}
```

**Test:**
```kotlin
@Test
fun testDecisionCoverage() {
    assertTrue(isValidRange(5))
    assertFalse(isValidRange(15))
}
```

## 4.Loop Testing

**Description:**  Test loops with both minimum and maximum iterations to ensure correct behavior.

**Snippet:**
```kotlin
fun calculateSum(numbers: List<Int>): Int {
    var sum = 0
    for (number in numbers) {
        sum += number
    }
    return sum
}
```

**Test:**
```kotlin
@Test
fun testLoopBehavior() {
    assertEquals(10, calculateSum(listOf(1, 2, 3, 4)))
    assertEquals(0, calculateSum(emptyList()))
}
```

## 5.Exception Handling

**Description:** Check that exceptions are handled appropriately within your code.

**Snippet:**
```kotlin
fun processInput(input: Int) {
    if (input < 0) {
        throw IllegalArgumentException("Input cannot be negative")
    }
    // Process input...
}
```

**Test:**
```kotlin
@Test(expected = IllegalArgumentException::class)
fun testExceptionHandling() {
    processInput(-5)
}
```

## 6.Overflow Testing

**Description:** Evaluate how your software handles situations where variables exceed their limits.

**Snippet:**
```kotlin
fun add(a: Int, b: Int): Int {
    return a + b
}
```

**Test:**
```kotlin
@Test
fun testOverflowHandling() {
    assertEquals(Int.MAX_VALUE, add(Int.MAX_VALUE, 1))
    assertEquals(Int.MIN_VALUE, add(Int.MIN_VALUE, -1))
}
```
