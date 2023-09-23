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
## Shadowing
```rust
fn main(){                                         fn main(){
  let x = 5;                                          let x = 5;
  let x = x + 1; // x is now 6                        let x+=1; ❌ 
}                                                  }
```
## Scalar data types

### Integer
```
            --- i = signed     --- store === -(2^(n-1)) to 2^(n-1)-1 ---
Integer ---|                                                           |---------default i32
            --- u = unsigned   --- store === 0 to 2^n-1              ---
```
### Floating-point
```
 use f32 and f64
              ⬆️------- default 
```
### Numerical Operations
```
+ = addition
- = subtraction
* = multiplication
/ = division
% = remainder
```
### Booleans
> use ```bool``` keyword
one bit size use values 
``` rust     
true     false 
```          
