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
 


# anyobject

                              func touch(sender: Anyobject){
                                        if let button = sender as?  UIButton{

                                        }else if let slider = sender as? UISlider

                                        }
                              }
                              
                              
# CGRect , NScoder

from story board               init (coder: NScoder)
from program                   init(frame: CGRect)

# Init UIView

method1

                    override init(frame:CGRect){//from storyboard
                              super.init(frame: frame)
                              setup()
                    }
                    override init(coder aDecoder: NSCoder){//force by compiler so it will work from storyboard
                              super.init(coder: aDecoder)
                              setup()
                    }
                    
method 2
                    awakeFromNib // from story board  only from storyboard
 
 
 # frame vs bound
 
 use bound to draw, your own coordinate system
 
 to draw: override func drawarect()
 
 to redraw: setNeeddisplay() or setneeddisplayinRect(rect: cgrect)
 
 # 2 way to draw
 
 c-like (non object oriented) API called  coregprahic and (object orietned) UIBezierPath
 
 #  core Graphics 
UIGraphicGetCurrentContext()
create path
set draw attiubtes
stroke or fill the path
 # UIBezierPath
same except we don't need to know the context

# Hit detection

func containPoint(CGPoint) -> Bool // return if point is inside the path, path need to be closed obviouly

# Alpha 0 = fully transparent, more alpha the more you can see...kind like the animal hierarchy

#  color can have lpah

let background = UIColor.yellow.colorWithAlphaComponent(0.05)

if you want to draw transparency in your view need to set

#  In View:  var opaque = false (to draw transpency)

#  Letters in UIView custom draw:

let text = NSAttributedString("hello") //objC class
text.drawAtPoint(CGPoint)

let textSize: CGize = text.size

if you want to chagne the text use 

let mutableText = NSMutableAttributedString("some String")

setting attributes

most used ones

NSForegroundColorAttibuteName
NSStrokeWidthAttributedName
NSFontAttibutedName

to remeber them just look at them this way
NS   ForegroundColor   AttibuteName
NS   StrokeWidth       AttributedName
NS   Font              AttibutedName
basically just foregroundcolor, strokeWidth and Font


Font to use

UIFontTextStyle.headline/body/footnote

UIFontDescriptor for more fonts


rotating your view

u want to use the property

var contentMode:UIViewContentMode
.Left/.rifght....

.scaletofill/scaleaspectfil....

or 
.redraw
 
