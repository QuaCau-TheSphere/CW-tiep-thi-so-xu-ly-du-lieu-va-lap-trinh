---
share: true
created: 2023-10-30T14:29
updated: 2025-03-03T18:48
---
  
AutoHotkey combines 3 concepts into 1 built-in basic object type:  
- linear arrays (e.g. obj[1] := "value") (AKA list/vector)  
- associative arrays (e.g. obj["key"] := "value") (AKA dictionary/map)  
- default class (custom/built-in, keys/value properties/dynamic properties/methods, can be added/modified/removed, to give custom classes)  
  
E.g. some ways to create an AHK basic object.  
Note: an AHK basic object does not have base object.

```autohotkey
;in each case obj is a basic object, and identical:
obj := ["a", "b", "c"]
obj := Array("a", "b", "c")
obj := {1:"a", 2:"b", 3:"c"}
obj := Object(1,"a", 2,"b", 3,"c")
obj := StrSplit("a,b,c", ",")

;here, MyClass is also a basic object:
class MyClass
{
	MyMethod()
	{
	}
}

MsgBox, % IsObject(ObjGetBase(obj)) ;0
MsgBox, % IsObject(ObjGetBase(MyClass)) ;0

;note: an instance of MyClass is *not* a basic object:
obj2 := new MyClass
MsgBox, % IsObject(ObjGetBase(obj2)) ;1
```

Nguồn:: [jeeswg's object classes tutorial - AutoHotkey Community](https://www.autohotkey.com/boards/viewtopic.php?f=7&t=54588)
