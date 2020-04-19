<h1 style="center">Godot Rust Helper Extensions</h1>

This is a library of extension helper methods that get added to projects when the `--extension` option is used with [godot-rust-helper](https://github.com/robertcorpnoi/godot-rust-helper).

## **Usage**

To use the extensions, you open the module you want to add them to and use:

```rust
use godot_rust_helper_extensions::NodeExt as _;
```

where `NodeExt` is the extension you want to use. The extensions available are listed below.

## **NodeExt**

These extensions are tailored around working with nodes.

### **get_typed_node**

Gets a node by its path and casts it into the expected type.

**example**

```rust
unsafe fn _ready(&self, owner: gdnative::Node) {
    let mut message_label: gdnative::Label = owner.get_typed_node("WinText").expect("Cannot cast to Label");
}
```

## **Acknowledgements**

This extensions library was inspired after seeing an [example](https://github.com/GodotNativeTools/godot-rust/blob/master/examples/dodge_the_creeps/src/extensions.rs) by @ankhers that added a helper method to get a typed node in 1 line instead of the 3+ line normal method.

## **License**

MIT