JSHint文档汉化版
=================

## JSHint options

JSHint有两种类型的options：强制型和宽松型，前者使JSHint更加严格，后者用来抑制一些警告.


#### 一. 强制型
  
##### * bitwise
    
    作用：值为true时，禁止使用位操作符，如"^，|，&"等.
    
##### * camelcase
  
    作用：值为true时，变量名必须使用驼峰风格（如"loginStatus"）或UPPER_CASE风格（如"LOGIN_STATUS"）.
    
##### * curly
    
    作用：值为true时，不能省略循环和条件语句后的大括号.
    
    备注：如"if (con) ..."，需要写成"if (con) { ... }".
    
##### * eqeqeq
    
    作用：值为true时，禁止使用"=="和"!="，而应该使用"==="和"!==".
    
##### * es3
    
    作用：值为true时，表示你的代码需要遵守ECMAScript 3规范.
    
##### * forin
    
    作用：值为true时，在所有"for in"循环中，必须使用hasOwnPropery过滤掉对象继承来的成员.
    
##### * immed
    
    作用：???.
    
##### * indent
    
    作用：该选项要求你的代码必须使用指定的tab缩进宽度，如"indent:4".
    
##### * latedef
    
    作用：值为true时，禁止在变量定义之前使用它.
    
##### * newcap
    
    作用：值为true时，构造函数名需要大写. 
    
    备注：经测试，该选项是否激活，JSHint都不会检查构造函数名.
    
##### * noarg
    
    作用：值为true时，禁止使用arguments.caller与arguments.callee.
    
##### * noempty
    
    作用：值为true时，不允许代码中出现空的语句块（"{}"）.
    
##### * nonew
    
    作用：值为true时，禁止使用产生副作用的构造器调用方式，如"new MyConstructor();".
    
##### * plusplus
    
    作用：值为true时，禁止使用一元递增（"++"）和递减（"--"）运算符.
    
##### * quotmark
    
    作用：该选项用于统一代码中的引号风格，可选的值有三个：
          (1) single -- 只能使用单引号；
          (2) double -- 只能使用双引号；
          (3) true -- 两者任选其一，但不能同时出现.
    
##### * undef
    
    作用：值为true时，禁止使用未定义的变量.
    
##### * unused
    
    作用：该选项激活后，对于"已定义却未使用的变量"会给出警告，可选的值有三个：
          (1) vars -- 只检查变量，不检查函数形参；
          (2) strict -- 检查变量和函数形参；
          (3) true -- 检查变量和函数形参，但允许这种情况：一个未使用的形参后紧随一个被使用的形参.
          
    示例：strict与true的区别
          (1) strict
              function show(x,y) {alert(y);}  // jshint校验结果：'x' is defined but never used
              show(1);
          
          (2) true
              function show(x,y) {alert(y);} // jshint校验结果：pass
              show(1); 
        
##### * strict
    
    作用：
 

#### 二. 宽松型

