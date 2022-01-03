# Bevy Embedded Assets

![MIT/Apache 2.0](https://img.shields.io/badge/license-MIT%2FApache-blue.svg)
[![Realease Doc](https://docs.rs/bevy_embedded_assets/badge.svg)](https://docs.rs/bevy_embedded_assets)
[![Crate](https://img.shields.io/crates/v/bevy_embedded_assets.svg)](https://crates.io/crates/bevy_embedded_assets)
[![Bevy tracking](https://img.shields.io/badge/Bevy%20tracking-main-lightblue)](https://github.com/bevyengine/bevy/blob/main/docs/plugins_guidelines.md#main-branch-tracking)

Embed your asset folder inside your binary for easier releases.

```rust
use bevy::prelude::*;
use bevy_embedded_assets::EmbeddedAssetPlugin;

fn main() {
    App::new().add_plugins_with(DefaultPlugins, |group| {
        group.add_before::<bevy::asset::AssetPlugin, _>(EmbeddedAssetPlugin)
    });
}
```

## Bevy Compatibility

|Bevy|bevy_embedded_assets|
|---|---|
|main|main|
|0.5|0.1|
