# Binary Search （二分查找）

### JAVA 实现

```
class Solution {
    public int search(int[] nums, int target) {
    if (nums.length == 0){
        return -1;
    }
    int low = 0;
    int high = nums.length - 1;
    while (low <= high) {
        int middle = (high - low) / 2 + low;
        if (nums[middle] == target) {
            return middle;
        } else if (nums[middle] > target){
            high = middle - 1;
        } else {
            low = middle + 1;
        }
    }
    return -1;
    }
}
```

### Swift 实现
```
class Solution {
    func search(_ nums: [Int], _ target: Int) -> Int {
    if (nums.count == 0) {
        return -1
    }
    var low = 0
    var high = nums.count - 1
    while (low <= high) {
        let middle = (high - low) / 2 + low
        if (nums[middle] == target) {
            return middle
        } else if (nums[middle] > target) {
            high = middle - 1
        } else {
            low = middle + 1
        }
    }
    return -1
    }
}
```