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

- project should be structured by components
- - Component 1
- - - Logic
- - - Views
- - - Storyboard / Assets
- - Component 2
- - ...

each component should be independent from the other major componnts, clojures or interfaces should be used to segregate them

## frameworks 

a set of code that has a common goal and is not specific to the project at hand should be extracted to a framework

## classes / files

- classes should generally contain superclass name: `DashboardTableViewCell`, `DashboardViewController`
- file containing class should be named same as class (unless containing multiple classes)
- obsolete classes / files / comments should be removed 
- in most cases, table cell classes should be in their own files separate from view controllers

## git commits 

- git commits should contain a descriptive description (unless a typo fix or minor alignment change) 
- git commits should relatively small and conceivable in size, containing logical complete changes (an implemented feature) 
- large features / changes should be split to multiple commits
- commit should not break project builds or introduce warnings

## cocoapods 

- pods should be included to git repo - unless containing files that does not fit to github / bitbucket file size limit 
- pods that are not in use anymore should be removed
