# Proxy

Proxy 对象用于创建一个对象的代理，从而实现基本操作的拦截（如属性查找、赋值、枚举、函数调用等）。

## 语法

```js
const p = new Proxy(target, handler)
```

### 参数

#### `target`

要使用 `Proxy `包装的目标对象（可以是任意类型的对象，包括原生数组，函数，甚至另一个代理）。

#### `handler`

一个通常以函数作为属性的对象，各属性中的函数分别定义了在执行各种操作时代理 `p` 的行为。

## 方法

#### proxy.revocable()

创建一个可撤销的 `Proxy` 对象。

### handler 对象的方法

`handler` 对象是一个容纳一批属性的占位符对象。它含有 `Proxy`的各个捕获器(trap)。

所有的捕捉器都是可选的。如果没有定义某一个捕捉器，就会保留源对象的默认行为。

#### `handler.getPrototypeOf()`

Object.getPrototypeOf 方法的捕捉器。

#### `handler.setPrototypeOf()`

Object.setPrototypeOf 方法的捕捉器。

#### `handler.isExtensible()`

Object.isExtensible 方法的捕捉器。

#### `handler.preventExtensions` 

Object.preventExtensions 方法的捕捉器。

#### `handler.getOwnPropertyDescriptor()`

Object.getOwnPropertyDescriptor 方法的捕捉器。

#### `handler.defineProperty()`

Object.defineProperty 方法的捕捉器。

#### `handler.has()`

`in` 操作符的捕捉器。

#### `handler.get()`

属性读取操作的捕捉器。

#### `handler.set()`

属性设置方法的捕捉器。

#### `handler.deleteProperty()`

delete 操作符的捕捉器。

#### `handler.ownKeys()`

Object.getPropertyNames 方法和 Object.getOwnPropertySymbols 方法的捕捉器。

#### `handler.apply()`

函数调用操作的捕捉器。

#### `handler.construct`

`new` 操作符的捕捉器。

## 示例

```js
const handler= {
	// 拦截
	get: (obj, prop) => {
		console.log('get拦截', 'prop:', prop)
		return prop in obj ? obj[prop] : 'test'
	},
	set: (obj, prop, value) =>{
		console.log('set拦截', 'prop:', prop, 'value:', value)

		switch (prop) {
			case 'money':
				if ( !Number.isInteger(value) ) {
					throw new TypeError('money字段必须为整数')
				}
				break;
			default:
        obj[prop] = value
		}
	},
	deleteProperty: (obj, prop, value) => {
		console.error(`delete 拦截: 删除了 prop 属性`)
		if ( obj.deletedProperties && obj.deletedProperties.length ) {
			obj.deletedProperties.push(prop)
		} else {
			obj.deletedProperties = [prop]
		}
	}
}

const p = new Proxy({}, handler)
p.a = 1
p.money = 1
```











