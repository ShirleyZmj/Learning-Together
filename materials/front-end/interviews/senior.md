# 阿娟蛋分享的高级前端面试题
## 面试题1
1. 针对单个文件上传如何知道上传进度？
2. 分块是如何进行分的，根据什么来进行分的，分的是依赖还是 chunk
3. 按需引入的背后逻辑是什么？
4. 那单入口它你刚刚说的那个引用次数你知道指的是什么吗？
5. resolve 有几种模式，几种方法
6. 移动端适配的方式有几种
7. 你会更推荐使用 vw 还是 rem
8. webpack 的 loader 的机制是什么？
9. webpack 使用的是什么模块？AMD、UMD
10. webpack 的插件系统是什么？
11. 前端动画实现的方式主要有哪几种？
12. 如何判断是否为可迭代对象
13. 如何将可迭代对象转为数组
14. watch 调用了多少次
15. 回答下列的值：
try{
  Promise.reject(1)
}catch(err){
  console.log(1)
}
16. 回答下列的值：
async()=>{
  try{
    await Promise.reject(1)
  }catch(err){
    console.log('err',err)
  }
}
17. 回答下列的值
Promise.resolve(Promse.reject(1))
Promise.reject(Promse.resolve(1))
18. async/await 底层实现的原理是什么？
19. yeild/generage 底层实现的原理是什么？


## 笔试题
1. 给定一个选择器的树形结构，每个树形都有name，ischecked，和children，children为数组，是下一级的数组，你需要对每个节点的children排序，要求ischecked为第一关键字，如果为true则排在前面，name为第二关键字升序
。返回一颗新树

2. 瀑布图的数据是一个span数组，每个数组有starttime和endtime两个字段。你需要将数组分割成不连续的多个块，每个块的持续时间就可以反应出用户的体感响应时间。不连续是指：对于任意两个块A和B，A中的任何一个span在时间轴上都不会与B中的任何一个span有任何重叠。对于span端点有重叠的场景，例如[1,5]和[5,10]我们认为它连续。请你按照时间从早到晚，输出每个块的持续时间。数据保证按照span的起始时间升序。使用js

## 面试题2
1. tailwindcss 的优势在哪里？
2. scss 与 less 的区别，scss 对比与 less 的优势有哪些？
3. 对函数式编程的理解，你还理解其他的编程范式吗？面向对象编程范式
4. 常用的数组 API
5. 数组去重对象，将重复的 id 进行一个去重
6. for 循环实现 reduce
7. 说说你对 Promise 的理解，它的 API、它的实现原理
8. webpack 构建打包优化，你在项目中都做了什么？
9. 单点登录 SSO，你主要做了什么，怎么样实现了单点登录
10. vue3 中是如何使用 proxy 来进行代理的？
11. vue3 对比 vue2 做了哪些东西，为什么要做这些东西？
12. 说说你知道的 React的内容
