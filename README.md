# design_pattern
# 23种设计模式
## 一、分类
### 创建型模式(5)
#### 主要用于创建对象
- **工厂方法模式**：延迟到子类来选择实现
  - 优点：向客户端隐藏具体产品类被实例化这一细节，创建一个新产品时，只需要提供创建产品的工厂，无需关注创造细节，甚至不需要了解产品了的类名；创建一个新产品时，只需要增加具体工厂类和产品类，而不需修改原有代码，符合开放封闭原则。
  - 缺点：创建一个新产品时，需要增加具体工厂类和产品类，系统中类的数量会成对增加，会增加系统的复杂性。
- **抽象工厂模式**：选择产品族的实现
- **建造者模式**：分离整体算法构建和部分构造
- **原型模式**：克隆生成对象
  - 优点：简化对象的创建过程，提高效率。
  - 缺点：不符合开放封闭原则，每个类都需要配备克隆方法，扩展困难。
- **单例模式**：控制实例数目
  - 优点：每个类只创建一个对象，节约资源；可以控制创建实例的数目。
  - 缺点：单例类的职责过多，不符合单一职责原则。

### 结构型模式(7)
#### 主要用于处理类和对象的组合
- 适配器模式
- 桥接模式
- 组合模式
- 装饰模式
- 外观模式
- **享元模式**：分离与共享
  - 优点：极大减少内存中对象的数量，使得相同对象或相似对象在内存中只保存一份。
  - 缺点：需要分离内部状态和外部状态，程序逻辑复杂化。
- **代理模式**：控制对象访问
  - 优点：代理模式协调了调用者和被调用者，在一定程度上降低了系统的耦合。
  - 缺点：实现代理模式需要额外的工作，所以有些代理模式会变得很复杂。
### 行为模式(11)
#### 主要用于描述对类或对象怎样交互和怎样分配职责
- 责任链模式
- 命令模式
- 中介者模式
- 备忘录模式
- 观察者模式
- 状态模式
- 策略模式
- 模板方法模式
- 访问者模式
- ~~迭代器模式~~
- ~~解释器模式~~
## 二、设计模式的定义
设计模式是一套被反复使用、多数被人知晓的、经过分类编目的、代码设计经验的总结，使用设计模式是为了重用代码、让代码更容易被他人理解、提高代码的可靠性。

## 三、设计模式的优点
- 提高软件系统的开发和软件质量，在一定程度上节约设计成本。
- 使得设计方案更加灵活，且易于修改。

## 四、设计模式的两大主题
**系统复用与系统扩展**
