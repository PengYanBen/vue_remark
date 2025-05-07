# 类型全解
一系列值及可以对其执行的操作

eg:

> boolean类型包含所有布尔值(只有两个:true和false)，以及可以对布尔值执行的操作(例如|、&&和!)。

> number类型包括所有数字，以及可以对数字执行的操作(例如+、-、/、%、|、&&和?)，还有可以在数字上调用的方法，例如.toFixed、.toPrecision、.tostring等。

> string类型包括所有字符串，以及可以对字符串执行的操作(例如+、|和&&)，还有可以在字符串上调用的方法，例如.concat和.toUpperCase。

## 3.2 类型

### 3.2.1 any
```
let a: any = 666 // any
let b: any = ['danger'] // any
let c = a + b // any 不会报错
```    
注意，正常情况下第三个语句将报错(谁会计算一个数字和一个数组的和呢?)，但是却没有，因为我们告诉TypeScript，相加的两个值都是any类型。如果想使用any,一定要显式注解。倘若TypeScript推导出值的类型为any(例如忘记注解函数的参数，或者引入没有类型的JavaScript模块)，将抛出运行时异常，在编辑器中显示一条红色波浪线。显式把a和b的类型注解为any(:any)，TypeScript便不会抛出异常，因为这样做就是告诉TypeScript，你知道自己在做什么。

#### TSC 标志:nolmplicitAny ####
默认情况下，TypeScript很宽容，在推导出类型为any时不会报错。如果想让TypeScript在遇到隐式any类型时报错，请在isconfig.json中启用noImplicitAny 标志。
noImplicitAny隶属于TSC的strict标志家族

### 3.2.2 unknown

unknown类型支持哪些操作呢?unknown类型的值可以比较(使用==、===、11、&&和?)、可以否定(使用!)、(与其他任何类型一样)可以使用JavaScript的typeof和instanceof运算符细化。unknown的用法如下:
```
let a: unknown = 30 // unknown
let b = a === 123 // boolean

let c = a + 10 
// Error T2571:0bject is of type 'unknown'

if(typeof a =='number'){
    let d = a + 10 // number
}


```

通过这个示例，我们大致可以了解unknown的用法:
1.TypeScript不会把任何值推导为unknown类型，必须显式注解(a)注1

2.unknown 类型的值可以比较(b)
但是执行操作时不能假定unknown类型的值为某种特定类型(c)，必须

3.先向TypeScript证明一个值确实是某个类型(d)

### 3.2.3 boolean
```
let a = true // boolean
var b = false // boolean
const c = true // true
let d: boolean = true // boolean
let e: true = true // true
let f: true = false // Error TS2322:Type 'false' is not assignable  to type 'true'.
```
这个示例表明我们可以通过多种方式告诉TypeScript一个值的类型为boolean :
1.可以让 TypeScript推导出值的类型为 boolean(a和b)
2.可以让 TypeScript推导出值为某个具体的布尔值(c)
3.可以明确告诉TypeScript，值的类型为boolean(d)
4.可以明确告诉TypeScript，值为某个具体的布尔值(e和f)

### 3.2.4 any
### 3.2.5 any
### 3.2.6 any
### 3.2.7 any