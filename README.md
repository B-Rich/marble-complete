A fork of AsciiDots based on turing-complete marble runs

Inspired by:
https://nbickford.wordpress.com/2014/03/25/images-from-marble-runs-and-turing-machines/

The only operator in this esolang is _toggle_. It works like this (taken from site page for Turing Tumble):
![Turing Tumble Bit Piece](https://ksr-ugc.imgix.net/assets/016/325/165/19cae5d12c1d7fbeb07222b17ac63909_original.gif?w=680&fit=max&v=1492659230&auto=format&gif-q=50&q=92&s=d6d2f74ec54534198f285ee2f0672606)

A starting marble is represented with a lowercase o (`o`)

If you want to create a toggler that starts learning _left_ (like \\), use a lowercase t (`t` -> `↘`).  
If you want to create a toggler that starts learning _right_ (like /), use an uppercase T (`T` -> `↙`).

In order to make togglers move in unison (thereby allowing turing-completeness), connect them with _wires_.  
In ascii, wires are represented via periods (`.`). These are prettified into unicode lines (e.g. `┄`).

<sub>
## Ascii vs Unicode source
Programs are typically written with AsciiDots' ascii path rules:

```
 /---
 |
 |
/t\
|.+..
\v/ .
/t\ .
|.+./
| |
| *---
| |
| |
| |
```

... And then translated into Unicode box drawings via `prettify.py`:

```
 ╔═══
 ║    
 ║    
╔↘╗   
║╰+┄╮
╚⇓╝ ┆
╔↘╗ ┆
║╰+┄╯
║ ║   
║ *══
║ ║   
║ ║   
║ ║
```

Prettified code can always be re-asciified via `asciify.py`.
</sub>
