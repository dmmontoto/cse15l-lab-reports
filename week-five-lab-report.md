# Lab Report 3
## By David Montoto

### Alternative and Unique Ways of Utilizing `grep`

* `grep -Rl` 

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

