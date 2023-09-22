# Rust

## Declare variables
> use ```let``` keyword
```rust
fn main(){                                           fn main(){
  let x = 5;                                           let mut x = 5;  
  x = 6; ❌ //cause an error                               ⬆️------------------mutable
}                                                      x = 6; ✅  // value update to 6
                                                      }
```
## Declare Constant
> use ```const``` keyword
```rust
fn main(){
  const SCORE_LIMIT: u32 = 100;         ---- u = non-negative 
                      ⬆️---------------|
}                                       ---- 32 = 32 bits 
```
