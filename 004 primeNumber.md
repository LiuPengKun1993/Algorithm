# 是否是质数

**给定一个整数，判断它是否是质数。**

### JAVA 实现

```
public static  boolean isPrimeNumber (int num) {
    int tmp = num - 1;
    for(int i= 2; i <= tmp; i++) {
        if (num % i == 0) {
            return false;
        }
    }
    return true ;
}
```


### Swift 实现
```
func isPrimeNumber(num: Int) -> Bool {
    let tmp = num - 1
    for i in 2...tmp {
        if (num % i == 0) {
            return false
        }
    }
    return true
}
```