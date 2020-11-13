# Day 1: Time Complexity Quiz

1. Multiple-choice

Calculate the time complexity for the following code. We've included both JS and Ruby for the same function.

<h3>JavaScript</h3>
<pre>
<code>
function logLetter(string) {
  for (const letter of string) {
    console.log(letter);
  }
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def log_letter(string)
  string.chars.each { |letter| puts letter }
end
</code>
</pre>

- O(n)
  - Correct! The runtime directly correlates to the length of the string. The loop is the weakest link and the number of iterations depends on the string's length.
- O(1)
  - Not quite. The function doesn't run in constant time - its runtime will change for different string lengths.
- O(n<sup>2</sup>)
  - Not quite. This is a lot slower than our function. Note that the function doesn't contain a nested loop or other markers that would indicate quadractic time.
- O(log n)
  - Not quite. Our function is slower than this.
- I don't know
  - That's OK! With study and practice, you'll get there.

2. Multiple choice

Calculate the time complexity for the following code. We've included both JS and Ruby for the same function.

<h3>JavaScript</h3>
<pre>
<code>
function findIndexOfElement(array, target) {
  return array.indexOf(target);
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def find_index_of_element(array, target)
  array.index(target)
end
</code>
</pre>

- O(n)
  - Correct! The runtime directly correlates to the length of the array. The array method that searches for the element will look through the entire array in the worst case.
- O(1)
  - Not quite. The function doesn't run in constant time - its runtime will change for different array lengths.
- O(n<sup>2</sup>)
  - Not quite. This is a lot slower than our function. Note that the function doesn't contain a nested loop or other markers that would indicate quadractic time.
- O(log n)
  - Not quite. Our function is slower than this.
- I don't know
  - That's OK! With study and practice, you'll get there.

3. Multiple Choice

Calculate the time complexity for the following code. We've included both JS and Ruby for the same function.

<h3>JavaScript</h3>
<pre>
<code>
function badCounting(array) {
  let count = 0;

  array.forEach((value, idx) => {
    array.forEach((testValue, testIdx) => {
      if (testIdx !== idx && value === testValue) {
        ++count;
      }
    });
  });

  return count / 2;
}
</code>
</pre>

<h3>Ruby</h3>
<pre>
<code>
def bad_counting(array)
  count = 0

  array.each_with_index do |value, idx|
    array.each_with_index do |testValue, testIdx|
      if testIdx != idx && testValue == value
        count += 1
      end
    end
  end

  count
end
</code>
</pre>

- O(n<sup>2</sup>)
  - Perfect! There is a nested loop in this code, and it iterates over the entire array for every single element in the input array.
- O(n)
  - Not quite. This function is a lot slower than this. How many total iterations will occur for an array of 3 items.
- O(1)
  - Not quite. The function doesn't run in constant time - its runtime will change for different array lengths.
- O(log n)
  - Not quite. Our function is slower than this.
- I don't know
  - That's OK! With study and practice, you'll get there.
