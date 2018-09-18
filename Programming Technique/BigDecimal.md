# BigDecimal

When your decimal is too big and you want to minimize it

> Works well with **currency**





**Example:**

```java
double value = .12;
double sum = 3*.12;

System.out.print(sum);
```

> 0.036000000000000004

**What if we just want to display as `0.036`**



## Step by Step

1. `import java.math.BigDecimal`

2. Convert `value` to `string`

   - Why?

   - Iet say if you don't convert and keep the original value 

     ```java
     double value = .12;
     BigDecimal newVal = new BigDecimal(value);
     System.out.print(newVal);
     ```

     > 0.0120000000000000002498001805406602215953171253204345703125

   **If we convert to `string`**

   ```java
   double value = .12;
   String strVal = Double.toString(value); // "0.12"
   BigDecimal newVal = new BigDecimal(value);
   System.out.print(newVal)
   ```

   > 0.12

3. Use method `.add()` for `BigDecimal`

   - Why?
     - Because it's not compatible with normal operations.

   ```java
   double value = .12;
   String strVal = Double.toString(value); // "0.12"
   BigDecimal newVal = new BigDecimal(value);
   BigDecimal newSum = newVal.add(newVal).add(newVal);
   System.out.print(newSum);
   ```

   > 0.036