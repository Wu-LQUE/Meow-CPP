# Meow Wu Obfuscator

GPT-5生成的C++~~混淆~~工具。

## 简介

这是一个由 GPT-5 生成的 C++ 代码处理工具，它会将源代码中的关键字、标识符、数字等替换为 "喵" (Meow) 和 "呜" (Wu) 的组合。

生成的代码看起来像是猫叫，但实际上通过头部插入的宏定义，它仍然是完全合法的、可编译的 C/C++ 代码！

## 使用方法

### 1. 编译工具

```bash
g++ meow_wu_obfuscator.cpp -o meow_wu_obfuscator -O3
```

### 2. 运行工具

```bash
./meow_wu_obfuscator <输入文件> [输出文件]
```

如果未指定输出文件，结果将打印到标准输出。

### 3. 示例

仓库中包含了一个 `test.c` 文件作为测试用例。

```bash
# 转换 test.c 并保存为 test_meow.c
./meow_wu_obfuscator test.c test_meow.c

# 编译生成的“喵呜”代码 (它仍然可以正常工作！)
gcc test_meow.c -o test_meow

# 运行程序
./test_meow
```

## 效果展示

原始代码 (`test.c`):
```c
int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}
```

转换后的代码 (片段):
```c
#define 喵呜 int
#define 喵喵喵 factorial
// ... 更多宏定义 ...

喵呜 喵喵喵(喵呜 喵呜喵) {
    // ... 喵喵呜呜 ...
}
```

## 注意事项

- 本工具仅供娱乐和学习使用。
- 生成的代码虽然可编译，但可读性极差（这正是目的！）。
