# Task 2 - Leo 入门：学会这门语言 

请将本文件复制到 `learn/YourName/` 文件夹中，填写你的答案后提交 PR。
 

## 问题

**Q1. Leo 中的 "Private by Default"（默认隐私）语义是什么？**

A:在 Leo 语言中，所有的变量、函数参数和计算过程默认都是私密的（Private），外界无法查看。

---

**Q2. Tuple 包含 array structs 的示例，以及如何访问 struct 中的元素。**

A:// 定义一个包含 array (数组) 的 struct
struct MyStruct {
    data: [u8; 2]
}
// 创建一个 Tuple，里面包含上面定义的 struct 和一个普通的 u8 变量
let my_tuple: (MyStruct, u8) = (MyStruct { data: [1u8, 2u8] }, 5u8);
使用点号来访问
let first_num: u8 = my_tuple.0.data[0u8]; 
// .0 访问 Tuple 第一项，.data 访问 struct 字段，[0u8] 访问数组第一个元素
---

**Q3. Aleo record 中 owner 字段的作用是什么？**

A:owner 字段用于证明这条记录的所有权。它里面存放的是一个 Aleo 钱包地址，只有掌握对应私钥的人，才有权限解密、使用或消耗这条 Record

---

**Q4. 程序中的 final 是什么？**

A:finalize 是 Leo 程序中用来更新链上公开状态（Public State）的代码块
---

**Q5. 如何创建 helper functions（辅助函数）？**

A:使用 function 关键字

---

**Q6. helper functions 能否创建 records？**

A:不能

---

**Q7. constructor 的目的是什么？**

A:定义程序的升级逻辑

---

**Q8. 如何组合多个 interfaces（接口）？**

A:通过继承的方式来组合

---

**Q9. record interface 中 `..` 的含义是什么？**

A:允许存在额外字段

---

**Q10. 何时使用 dyn record（动态 record）？**

A:当进行动态调用，即在编译时无法确定具体要调用哪个程序时使用,因为目标程序的具体 record 结构在编译时是未知的，所以使用 dyn record

---

**Q11. storage vector 支持的核心操作有哪些？**

A:push(value): 向数组末尾添加一个新元素,get(index): 获取指定索引位置的元素,set(index, value): 更新/修改指定索引位置的元素
