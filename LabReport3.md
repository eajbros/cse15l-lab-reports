# Lab Report 3
---
## Part One - Bugs
## Associated Code
```java
public class ArrayExamples {
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
}
```
## Failure Inducing Input
```java
 @Test
 public void testAverageWithoutLowestTwoLowest() {
   double[] input = {1.5, 3.0, 5.0, 8.5, 1.5};
   assertEquals(4.5, ArrayExamples.averageWithoutLowest(input), 0.00001);
 }
```
## Non-Failure Inuducing Input
```java
@Test
 public void testAverageWithoutLowestOneLowest() {
   double[] input = {1.5, 2.0, 4.5, 8.5};
   assertEquals(5.0, ArrayExamples.averageWithoutLowest(input), 0.00001);
 }
```
## Symptom
![symptom](SymptomAverage.png)
## The fix of the bug
### Before:
```java
public class ArrayExamples {
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    for(double num: arr) {
      if(num != lowest) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
}
```
### After:
```java
public class ArrayExamples {
  static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowestIndex = 0;
    for(int i = 0; i < arr.length; i++) {
      if(arr[i] < arr[loewstIndex]) { lowestIndex = i; }
    }
    double sum = 0;
    for(int i = 0; i < arr.length; i++) {
      if(i != lowestIndex) { sum += num; }
    }
    return sum / (arr.length - 1);
  }
  }
}
```
This fix stores the index of the lowest value instead of the value itself. This allows the program to only remove the one lowest number it picks instead of every number that has that same value.
## Part Two - `grep` research
## `\|` option
### Directory:
```
etjenkins@ETHANLAPTOP:/mnt/c/Users/eajcu/Documents/VS Code Files/docsearch/technical$ grep -r 'inseminate\|ultrastructural' biomed
biomed/1471-2121-2-10.txt:          We have performed ultrastructural analysis by SEM of
biomed/1471-2121-2-10.txt:          ultrastructural features of the cytoskeleton,
biomed/1471-2121-2-22.txt:        ultrastructural immunogold labeling techniques especially
                                --- A lot of lines ---
biomed/1472-6793-2-17.txt:          thin filaments and had many of the ultrastructural
biomed/1472-6793-2-17.txt:          The overall ultrastructural organization of the
```
This option used with a directory searches through every line in every file in the directory returning lines that either have the string inseminate OR ultrastructural. This is useful because it allows us to search for multiple strings in just one command line.

### File:
```
etjenkins@ETHANLAPTOP:/mnt/c/Users/eajcu/Documents/VS Code Files/docsearch/technical$ grep "interventions\|clinical" biomed/1468-6708-3-1.txt
        whom risk factors, subclinical disease, and morbidity are
        modification interventions in older adults.
        significantly greater than zero. A clinical trial of a
          Implications for clinical trials
          interventions for older adults who were merely overweight
          would appear to be fruitless since the interventions
          outcome in evaluations of interventions such as diet or
          interventions such as weight-loss drugs may be harmful [
          outcome measure. Both YOL and YHL would be clinically
        YHL as the outcome measure in clinical trials involving
```
This option used with a file searches through every line a file returning lines that either have the string interventions OR clinical. This is useful because it allows us to search for multiple strings in just one command line.
