---
lang: en
title: 'LCOV - coverage.dat - math/FloatExtensions.kt'
---

+-----------------------------------------------------------------------+
| LCOV - code coverage report                                           |
+-----------------------------------------------------------------------+
| ![](../glass.png){width="3" height="3"}                               |
+-----------------------------------------------------------------------+
|   ---------------------------------                                   |
| -------- ------------------------------------------------------------ |
| --------------------------------------------------------------------- |
| ---------------------------- -- ------------ ----- ------- ---------- |
|   Current view:                                                       |
|            [top level](../index.html) - [math](index.html) - FloatExt |
| ensions.kt[ (source / [functions](FloatExtensions.kt.func-sort-c.html |
| ))]{style="font-size: 80%;"}                   Hit   Total   Coverage |
|   Test:                                                               |
|              coverage.dat                                             |
|                                                                       |
|                                     Lines:       1     3       33.3 % |
|   Date:                                                               |
|              2024-04-02 21:43:31                                      |
|                                                                       |
|                                     Functions:   1     3       33.3 % |
|   Legend:                                                             |
|                    Lines: [hit]{.coverLegendCov} [not hit]{.coverLege |
| ndNoCov}                                                              |
|                                                                       |
|   ![](../glass.png){width                                             |
| ="3" height="3"}                                                      |
|                                                                       |
|                                                                       |
|   ---------------------------------                                   |
| -------- ------------------------------------------------------------ |
| --------------------------------------------------------------------- |
| ---------------------------- -- ------------ ----- ------- ---------- |
+-----------------------------------------------------------------------+
| ![](../glass.png){width="3" height="3"}                               |
+-----------------------------------------------------------------------+

+-----------------------------------------------------------------------+
| \                                                                     |
+-----------------------------------------------------------------------+
| ``` {.sourceHeading}                                                  |
|           Line data    Source code                                    |
| ```                                                                   |
|                                                                       |
| ``` {.source}                                                         |
|        1             : package org.oppia.android.util.math            |
|        2             :                                                |
|        3             : import kotlin.math.abs                         |
|        4             :                                                |
|        5             : /**                                            |
|        6             :  * The error margin used for a                 |
| pproximately [Float] equality checking, that is, the largest distance |
|        7             :  * from any particular number b                |
| efore a new value will be considered unequal (i.e. all values between |
|        8             :  * a float and (fl                             |
| oat-interval, float+interval) will be considered equal to the float). |
|        9             :  *                                             |
|       10             :  * Note that the machine epsilo                |
| n value from https://en.wikipedia.org/wiki/Machine_epsilon is defined |
|       11             :  * defined as the smallest v                   |
| alue that, when added to, or subtract from, 1, will result in a value |
|       12             :  * that is exactly equa                        |
| l to 1. A larger value is picked here for more allowance in variance. |
|       13             :  */                                            |
|                                                                       |
|      14             : const val FLOAT_EQUALITY_EPSILON: Float = 1e-6f |
|       15             :                                                |
|       16             : /**                                            |
|       17             :                                                |
| * The error margin used for approximately [Double] equality checking. |
|       18             :  *                                             |
|       19                                                              |
|   :  * See [FLOAT_EQUALITY_EPSILON] for an explanation of this value. |
|       20             :  */                                            |
|                                                                       |
|    21             : const val DOUBLE_EQUALITY_EPSILON: Double = 1e-13 |
|       22             :                                                |
|       23             : /**                                            |
|       24             :  * Returns whether this f                      |
| loat approximately equals another based on a consistent epsilon value |
|       25             :  * ([FLOAT_EQUALITY_EPSILON]).                 |
|       26             :  */                                            |
|       27                                                              |
|           : fun Float.isApproximatelyEqualTo(other: Float): Boolean { |
|                                                                       |
|  28           0 :   return abs(this - other) < FLOAT_EQUALITY_EPSILON |
|       29             : }                                              |
|       30             :                                                |
|       31             : /**                                            |
|       32             :  * Returns whether this do                     |
| uble approximately equals another based on a consistent epsilon value |
|       33             :  * ([DOUBLE_EQUALITY_EPSILON]).                |
|       34             :  */                                            |
|       35                                                              |
|         : fun Double.isApproximatelyEqualTo(other: Double): Boolean { |
|                                                                       |
| 36           1 :   return abs(this - other) < DOUBLE_EQUALITY_EPSILON |
|       37             : }                                              |
|       38             :                                                |
|       39             : /**                                            |
|       40             :  * Returns a string representa                 |
| tion of this [Double] that keeps the double in pure decimal and never |
|       41                                                              |
|        :  * relies on scientific notation (unlike [Double.toString]). |
|       42             :  */                                            |
|       43           0                                                  |
| : fun Double.toPlainString(): String = toBigDecimal().toPlainString() |
| ```                                                                   |
+-----------------------------------------------------------------------+

\

  ---------------------------------------------------------------------------------
  ![](../glass.png){width="3" height="3"}
  Generated by: [LCOV version 1.14](http://ltp.sourceforge.net/coverage/lcov.php)
  ---------------------------------------------------------------------------------

\
