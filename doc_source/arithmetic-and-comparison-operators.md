# Arithmetic and Comparison Operators<a name="arithmetic-and-comparison-operators"></a>

You can use the following arithmetic and comparison operators in calculated fields:

+ Addition \(\+\)

+ Subtraction \(\-\)

+ Multiplication \(\*\)

+ Division \(/\)

+ Equal \(=\)

+ Not equal \(<>\)

+ Greater than \(>\)

+ Greater than or equal to \(>=\)

+ Less than \(<\)

+ Less than or equal to \(<=\)

+ AND

+ OR

+ NOT

Equal \(=\) and not equal \(<>\) comparisons are case\-sensitive\. For example, if the condition is `state = 'WA'` and the value in the field is **wa**, those values are not considered to be equivalent\.

You can determine the order in which operators are applied by using parentheses\. For example, in the following statement the addition statement is processed first, and then the result is multiplied by three, returning a value of 36\.

```
(5 + 7) * 3
```

In the following statement, the multiplication statement is processed first, and then the result is added to five, returning a value of 26\.

```
5 + (7 * 3)
```

## Examples<a name="operator-example"></a>

The following example uses multiple arithmetic operators to determine a sales total after discount\.

```
({quantity} * {sales amount}) - {discount amount}
```

The following example uses multiple conditional operators to identify top customers in Washington or Oregon for a promotion\.

```
ifelse(((State = 'WA' OR State = 'OR') AND {Number of orders} > 10), 'Special offer', 'n/a')
```