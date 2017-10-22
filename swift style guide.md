## classes / structs declarations

- opening brace should be on the same line with class / struct declaration
- use extensions for logically different parts of the class, e.g. `UITableViewDelegate` in a `UIViewController`

## let / var 

- camelCase 
- short names (e.g. `i`, `n`, `x`) for short scopes of several lines, long and self-explainatory names (e.g. `newImageSize`) for longer scopes
- use `if-let` instead of `if a != nil { a! }`

## funcs 

- descriptive func names
- long names for short scopes and short nice names for long scopes (opposite for `var` names)
- braces style - opening brace should be on the same line with scope declaration; very small blocks should be one-liners: 

```swift
func dismiss() { dismiss(animated: true) }
```

```swift
if isLoading == false {
  APIHelper.loadData()
  tableView.reloadData()
}
```

```swift
override func viewDidLoad() {
    super.viewDidLoad()
    navigationItem.title = "Add new"
    navigationItem.leftBarButtonItem = UIBarButtonItem(barButtonSystemItem: .cancel, target: self, action: #selector(self.dismissThis))
    navigationItem.rightBarButtonItem = UIBarButtonItem(barButtonSystemItem: .add, target: self, action: #selector(self.btnAddTap))
}
```

- `else` clause should be on separate line from closing brace, like so
```swift
}
else {
```
and not like so
```swift
} else {
```

- curly braces should have exactly one space before / after content, e.g. `{ doWork() }` and not `{doWork()}`
- func param spaces should be aligned like so `func funcName(paramName: ParamType, anotherParam: ParamType)`

## fail early, prefer `guard` to `if-else`

- use: 
```swift 
guard success else { fail(); return }
doWork()
```
instead of:
```swift
if error != nil { 
  doWork() 
}
else { 
  fail() 
}
```

