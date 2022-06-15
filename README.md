# 23种设计模式
## 一、分类
### 创建型模式(5)
#### 主要用于创建对象
- **工厂方法模式**：延迟到子类来选择实现
  - **作用**：定义一个用于创建产品的接口，由子类决定生产什么产品。 
  - 何时使用?
    - 如果一个类需要创建一个接口的对象，但是又不知道具体的实现，使用工厂方法模式把创建对象工作延迟到子类去实现。
    - 如果一个类本身就希望由它的子类来创建所需对象。 
  - 优点：
    - 向客户端隐藏具体产品类被实例化这一细节，创建一个新产品时，只需要提供创建产品的工厂，无需关注创造细节，甚至不需要了解产品类的类名。
    - 创建一个新产品时，只需要增加具体工厂类和产品类，而不需修改原有代码，符合开放封闭原则。
  - 缺点：
    - 创建一个新产品时，需要增加具体工厂类和产品类，系统中类的数量会成对增加，会增加系统的复杂性。
  - 工厂方法模式与简单工厂模式
    - 工厂方法模式实现时，客户端需要觉得是实例化哪个工厂，有选择判断的问题，工厂方法把简单工厂的内部逻辑判断转移到了客户端代码来进行。 
    - 工厂方法类的核心是一个抽象工厂类，而简单工厂模式把核心放在一个具体类上。
- **抽象工厂模式**：选择产品族的实现
  - **作用**：提供一个创建产品族的接口，其每个子类可以生产一系列相关的产品。
  - 优点：
    - 符合开放封闭原则。增加新的具体工厂类无需修改已有代码。
    - 符合单一职责原则。将生成产品的代码抽取到同一位置，使得代码易于维护。
    - 可以避免客户端和具体产品代码的耦合。
    - 可以确保同一工厂生成产品相互匹配。
  - 缺点： 
    - 引入众多的类和接口，代码会很复杂。
    - 不太容易扩展新的产品。
- **建造者模式**：分离整体算法构建和部分构造
  - **作用**：将一个复杂对象分解成多个相对简单的部分，然后根据不同需要分别创建它们，最后构建成该复杂对象。 
  - 优点
    - 客户端不必知道产品内部的组成细节，将产品本身和产品的创建过程解耦，使得相同的创建过程可以创建出不同的对象。
    - 可以更加精细地控制产品的创建过程。将复杂产品的创建步骤分解在不同的方法中，使得创建过程更加清晰，也更加方便使用程序来控制创建过程。
    - 增加新的具体建造者无需修改原有类库代码，符合开放封闭原则。
  - 缺点
    - 建造者模式所创建的产品一般都具有较多共同点，其组成部分相似。如果产品的差异性较大，则不适合建造者模式，因此其使用范围限制。
    - 如果产品内部变化复杂，可能会导致需要定义很多具体建造者来实现这种变化，导致系统变得庞大臃肿。   
- **原型模式**：克隆生成对象
  - **作用**：将一个对象作为原型，通过对其进行复制而克隆出多个和原型类似的新实例。
  - 优点：
    - 简化对象的创建过程，提高效率。
  - 缺点：
    - 每个类都需要配备克隆方法，对已有类改造不符合开放封闭原则。
    - 带有引用对象的类进行克隆时需要深克隆，使系统变得复杂。
- **单例模式**：控制实例数目
  - **作用**：某个类只能生成一个实例，该类提供了一个全局访问点供外部获取该实例。
  - 优点：
    - 每个类只创建一个对象，节约资源
    - 可以控制创建实例的数目。
  - 缺点：
    - 单例类的职责过多，不符合单一职责原则。

### 结构型模式(7)
#### 主要用于处理类和对象的组合
- **适配器模式**：转换匹配，复用功能
  - **作用**：将一个类的接口转换成客户希望的另外一个接口，使得原本由于接口不兼容而不能一起工作的那些类能一起工作。
  - 优点：
    -  将目标类和适配者类解耦，通过引入适配器类重用现有适配者类，而无需修改原有代码。
    -  增加了类的透明性和复用性，将具体的实现封装在适配者中，对于客户端是透明的，且提高了适配者的复用性。
    -  更好的灵活性和扩展性。
  - 缺点：
    - 代码整体复杂度增加。 
