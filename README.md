# Explain Skill

用小白能理解的语言，逐行解释任意代码文件或代码段。

## 功能

输入 `/explain <文件路径或代码>`，即可获得：

- **基础语法**：这行代码在语法层面做了什么
- **运行逻辑**：程序执行到这里实际发生了什么
- **关键知识**：为什么要这样写，背后的设计意图

## 安装

将 `SKILL.md` 放入你的 Claude Code skills 目录：

```
~/.claude/skills/explain/SKILL.md
```

## 使用示例

```
/explain src/utils.ts
/explain "const doubled = nums.map(n => n * 2)"
```

## 输出格式

```
📄 文件：src/utils.ts
语言：TypeScript

━━━━━━━━━━━━━━━━━━━━━━

【第 1-3 行】
function add(a: number, b: number): number {
  return a + b;
}

📝 基础语法：
  - `function` 声明函数
  - `(a: number, b: number)` 参数及类型
  - `return` 返回计算结果

⚙️ 运行逻辑：
  调用 add(2, 3) 时，a=2, b=3，计算得 5 并返回。

💡 关键知识：
  - TypeScript 编译时检查类型
  - 纯函数无副作用，易于测试
```

## 原则

1. **不用术语吓人** — 术语附带通俗解释
2. **关联生活场景** — 用日常事物类比抽象概念
3. **标注隐藏逻辑** — 指出隐式转换、短路求值等陷阱
4. **由浅入深** — 先讲做什么，再讲为什么
5. **控制长度** — 每块解释 3-5 点

## License

MIT
