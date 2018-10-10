# css预编译处理：less

- css和javascript相比: css是静态的,没有变量、函数

- less文件.less > 通过less工具编译成 > css文件.css

- 常用语法: 定义变量、后代选择器、文件引用、函数

  - 定义变量:

  ``` less
  @bgColor: #000;

  .frame {
      background-color: @bgColor;
  }
  ```

  - 后代选择器:

  ``` less
  .frame {
      background-color: @bgColor;
      // .frame .select
      .select {
          width: 100px;
      }
      // .frame:after
      &:after {
          content: "";
      }
  }
  ```

  - 文件引用

  ``` less
  @import "文件名"
  ```

  - 函数

  ``` less
  .fun(@px) {
      height: @px;
  }

  .frame {
      .fun(123px);
  }
  ```