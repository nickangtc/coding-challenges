# [Cyclic rotation](https://codility.com/programmers/lessons/1-iterations/)

### Solution (Ruby)
[Test Score: 100%](https://codility.com/demo/results/trainingDACSW8-UN3/)

```rb
def solution(a, k)
  # Exit as early as possible if input array is empty, or K is 0.
  if a.length == 0 || k == 0
    return a
  else
    # Move last element to the front K times.
    k.times do
      temp = a.pop
      a.unshift(temp)
    end
    return a
  end
end
```
