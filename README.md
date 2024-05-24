# axum route helper

```rust
route!(SomeRoute => "/path/{}/with/{}", (:something: String, *parameter: u8));

assert_eq!(
    SomeRoute::handler_route(),
    "/path/:something/with/*parameter"
);

assert_eq!(
    SomeRoute::route_path(String::from("test"), 13),
    "/path/test/with/13"
);
```
