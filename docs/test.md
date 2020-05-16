# 特殊语法

## tip

```markdown
!!! info "tip"

    **Tips：** 这样子。
```

### 参数

* warning
* danger
* info
* note

### 效果

!!! info "tip"

    **Tips：** 这样子。



## 代码 tab

```markdown
​```javascript tab="代码"
let count = 0;
count++;
console.log(count);
​```

​```javascript tab="结果"
count++;
​```
```

### 效果

```javascript tab="代码"
let count = 0;
count++;
console.log(count);
```

```javascript tab="结果"
count++;
```

## question

```markdown
??? question "1 + 1 = ?"

    ​```javascript
    console.log(1 + 1);
    ​```

		**Tips：**
	
		- What a good question!!
```

### 效果

??? question "1 + 1 = ?"

    ```javascript
    console.log(1 + 1);
    ```
    
    **Tips：**
    
    - What a good question!!