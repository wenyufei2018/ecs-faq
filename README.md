该仓库是 [ecs-faq](https://github.com/SanderMertens/ecs-faq) 的翻译。

## About Author 
He's the author of [Flecs](https://github.com/SanderMertens/flecs), an Entity Component System for C & C++. He's always experimenting with better ways to implement ECS features, and write about it if I can. If you're interested in discussing ECS, [join the Discord](https://discord.gg/BEzP5Rgrrp)!

## General Questions

- [什么是 ECS？](#什么是-ECS)
- [ECS 的普遍定义？](#ECS-的普遍定义)
- [为什么使用 ECS？](#为什么使用-ECS)
- [谁使用 ECS？](#谁使用-ECS)
- [ECS 和 OOP 的区别是什么？](#ECS-和-OOP-的区别是什么)
- [ECS 和 Entity-Component 的区别是什么？](#ECS-和-Entity-Component-的区别是什么)
- [ECS 难学么？](#ECS-难学么)
- [ECS 是一个底层的抽象么？](#ECS-是一个底层的抽象么)
- [ECS 需要写更多的代码么？](#does-ecs-require-writing-more-code)
- [ECS 对 low-level code 有用吗？](#ECS-对-low-level-code-有用吗)
- [ECS 可以用任何语言实现吗？](#ECS-可以用任何语言实现吗)
- [我应该自己编写 ECS 吗？](#我应该自己编写-ECS-吗)
- [ECS 更快么？](#ECS-更快么)
- [ECS 代码是否更可复用？](#ECS-代码是否更可复用)
- [ECS 适合多线程吗？](#ECS-适合多线程吗)
- [ECS 可以在游戏之外使用吗？](#ECS-可以在游戏之外使用吗)
- [如何开始使用ECS？](#如何开始使用ECS)
- [如何设计 ECS？](#如何设计-ECS)
- [实现 ECS 的不同方式有哪些？](#实现-ECS-的不同方式有哪些)
- [如何修改 Component？](#如何修改-Component)
- [Entity 如何与 System 匹配？](#Entity-如何与-System-匹配)
- [什么是 entity relationships？](#什么是-entity-relationships)

## How-to
- [在 ESC 中如何创建一个 hierarchy？](#在-ESC-中如何创建一个-hierarchy)
- [在 ECS 中如何存储 spatial data？](#在-ECS-中如何存储-spatial-data)

## Data Oriented Design Questions
- [什么是面向数据的设计？](#什么是面向数据的设计)
- [ECS 与 DoD 是否相同？](#ECS-与-DoD-是否相同)
- [什么是随机 RAM？](#什么是随机-RAM)
- [什么是 CPU cache？](#什么是-CPU-cache)
- [什么是 cache line？](#什么是-cache-line)
- [什么是 locality of reference?](#什么是-locality-of-reference?)
- [什么是 SIMD？](#什么是-SIMD)
- [什么是 vectorization？](#什么是-vectorization)
- [什么是 false sharing？](#什么是-false-sharing)
- [什么是 AoS?](#什么是-aos)
- [什么是 SoA?](#什么是-soa)
- [什么是 branch prediction?](#什么是-branch-prediction)

## Glossary
- [Entity](#entity)
- [Component](#component)
- [Tag](#tag)
- [System](#system)
- [Query](#query)
- [World](#world)
- [Registry](#registry)
- [Table](#table)
- [Archetype](#archetype)

## ECS frameworks
The current list includes both open and closed source ECS implementations, and engines that have adopted ECS pattern. Projects that had no activity in the past year are not included.

- [AFRAME](https://aframe.io) (HTML5/JS, MIT)
- [Artemis](https://github.com/junkdog/artemis-odb) (Java, custom license)
- [Bevy ECS](https://github.com/bevyengine/bevy) (Rust, MIT)
- [Dominion](https://github.com/dominion-dev/dominion-ecs-java) (Java, MIT)
- [Ecsact](https://ecsact.dev) (MIT)
- [EntityX](https://github.com/alecthomas/entityx) (C++11, MIT)
- [Entitas](https://github.com/sschmid/Entitas-CSharp) (C#, MIT)
- [Entitas-Redux](https://github.com/jeffcampbellmakesgames/Entitas-Redux) (C#, MIT)
- [EnTT](https://github.com/skypjack/entt) (C++17, MIT)
- [Esper](https://github.com/benmoran56/esper) (Python, MIT)
- [Fireblade](https://github.com/fireblade-engine/ecs) (Swift, MIT)
- [Flecs](https://github.com/SanderMertens/flecs) (C/C++11, [C#](https://github.com/flecs-hub/flecs-cs), [Rust](https://github.com/jazzay/flecs-rs), [Zig](https://github.com/prime31/zig-flecs), [Lua](https://github.com/flecs-hub/flecs-lua), MIT)
- [Hecs](https://github.com/Ralith/hecs) (Rust, Apache/MIT)
- [Legion](https://github.com/amethyst/legion) (Rust, MIT)
- [LeoECS](https://github.com/Leopotam/ecs) (C#, MIT)
- [Mach ECS](https://github.com/hexops/mach) (Zig, MIT, Apache)
- [Nu](https://github.com/bryanedds/Nu) (F#, MIT)
- [Photon Quantum](https://doc.photonengine.com/en-us/quantum/current/getting-started/quantum-intro) (C#, Commercial license)
- [Shipyard](https://github.com/leudz/shipyard) (Rust, Apache/MIT)
- [Specs](https://github.com/amethyst/specs) (Rust, Apache/MIT)
- [Svelto](https://github.com/sebas77/Svelto.ECS) (C#, MIT)
- [tiny-ecs](https://github.com/bakpakin/tiny-ecs) (Lua, MIT)
- [Unity DOTS](https://unity.com/dots) (C#, Commercial license)
- [Unreal Mass](https://docs.unrealengine.com/5.0/en-US/overview-of-mass-entity-in-unreal-engine/) (C++, Commercial license)
- [Zig ECS](https://github.com/prime31/zig-ecs) (Zig, MIT)
- [luaecs](https://github.com/cloudwu/luaecs) (C/Lua, MIT)

## Resources
- [Overwatch Gameplay Architecture and Netcode](https://www.youtube.com/watch?v=W3aieHjyNvw) (Blizzard, GDC)
- [Data-Oriented Design and C++](https://www.youtube.com/watch?v=rX0ItVEVjHc) (Mike Acton, CppCon)
- [CPU caches and why you care](https://vimeo.com/97337258) (Scott Meyers, NDC)
- [Building a fast ECS on top of a slow ECS](https://youtu.be/71RSWVyOMEY) (UnitOfTime, Youtube)
- [Culling the Battlefield: Data Oriented Design in Practice](https://www.gdcvault.com/play/1014491/Culling-the-Battlefield-Data-Oriented) (DICE, GDC)
- [Game Engine Entity/Object systems](https://www.youtube.com/watch?v=jjEsB611kxs) (Bobby Anguelov, presentation)
- [Understanding Data Oriented Design for Entity Component Systems](https://www.youtube.com/watch?v=0_Byw9UMn9g) (Unity, GDC)
- [Understanding Data Oriented Design](https://learn.unity.com/tutorial/part-1-understand-data-oriented-design?courseId=60132919edbc2a56f9d439c3&signup=true&uv=2020.1) (Unity, Tutorial)
- [Data Oriented Design](https://www.dataorienteddesign.com/dodbook/dodmain.html) (Richard Fabian, book)
- [Entities, Components and Systems](https://medium.com/ingeniouslysimple/entities-components-and-systems-89c31464240d) (Mark Jordan, blog)
- [Awesome Entity Component System](https://github.com/jslee02/awesome-entity-component-system) (Jeongseok Lee, link collection)
- [Why Vanilla ECS is not enough](https://ajmmertens.medium.com/why-vanilla-ecs-is-not-enough-d7ed4e3bebe5) (Sander Mertens, blog)
- [Formalisation of Concepts behind ECS and Entitas](https://medium.com/@icex33/formalisation-of-concepts-behind-ecs-and-entitas-8efe535d9516) (Maxim Zaks, blog)
- [Entity Component System and Rendering](https://ourmachinery.com/post/ecs-and-rendering/) (Our Machinery, blog)
- [Specs and Legion, two very different approaches to ECS](https://csherratt.github.io/blog/posts/specs-and-legion/) (Cora Sherrat, blog)
- [Where are my Entities and Components](https://ajmmertens.medium.com/building-an-ecs-1-where-are-my-entities-and-components-63d07c7da742) (Sander Mertens, blog)
- [Archetypes and Vectorization](https://medium.com/@ajmmertens/building-an-ecs-2-archetypes-and-vectorization-fe21690805f9) (Sander Mertens, blog)
- [Building Games with Entity Relationships](https://ajmmertens.medium.com/building-games-in-ecs-with-entity-relationships-657275ba2c6c) (Sander Mertens, blog)
- [Making the most of Entity Identifiers](https://ajmmertens.medium.com/doing-a-lot-with-a-little-ecs-identifiers-25a72bd2647) (Sander Mertens, blog)
- [Why Storing State Machines in ECS is a Bad Idea](https://ajmmertens.medium.com/why-storing-state-machines-in-ecs-is-a-bad-idea-742de7a18e59) (Sander Mertens, blog)
- [ECS back & forth](https://skypjack.github.io/2019-02-14-ecs-baf-part-1/) (Michele Caini, blog series)
- [Sparse Set](https://www.geeksforgeeks.org/sparse-set/) (Geeks for Geeks)
- [Hibitset](https://docs.rs/hibitset/0.6.3/hibitset/) (DOCS.RS)

## General Questions

### 什么是 ECS
ECS ("Entity Component System") 是一种通过 **将数据与行为分离** 来提高代码可重用性的设计方法。数据通常以 cache-friendly 的方式存储，从而提高性能。ECS 由 System 、 Entity 和 Component 构成。

- Entity 用于唯一标识
- Component 是没有行为的纯数据类型
- Entity 可以包含一个或者多个 Component
- Entity 可以动态的更新 Component
- System 是 与具有特定 Component集合 的 Entity 相匹配的功能

### ECS 的普遍定义
在实践中，ECS 的使用更加自由。有些 ECS 框架没有 System ，只提供查询 Entity 的方法；有些框架可能允许向 Entity 添加非 Component 的内容。

一个框架，允许向 Entity 添加东西，并且有 查询具有某些东西的 Entity 的方法，通常被认为是 ECS。

### 为什么使用 ECS？
ECS 在游戏开发者中越来越受欢迎的原因有很多：

- ECS 通常可以支持更多的游戏对象
- ECS 代码更易于重用
- ECS 代码更易于扩展新功能
- ECS 允许更动态的编码风格

### 谁使用 ECS？

- [Unity DOTS](https://unity.com/dots) (Engine)
- [Unreal (Sequencer)](https://www.unrealengine.com/en-US/tech-blog/performance-at-scale-sequencer-in-unreal-engine-4-26) (Engine)
- [Our Machinery](https://ourmachinery.com/) (Engine)
- [Photon Quantum](https://doc.photonengine.com/en-us/quantum/current/getting-started/quantum-intro) (Engine)
- [Bevy](https://bevyengine.org/) (Engine)
- [Amethyst](https://amethyst.rs/) (Engine)
- [Overwatch](https://playoverwatch.com/en-us/) (Game, uses custom ECS)
- [Xenonauts](https://store.steampowered.com/app/223830/Xenonauts/) (Game, uses custom ECS)
- [Survival City](https://play.google.com/store/apps/details?id=com.playstack.survivalcity&hl=en&gl=US) (Game, uses Entitas)
- [Penko Park](https://store.steampowered.com/app/852090/Penko_Park) (Game, uses Entitas)
- [Doomsday Vault](https://apps.apple.com/us/app/doomsday-vault/id1457773760) (Game, uses Entitas)
- [Phantom Brigade](https://www.youtube.com/watch?v=uHsh9kWQeDc&ab_channel=BraceYourselfGames) (Game, uses Entitas)
- [Minecraft Bedrock](https://minecraft.gamepedia.com/Bedrock_Edition) (Game, uses EnTT)
- [War of Rights](https://store.steampowered.com/app/424030/War_of_Rights/) (Game, uses EnTT)
- [ArcGIS](https://developers.arcgis.com/arcgis-runtime/) (Framework, uses EnTT)
- [Aether Engine](https://hadean.com/spatial-simulation/) (Framework, uses EnTT)
- [FastSuite](https://www.fastsuite.com/) (Simulation, uses EnTT)
- [RoboCraft](https://robocraftgame.com/) (Game, uses Svelto)
- [GameCraft](https://store.steampowered.com/app/1078000/Gamecraft/) (Game, uses Svelto)
- [CardLife](http://cardlifegame.com/) (Game, uses Svelto)
- [Bebylon](https://bebylon.world/) (Game, uses Flecs)
- [The Forge](https://github.com/ConfettiFX/The-Forge) (Rendering Engine, uses Flecs)
- [Territory Control](https://store.steampowered.com/app/690290/Territory_Control_2/) (Game, uses Flecs)
- [Sol Survivor](https://nicok.itch.io/sol-survivor-demo) (Game, uses Flecs)

### ECS 和 OOP 的区别是什么？
ECS 通常被认为是 OOP 的替代方案。虽然 ECS 和 OOP 重叠，但在应用程序的设计方式上有差异：

- 继承是 OOP 中的一等公民，组合是 ECS 中的一等公民。
- OOP 鼓励封装数据， ECS 鼓励公开 POD(plain old data) 对象。
- OOP 将数据与行为放在一起(class)，ECS 将数据和行为分离。
- OOP 对象实例是单一的静态类型，ECS Entity 可以有多个动态变化的 Component

应该注意的是，有些人认为 ECS 符合面向对象设计的特点（参见https://www.gamedev.net/blogs/entry/2265481-oop-is-dead-long-live-oop/)，因此 ECS 应被视为 OOP 的子集。

然而，在实践中，ECS 应用程序的设计过程与大多数人认为的 OOP 完全不同。因此，将其作为一种单独的设计方法至少是有用的。

### ECS 和 Entity-Component 的区别是什么？
令人困惑的是，ECS 和 Entity-Component 并不相同。通常在游戏引擎 中发现的 EC 与 ECS 相似，因为它们允许创建 Entity和 Component。然而，在 EC 中， Component 是同时包含数据和行为的类，行为直接在 Component 上执行。

一个简单的 EC 应该是这样的：

```cpp
class IComponent {
public:
    virtual void update() = 0;
};

class Entity {
    vector<IComponent*> components;
public:
    void addComponent(IComponent *component);
    void removeComponent(IComponent *component);
    void updateComponents();
};
```

在 EC 中构建特性通常意味着从 IComponent 接口继承，并从多个 Component 组成 Entity。EC 在实践中的一个例子是 Unity 的 GameObject 系统。

### ECS 难学么？
ECS 的少量概念和规则通常很容易学习。然而，正确应用它们需要练习。ECS设计的某些方面违背了直觉，尤其是对于当来自 OOP 背景的开发者。

有趣的是，一些用户报告说，一旦开始用 ECS，它就更容易编写、重用和扩展代码。

### ECS 是一个底层的抽象么？
不一定。虽然某些 ECS 设计可以利用低级别的机器优化，但为 ECS 编写的代码不一定比其他方法低或高。

### ECS 需要写更多的代码么？
对此没有单一的答案，并且高度依赖于所使用的 ECS 框架和 engine。

当一个 ECS 框架与一个 engine 集成时，它可以产生非常紧凑和简洁的代码，甚至比非 ECS 替代方案更短。

当 ECS 未与 engine 集成时，在 engine 类型和 ECS 之间桥接的粘合代码可能会导致应用程序不得不编写更多代码。

话虽如此，由于代码库更易于维护，编写 ECS 代码所花费的时间被节省的时间所抵消。

### ECS 对 low-level code 有用吗？
low-level code（如渲染和物理）可能希望使用底层硬件的高级功能(eg: vectorization)，同时优化 cache locality。一些 ECS 框架比其他框架更适合于此。

一般来说，当 ECS 提供 raw component arrays 的访问权限时，它更适合于 low-level 优化。另一个决定因素，ECS 在多线程这样的系统中更容易，特别是在现代游戏中。

> raw component arrays（原始组件数组）是指对组件数据进行连续存储的一种方式。具体地说，它是指将每个组件类型的实例存储在一个连续的数组中，使得它们在内存中是紧凑的

### ECS 可以用任何语言实现吗？
是

### 我应该自己编写 ECS 吗？
由于它的概念和规则很小，构建一个功能性的 ECS 并不难。构建自己的 ECS 有很多好处，比如可以自由添加新功能，以及只构建真正需要的功能。

然而，如果您编写自己的实现，您应该充分期望它不会超过已建立的实现。随着时间的推移，人们发明了许多技巧来在 ECS 操作中提供平衡的性能。它需要不断的实验和迭代。

正如许多事情一样，编写 ECS 很容易，但很难掌握。

### ECS 更快么？
通常是的。但这取决于所测量的内容以及 ECS 的实现。不同的实现会产生不同的权衡，因此，在一个框架中非常快的操作可能在另一个框架内非常慢。

ECS 实现通常擅长的是**线性查询**和**迭代 entities 集**，或者在**运行时动态更改 components**。ECS 实现通常不擅长的是需要高度专业化的数据结构（如二叉树或空间结构）的查询或操作。了解实现的权衡并利用其设计，可以确保您从 ECS 中获得最佳性能。

### ECS 代码是否更可复用？
是的。ECS 中的行为与一组 components 相匹配，而不是与 OOP 中的类紧密耦合。这有两个含义。

第一个是显而易见的。因为行为不绑定到单个类，所以它可以在不同类的 entities 之间复用。典型的例子是 move system，它与具有 速度components 和 速度components 的任何 entities 相匹配。这在其他 OOP 风格的设计中并非不可能实现，但这通常依赖于基于类的继承。继承有众所周知的问题，例如重构 class hierarchy 很困难，或者低级基类随着时间的推移会积累膨胀。

EC 框架可以提供类似级别的可重用性，其中 components 只是简单地添加到 entities 中。但是 ECS 的最大优势在于，可以在任何开发阶段引入新 system ，并将自动与具有正确 components 的任何新 entities 相匹配。这促进了一种设计，即 System 被开发为单一责任的小功能单元，可以轻松地跨不同项目的部署。

### ECS 适合多线程吗？
通常是的。数据和行为的分离使**识别单个系统和它们的依赖关系**以及**它们应该如何调度**变得更加容易。多线程的方法在不同的 ECS 实现之间有所不同，但大多数方法都使多线程代码更容易。

### ECS 可以在游戏之外使用吗？
是的。

### 如何开始使用ECS？
我强烈建议阅读 ECS 上的现有资源，并练习他们描述的方法。阅读示例 ECS 项目的代码也是快速理解 ECS 应用程序编写方式的好方法。

### 如何设计 ECS？
设计 ECS 应用程序首先要创建包含数据的 Component（数据结构）。需要考虑如下的点：

- 存在多少数据实例
- 访问数据的频率
- 数据突变的频率
- 何时需要访问/更新数据
- 哪些数据被一起访问/更新
- 数据的基数是多少

设计具有单一责任的 Component 和 System 是一种良好的做法。这使得它们更容易在项目中重用，并且更容易重构代码。

### 实现 ECS 的不同方式有哪些？
有许多不同的方式可以实现实体-组件系统（ECS），每种方式都具有特定的优点和缺点，具体取决于特定的用例。下面是一些常见的ECS实现方法，

#### Archetypes (aka "Dense ECS" or "Table based ECS")
Archetypes ECS 将 Entity 存储在 Table 中，其中 Component 是列， Entity 是行。 Archetypes 实现可以快速查询和迭代。

Examples of archetype implementations are [Flecs](https://github.com/SanderMertens/flecs), [Our Machinery](https://ourmachinery.com/), [Unity DOTS](https://unity.com/dots), [Unreal Sequencer](https://www.unrealengine.com/en-US/tech-blog/performance-at-scale-sequencer-in-unreal-engine-4-26), [Unreal Mass](https://docs.unrealengine.com/5.0/en-US/overview-of-mass-entity-in-unreal-engine/), [Bevy ECS](https://bevyengine.org/), [Legion](https://github.com/amethyst/legion) and [Hecs](https://github.com/Ralith/hecs).

#### Sparse set ECS (aka "Sparse ECS")
Sparse set ECS 将每个 Component 存储在其自己的 Sparse set 中，该 Sparse set 以 Entity id 为密钥。Sparse set 实现允许快速添加/删除操作。

Examples of sparse set implementations are [EnTT](https://github.com/skypjack/entt) and [Shipyard](https://github.com/leudz/shipyard).

#### Bitset based ECS
Bitset based ECS 将 Component 存储在数组中，其中 Entity id 用作索引，并使用 Bitset 指示 Entity 是否具有特定 Component。存在不同类型的基于 Bitset 的方法。一种方法是为每个 Component 设置一个数组，并附带一个位集，以指示哪些 Entity  具有该 Component。另一种方法使用[hibitset](#hibitset)数据结构（请参阅链接）。

Examples of bitset implementations are [EntityX](https://github.com/alecthomas/entityx) and [Specs](https://github.com/amethyst/specs).

#### Reactive ECS
Reactive ECS 使用由 Entity 突变产生的信号来跟踪哪些 Entity匹配 System/Queries

An example of a reactive ECS is [Entitas](https://github.com/sschmid/Entitas-CSharp).

### 如何修改 Component？
ECS通常有两种方式允许修改 Component，一种是通过修改单个 Entity 上的 Component，另一种是修改 System 中多个 Entity 的 Component。

第一种方法
```cpp
entity.set<Position>({10, 20});
```

第二种方法
```cpp
system<Position, Velocity>().each(
    [](entity e, Position& p, Velocity & v) {
        p.x += v.x;
        p.y += v.y;
    });
```

第二种方法通常更快，因为它需要更少的查找，并且可以利用高效的 Component 存储方法。

### Entity 如何与 System 匹配？
有三种流行的实现方法。

1. 在 Archetypes ECS 中，查询存储匹配 Table 的列表，其中 Table 可以包含许多 Entity。这种方法的优点是，随着 Table 快速稳定，查询评估开销平均减少到零。
2. 在 Sparse set 中，查询会迭代一个查询 Component （通常是 Entity 最少的 Component ）中的所有 Entity ，并测试每个后续 Component 是否有 Entity。Bitset based ECS 实现使用类似的方法。
3. 在 Reactive ECS 中，System 通过监听可能导致 Entity 匹配的信号来收集具有正确 Component 集合的 Entity。

### 什么是 entity relationships？
entity relationships 是 ECS 模型的扩展，在 ECS 模型中，除了添加 Component 之外，还可以向 Entity 添加一对对象。一个简单的关系示例可能如下：

```c
alice.add<Likes>(bob);
```

在本例中，"Likes, bob" 是一对，"Likes" 是一种 relationships，"bob" 是 relationship 目标。alice 和 bob 都是常规 Entity 。entity relationships 的更多信息，看 [this article](https://ajmmertens.medium.com/building-games-in-ecs-with-entity-relationships-657275ba2c6c).

## How-to

### 在 ESC 中如何创建一个 hierarchy？
有几种方法可以在 ECS 中实现 hierarchy，这取决于应用程序可以使用的 ECS 实现。在任何实现中都可以使用的一种方法是将 hierarchy 存储在 Component 中，如下所示：

```c
// Store the parent entity on child entities
struct Parent {
    entity parent;
};

// Store all children of a parent in a component with a vector
struct Children {
    vector<entity> children;
};

// Store children in linked list
struct ChildList {
    entity first_child; // First child of entity
    entity prev_sibling; // Previous sibling
    entity next_sibling; // Next sibling
};
```

这种方法的缺点是依赖于 Component 查找，会降低系统迭代 hierarchy 的速度。虽然这种方法很灵活，但对于低级系统（如 applying transforms）来说，这种方法并不理想。

如果应用程序只需要从上到下迭代 hierarchy ，一种特别有效的方法是根据 Entity 在 hierarchy 中的深度对其进行排序。这具有迭代的优点是速度快，缺点是它需要频繁的排序。

Archetype ECS 框架可能允许在不同的表中拆分子树。表/子树可以根据其深度进行排序。这样做的优点是迭代速度快，排序不频繁。但缺点是它会创建许多小表，降低性能。

### 在 ECS 中如何存储 spatial data？
四叉树和八叉树等 spatial data 通常不会直接存储在ECS中，因为它们的布局与典型的 ECS 布局不匹配。

一种与 ECS 相结合的 narrow-phase spatial 查询非常有效的方法是创建一个查询，该查询迭代相关 Entity 并将它们存储在每个帧开头（或结尾）的 spatial data 中。

对于 broad-phase spatial 查询，应用程序可以利用运行时标记（如果 ECS 支持），其中标记与空间网格中的单元格相对应。结合与标记匹配的查询，应用程序可以快速丢弃不在特定区域内的大量 Entity。

## Data Oriented Design

### 什么是面向数据的设计
维基百科将面向数据的设计定义为：

> ... 在视频游戏开发中，使用的一种 **激励 CPU缓存 有效使用** 的优化方法。这种方法是**关注数据布局**，**根据需要对字段进行分离和排序**，并**考虑数据的转换**。

面向数据的设计是大量技术和条件的统称。一般来说，他的目标是分析应用程序中不同类型数据的访问模式，并为这些访问模式选择数据结构，以最佳地利用底层硬件。**硬件优化**通常与（但不限于）**优化CPU缓存的使用**、**减少对 RAM（缓存未命中）的加载/存储**以及**SIMD 指令的使用**有关。

理查德·法比安（Richard Fabian）的《Data oriented design》一书全面介绍了面向数据设计：[https://www.dataorienteddesign.com/dodbook/](https://www.dataorienteddesign.com/dodbook/)

### ECS 与 DoD 是否相同？

不相同。

ECS 模式确实很适合 DoD，这就是为什么许多 ECS 框架（尽管不是所有框架）都具有 DoD 的存储设计。

如果 ECS 迭代 contiguous component arrays，则需要利用 DoD 原则和优化。

### 什么是随机 RAM？
RAM 是计算机通常拥有的一种内存，是存储应用程序及其代码的整个状态的地方。CPU 在执行应用程序代码时与 RAM 交换数据。

虽然 RAM 的绝对速度非常快，但 CPU 和 RAM 之间的总线可能会成为数据密集型应用程序的瓶颈。这就是为什么在面向数据的设计中，采用技术来最小化 RAM 的加载数量。

### 什么是 CPU cache？
CPU cache 是一种比 RAM 快得多，但也比 RAM 小得多的内存。当 CPU 从 RAM 加载数据时，它存储在 cache 中。

面向数据的设计采用尽可能有效地利用 CPU cache 的技术，从而使 RAM 的负载数量最小化。

### 什么是 cache line？
cache line 表示在一次加载中从 RAM 检索的数据量。当一个应用程序从 RAM 请求（比如4字节）时，CPU 将从请求的地址开始实际加载 64字节。

应用程序可以通过在附近存储数据来减少从 RAM 加载的次数，这增加了将来操作所需的数据已经加载到 cache 中的可能性。

### 什么是 locality of reference(Cache locality)?
locality 指时间或空间。时间局部性是指在短时间内重复使用数据。空间局部性是指存储位置的紧凑程度。由于 CPU 能够更好地预测访问模式，这两种类型中的高局部性都会提高缓存的效率。

Cache locality 是一个计算机程序中数据访问的一种现象，即程序重复访问彼此接近的数据，使这些数据存储在缓存内存或处理器缓存中。这提高了系统的速度、效率和性能，因为从缓存内存中访问数据比从主内存中访问数据快得多。

Cache locality 有两种类型: 时间局部性(Temporal Locality)和空间局部性(Spatial Locality)。

- 时间局部性指的是在计算机程序中，部分代码段的重复使用在一段时间内非常频繁，这些代码段被经常地访问和引用。这种局部性通常是指在一段时间内程序的执行中，只有少数指令或数据被频繁重复使用，这些指令或数据的局部性相对于程序中的其他指令或数据更强。
- 地址局部性指的是在程序访问内存时，指令或数据的地址以及其相邻地址上的数据将被频繁地访问。这种局部性通常是指在程序的执行中，只有少数内存地址被频繁地访问，这些地址的局部性也相对于内存中的其他地址更强。

通过优化cache locality，开发者可以显著提高程序的性能。他们可以通过重新排列他们的数据结构或使用利用数据访问模式的空间和时间局部性的算法来实现这一点。

### 什么是 SIMD？
SIMD（单指令多数据）是指一组指令或指令系列，可以在执行一条指令时，处理多个值。

### 什么是 vectorization？
vectorization（或 auto vectorization）是**满足特定标准的代码**使用 SIMD 指令来提高性能的过程。使用这些优化指令的结果是运行速度可以比常规代码快几倍。

vectorize 代码的条件是：

- 数据必须连续存储（在数组中）
- 代码不应包含分支或函数调用

编译器通常能够对满足上述条件的**循环**进行 vectorization。然而，这取决于编译器将自动 vectorization 哪些场景。[该网站](https://llvm.org/docs/Vectorizers.html)提供了 clang 编译器能够自动 vectorize 的场景概述。

### 什么是 false sharing？
当不同的线程尝试加载和更改两个不同但位于同一缓存行中的值时，会发生 false sharing。这会导致缓存同步，从而降低性能。

通过确保不同线程访问的数据不太接近，无法在单个 cache line 中加载，可以避免 false sharing。

### 什么是 AoS?
AoS, or "array of structs" 指包含多个字段的 struct 存储在 array 中的内存布局。如

```c
struct AoS {
  int m_1;
  int m_2;
};

AoS values[1000];
```

AoS的一个优点是数据存储在有利于缓存 locality 的数组中。AoS 的一个潜在缺点是，当代码只需要结构中的成员子集时，加载到 cache 中的数据比需要数据要多的多。

在 ECS 的上下文中，AoS 通常指所有 components 存储在相同 array 中的内存布局。

### 什么是 SoA?
SoA, or "struct of arrays" 指一个 struct 包含多个 array 的内存布局。如

```c
struct SoA {
  int m_1[1000];
  int m_2[1000];
};

SoA values;
```

与 AoS 一样，SoA 的数据存储在有利于缓存 locality 的数组中。SoA 的另一个优点是，当代码只需要结构中的成员子集时，其他成员不会加载到缓存中。SoA 的一个潜在缺点是，如果代码随机需要访问其他成员，它会导致比 AoS 更多的缓存未命中。

在 ECS 的上下文中，SoA 通常指 components 存储在 separate arrays 中的内存布局。

### 什么是 branch prediction?
当 CPU 执行一组指令时，它试图通过对条件语句（如if-else、switch）的求值方式进行有根据的猜测来预测代码将走哪条路径。这些指令随后被预加载到指令缓存中，甚至可以提前执行。

当代码包含许多不可预测的分支时，分支预测器可能经常不得不丢弃预先计算的结果，这会导致代码明显变慢。

## Glossary

### Entity
一个 Entity 在游戏中表示单个“事物”，通常用唯一的整数值标识。

### Component
一个 Component 是可以添加到 Entity 或从 Entity 中删除的数据类型。ECS 中的 Component 通常是没有封装的普通的数据类型。

### Tag
一个 Tag 是一个没有数据的 Component

### System
一个 System 是与具有特定 components集合 的 Entity 相匹配的可执行对象。

### Query
Query 类似于 System，但不能单独执行。

### World
一个 World 是所有 ECS 数据的容器。ECS 框架通常允许单个应用程序拥有多个 World。

### Registry
同 World

### Archetype
Archetype 是存储 Entities 的数据结构。Components 存储在连续的数组中。

### Table
Table 通常与 Archetype 互换使用。在一些 ECS 的实现中，Table 是指存储密集的 Component （具有对齐索引的连续数组）的 Archetype ，其中将稀疏 Component（不连续存储的 Component，或不具有对齐索引存储的 Component）存储在 Archetype 中，将他们的索引存储到 Table 中。

### Sparse set
提供快速迭代、查找、插入和删除时间的数据结构。类似于哈希图，但更适合顺序标识符。

