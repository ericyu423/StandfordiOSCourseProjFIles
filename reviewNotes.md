# optional 
          let x: String? = "hello"
          var y = Optional<String>.none

          if let p = y {
              print("here")
          }
          //same
          switch y {
              case .some(let p):
              print("here")
              case .none:
              print("fail")
              break
          }
          
          
          let j = y ?? x
          print(j) -> Optional("hello") since j is an optional
          
   

                    var j = y ?? x
                    //they are the same
                    if y != nil {
                        j = y
                    }else{
                        j = x
                    }

# Tuples

                    let a: (String, Int, Double) = ("hello", 5, 8.8)

                    let (x,y,z) = a

                    print(x) -> hello
                    
                    
                    
                    let a: (w: Int, y: String) = (9,"l")

                     a.w = 9
                     
 //return value from function...well...I been using this for 2 year but never think of them as tuples...
 
 
 # Range  ...
 
                     struct Range<T>{
                     var startIndex: T
                     var endIndex: T
                     }
                     
                     let x = [9,8,7,6,5]

                    let xa = x[0...3]

                    print(xa) -> 9 8 7 6
                    
 # struct need mutating if it's mehod changes the struct
 
 reason is that is a value type
 
 # type and instance can have methods 
 
 
                    var x: Double = 3

                    x.isLessThanOrEqualTo(1)

                    false
                    
                    var x: Double = -3

                     x.sign  -> minus
                    
                    
    // i do not know about this
    
                    Double.abs(x)
                    
                    
   
   //create type method by "static func"
   
# String methods example. a lot of data are commma seperated, this turns it into a an array
 
 let y = "k,lh,jlkjh".components(separatedBy: ",")
 