- **桥接模式**：分离抽象和实现
  - **作用**：将抽象与实现分离，使它们可以独立变化。它是用组合聚合关系代替继承关系来实现，从而降低了抽象和实现这两个可变维度的耦合度。
  - 优点：
    - 分离抽象和实现部分。
    - 桥接模式有类似多继承的方案，但是多继承不符合单一职责且类太多，桥接模式是一种比多继承更好的方案，符合合成复用原则。
    - 具有良好的可扩展性，符合开放封闭原则，在两个维度中任何一个维度增加产品都不需要修改原有代码。
    - 实现对用户透明，对用户隐藏细节，用户不需要关心实现，在抽象层通过聚合关联关系完成封装和对象的组合。
  - 缺点：
    - 桥接模式的引入增加了系统的理解和设计维度。
- **组合模式**：统一叶子对象和组合对象。
  - **作用**：将对象组合成树状层次结构，使用户对单个对象和组合对象具有一致的访问性。
  - 优点：
    - 增加新的元素无需修改原有代码，符合开放封闭原则。
    - 统一了叶子对象和组合对象，客户端调用简单，无需关注自己创建的是叶子对象还是组合对象。 
  - 缺点：
    - 在添加时，很难限制组件(组合对象)的类型，需要检测组件类型的时候，使得我们不能依靠编译期的类型约束来完成，必须在运行期间动态检测。 
- **装饰模式**：动态组合，动态是手段，组合是目的
  - **作用**：动态的给对象增加一些职责，即增加其额外的功能。
  - 优点：
    - 装饰模式与继承关系都是扩展对象的功能，但是装饰模式可以提供比继承关系更加的灵活。
    - 通过使用不同装饰类的排列组合，可以创造出不同行为的组合。 
  - 缺点： 
    - 会产生很多细粒度对象。 
- **外观模式**：封装交互，简化调用
  - **作用**：为多个复杂的子系统提供一个一致的接口，使这些子系统更加容易被访问。
  - 优点：
    - 实现了子系统和客户端的松耦合关系，当子系统发生变化时，无需通知客户端，由外观类直接调用。 
  - 缺点： 
    - 增加新的子系统需要修改外观类，不符合开放封闭原则。
- **享元模式**：分离与共享
  - **作用**：运用共享技术来有效地支持大量细粒度对象的复用。
  - 优点：
    - 极大减少内存中对象的数量，使得相同对象或相似对象在内存中只保存一份。
  - 缺点：
    - 需要分离内部状态和外部状态，程序逻辑复杂化。
- **代理模式**：控制对象访问
  - **作用**：为某对象提供一种代理以控制对该对象的访问。即客户端通过代理间接地访问该对象，从而限制、增强或修改该对象的一些特性。 
  - 优点：
    - 代理模式协调了调用者和被调用者，在一定程度上降低了系统的耦合。
  - 缺点：
    - 实现代理模式需要额外的工作，所以有些代理模式会变得很复杂。
### 行为模式(11)
#### 主要用于描述对类或对象怎样交互和怎样分配职责
- 责任链模式
- 命令模式
- 中介者模式
- **备忘录模式**：保存和恢复内部状态
  - **作用**：：在不破坏封装性的前提下，获取并保存一个对象的内部状态，以便以后恢复它。
  - 优点：
  - 缺点：
- 观察者模式
- 状态模式
- 策略模式
- 模板方法模式
- **访问者模式**：预留通路，回调实现。
  - **作用**：在不改变集合元素的前提下，为一个集合中的每个元素提供多种访问方式，即每个元素有多个访问者对象访问。**将数据结构和数据操作分离。**
  - 优点：
    -  增加新的访问操作无需修改原有代码，符合开放封闭原则。
    -  将有关的行为集中到一个访问者对象中，而不是分散到一个个的节点元素类中。
  - 缺点：
    - 增加新的元素很困难。每增加一个新的元素就要在抽象访问者种增加一个新的抽象操作，并每个每个具体访问者类中增加相应的具体操作。
    - 破环封装。访问者模式要求访问者对象访问并调用每一个元素对象的操作，这意味着元素对象有时候暴露一些自己的内部操作和内部状态，否则无法供访问者访问。
- ~~迭代器模式~~
- ~~解释器模式~~
## 二、设计模式的定义
设计模式是一套被反复使用、多数被人知晓的、经过分类编目的、代码设计经验的总结，使用设计模式是为了重用代码、让代码更容易被他人理解、提高代码的可靠性。

## 三、设计模式的优点
- 提高软件系统的开发和软件质量，在一定程度上节约设计成本。
- 使得设计方案更加灵活，且易于修改。

## 四、设计模式的两大主题
**系统复用与系统扩展**
