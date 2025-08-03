# bro 这太酷了

## Ecs 碰撞检测——bevy 0.16.1
* 有一个插件
```rust
struct CollisionPlugin{}
```
* 实现plugin trait
```rust
impl Plugin for CollisionPlugin{
    fn build(&self, app: &mut App){
        app.add_systems(FixedUpdate,check_collision,update_collidable_enities);
    }
}
```

* 声明其余部分
```rust
impl CollisionPlugin{
    fn check_collision(){
        todo()!
    }

    fn update_collidable_enities(){
        todo()!
    }
}
```


我们从最简单的入手

即AABB的碰撞检测

>为了优化我们可以使用SAP算法
>
>具体思路是将包围盒的横纵坐标相比较
>优化点在于
>
>如果两个包围盒在一个坐标上没有重合就意味着:
>
>**不可能发生碰撞，从而不进行另一个坐标的计算**

## 现在我们需要声明一个组件

```rust
[derive(Component)]
struct Collidable;

[derive(Component)]
struct IsStatic
```

## 接下来，声明一个资源以存放

```rust

```
