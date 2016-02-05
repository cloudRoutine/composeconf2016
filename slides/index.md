- title : Ionide and F# OSS
- description : Building Open Source F# Tooling and the F# OSS Community
- author : Jared Hester
- theme : night
- transition : default

***

## Ionide and the State of F# OSS

![Ionide](images/ionide-logo.png)

-------
## Jared Hester

![cloudRoutine](images/cloudRoutine.png)
###[https://github.com/cloudRoutine](https://github.com/cloudRoutine)
###[@cloudRoutine](https://twitter.com/cloudRoutine)


-----

### Maintainer
|-------------------------------------------------------------------|---------------------------------------|-----------------------------------------------|
|![FSharp.Control.Reactive](images/fsharp.control.reactive-logo.png)|![Ionide](images/ionide-logo-small.png)|![VisualFSharpPowertools](images/vfpt-logo.png)|

### Contributor
|-------------------------------|-----------------------------------------------|
|![Paket](images/paket-logo.png)|![VisualFSharpPowertools](images/fake-logo.png)|


***

## What is Ionide?

| Atom                      |                                       | vscode            |
|:-------------------------:|---------------------------------------|:---------------------------:|
|![Atom](images/atom-logo.png)|![FSharp](images/fsharp-logo.png)|![Vscode](images/vscode-logo.png)|

---------

### Syntax Highlighting

![Highlighting](images/syntax-highlighting.png)


----

### Intellisense Tooltips

![Tooltips](http://i.imgur.com/OqWA08g.gif)


---
### Autocomplete

![Autocomplete](http://i.imgur.com/wlesaW5.gif)

-----
### Glyph Completion

![Glyphs](http://i.imgur.com/rsq5ukR.gif)

---
### Ionide FSI

![FSI](http://i.imgur.com/zCmpk1u.gif)

------

## Ionide Paket

![Paket](http://i.imgur.com/Vp9GjuH.gif)

---

## Ionide FAKE

![FAKE](http://i.imgur.com/qMXsHMV.gif)

---

## Code Snippets

![Snippets](http://i.imgur.com/jta19C6.gif)

---

## Yeoman Generator

![Yeoman](http://i.imgur.com/ObskEMT.gif)


***

# Ionide Internals

-----

![Electron](images/electron.png)

----

![Funscript](images/Funscript.png)

----
```
[<ReflectedDefinition>]
module Atom.FSharp.CompletionHelpers

/// Find the minimum of three three terms that support comparison
let inline min3(a, b, c) = min a (min b c)

let inline distanceCalc (m, u) (n, v) =
    let d1 = Array.init n id
    let d0 = Array.create n 0
    for i=1 to m-1 do
        d0.[0] <- i
        let ui = u i
        for j=1 to n-1 do
            d0.[j] <- 1 + min3(d1.[j], d0.[j-1], d1.[j-1] + if ui = v j then -1 else 0)
        Array.blit d0 0 d1 0 n
    d0.[n-1]

let editDistance (s: string) (t: string) =
    distanceCalc (s.Length, fun i -> s.[i]) (t.Length, fun i -> t.[i])
```

----

***

# OSS for F# Success

----

### This Presentation was brought to you by

| FSharp.Formatting   |  Suave  |FsReveal|
|:-------------------:|:-------:|:------:|
| ![FSharp.Formatting](images/FSharp.Formatting-logo-mid.png)|![Suave](images/suave-wide.png)  |![FsReveal](images/FsReveal-logo.png)|

----

## VFPT OSS Dependencies

- FSharp.Viewmodule
- FsXaml
- FsCheck
- FSharpLint
- Fantomas
- FsPickler
- FParsec

-------




***

## The F# OSS Community

-----

## Explore Projects

#### F# Community Incubation Space  
#### http://fsprojects.github.io/
![fsprojects](images/fsprojects-logo.png)

----

### Meet the Devs

#### FPChat - Functional Programming Slack Team #fsharp
![Slack](images/slack-logo.png)

#### https://gitter.im/ionide/ionide-project
![Gitter](images/gitter-logo.png)


***
# The Future of Ionide & VFPT

---

##[Ionide Roadmap](https://github.com/ionide/ionide-fsharp/wiki/Ionide-Roadmap)


- FSharpLint Integration
- FsLab Integration
- Fix Integration
- More Code Snippets
- Path Completion

---

## VisualFSharpPowertools
## ->
## FSharpPowertools


***

### [Links to Projects mentioned in this presentation](https://github.com/cloudRoutine/composeconf2016)
