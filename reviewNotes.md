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
