# Rust 
- [x] `Chapter 1 Introduction`
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
## Compound data types

### Array
``` rust     
fn main(){
  let first_name = array[0]; 
} 
```
### Tuples
> empty tuple called `unit`
``` rust     
fn main(){
  let tuple:(bool ,u16,u8)=(true,2,3);
  println!("{}",tuple.0);
}
```
## Function
> start with `fn`
``` rust     
fn exclaim(input :String) -> String {                         fn main(){
  //funtion body              ⬆️---optional return type          last_char(String::from("hello"));
}                                                                   ⬆️---------call the funtion
                                                              }
                                                              fn last_char(input:String) -> char{
                                                                if input.is_empty()
                                                                {
                                                                      return '😁'
                                                                }
                                                                input.chars().next_back().unwrap()
                                                              }
```
## Structs
> A type that's composed of other types
> use `struct`
``` rust
struct Car {
  make: String,
  model: String,
  year: u32,
}
fn main(){
  let car1 = Car
 {
    make: String::from("Ford"),
    model: String::from("Mustang"),
    year:1967
 }
}
```
## Enum
> use `enum`
> custom data types that can be use used in code
```rust
  enum CardinalDirections{
    North,
    South,
    East,
    West,
  }
fn main(){
  let west = CardinalDirections::West(string::from("West"));
}
```
### if/else match
```rust
fn main() {                                                         fn main(){
    let number = 7;                                                      let fruit = "apple";
    if number < 5 {                                                      match fruit{
        println!("Number is less than 5");                                    "apple" => println!("🍎"),
    } else {                                                                  "banana" => println!("🍌"),
        println!("Number is greater than or equal to 5");                     "chery" => println!("🍒"),
    }                                                                          _=>println!("⚠️"),
}                                                                        }
                                                                      }
```
### Loop
```rust
fn main(){                               fn main(){                           fn main(){
  loop {                                   let mut number = 3;                   let a = [10,20,30,40];
    println!("I am loop");                 while number != 0{                    for element in a.iter(){
    break;                                    println!("{}",number);                               ⬆️----iterator       
  }                                           number -= 1;                         println!("the value is:{}",element);
}                                          }                                     }
                                           println!("loop off");              }
                                        }
```
## Error Handling

### panic
> use `panic` key word
``` rust          
  fn main(){                          fn main(){        
    panic!("farewell");                  let v:Vec<i32> = Vec![0,1,2,3];
}                                        println!("{}",v[6]);
```
> use match
``` rust
let f = match f{
  Ok(file)=>file,
  Err(error)=> panic!("Can'open the file: {:?}",error),
}
```                                 }
### 
