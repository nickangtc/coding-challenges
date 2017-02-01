# [Odd occurrences in Array](https://codility.com/programmers/lessons/2-arrays/)

### Solution (Ruby)
[Test Score: 100%](https://codility.com/demo/results/trainingRWKTN9-N9T/)

```rb
def solution(a)
  hash = {}

  # Map every element to a key-value pair.
  a.each do |x|
    hash[x] ? hash[x] += 1 : hash[x] = 1
  end

  # Find the odd numbered value and return that key.
  hash.each do |key, val|
    if val % 2 != 0
      # exit as soon as an odd value is found,
      # since it is assumed input array only has 1 unpaired element.
      return key
    end
  end
  puts "Error, #{a} has no unpaired element!"
end
```
