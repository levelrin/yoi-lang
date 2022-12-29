# Condition

Users can write conditional statements like this:
```yoi
user, do you have apple?
  yes: user, eat apple
  no: user, buy apple
```

The above is the same as the following in Java:
```java
if (user.doYouHaveApple()) {
    user.eatApple();
} else {
    user.buyApple();
}
```

---

Here is another example:
```yoi
user, do you have the item?
  item: "apple"
  yes: user, eat apple
  no: user, buy apple
```

The above is the same as the following in Java:
```java
if (user.doYouHaveTheItem("apple")) {
    user.eatApple();
} else {
    user.buyApple();
}
```

## Multiple Conditions

Users can have multiple conditions like this:
```yoi
user 1, do you have apple?
and do you have banana?
or user 2, do you have orange?
  yes:
    user 1, eat your fruit
    user 2, eat your fruit
  no: user 3, buy fruits 
```

The above is the same as the following in Java:
```java
if (user1.doYouHaveApple && user1.doYouHaveBanana || user2.doYouHaveOrange) {
    user1.eatYourFruit();
    user2.eatYourFruit();
} else {
    user3.buyFruits();
}
```

Here are the important notes:
1. There is no `not` operator.
2. It's either `if` or `else`.
3. Users can omit the object name if it's used consecutively.
4. `and` must comes before `or`.
