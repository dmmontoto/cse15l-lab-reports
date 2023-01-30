# Lab Report 2
## By David Montoto

### Part 1

### Part 2: arrayList Bug

* Below are two failure-inducing inputs as JUnit tests. They are for the two buggy methods provided in ArrayExamples.java, `reverseInPlace()` and `reversed()`.

```
@Test
public void testReverseInPlace2() {
  int[] input1 = {1, 2, 3, 4, 5};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{5, 4, 3, 2, 1}, input1);
}

@Test
public void testReversed1() {
  int[] input1 = {1, 2, 3, 4};
  assertArrayEquals(new int[]{4, 3, 2, 1}. ArrayExamples.reversed(input1));
}
```

* Below are two inputs as JUnit tests, that do not induce a failure. The first test, for `reverseInPlace()`, fails to point out the bug because the array has a signle element, and the sympton is the same as the input. Test two, for `reversed()`, fails to point out the bug because the input is an emtpy array, and so is the symptom.

```
@Test
public void testReverseInPlace() {
  int[] input1 = { 3 };
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[]{ 3 }, input1);
}

@Test
public void testReversed() {
  int[] input1 = { };
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
```

* Below are the symptoms for `testReverseInPlace2()` and `testReversed1()`. In `testReverseInPlace2()`, the symptom you see in the terminal is `arrays first differed at element [3]; expected: <2> but was: <4>`. In `testReversed1()`, the symptom you see in the terminal is `arrays first differed at element [0]; expected: <4> but was:«0>`.

### Part 3
