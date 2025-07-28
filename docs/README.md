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
        app.add_systems(FixedUpdate,check_collision);
    }
}
```
