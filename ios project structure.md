## gitignore

- `.gitignore` shoud be presend and should generally look like so

```
.DS_Store

# Xcode
# this ignores dummy workspace files in xcodeproj dir
project-name.xcodeproj/*
!project-name.xcodeproj/project.pbxproj

# this ignores all files in workspace dir except the needed one
project-name.xcworkspace/*
!project-name.xcworkspace/contents.xcworkspacedata

# pods xcodeproj
Pods/Pods.xcodeproj/*
!Pods/Pods.xcodeproj/project.pbxproj
```
- unnecessary files like `.xcuserstate` should be excluded

## folder structure 

- folders should generally contain these with respective files placed inside
- - View Controllers
- - Models
- - Helpers

## classes
- classes should be generally contain superclass name: `DashboardTableViewCell`, `DashboardViewController`
- file containing class should be named same as class (unless containing multible classes)

## git commits 

- git commits should contain a descriptive description (unless a typo fix or minor alignment change) 
- git commits should relatively small and conceivable in size, containing logical complete changes (an implemented feature) 
- large features / changes should be split to multiple commits
- commit should not break project builds or introduce warnings
