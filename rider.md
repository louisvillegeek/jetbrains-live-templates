# Live Templates for Rider



Configure live templates in File -> Settings -> Editor -> Live Templates -> C#


## EF Core Live Templates

#### Navigational Properties
* Shortcut: nav
* Reformat: Unchecked

##### Template:

```
public int $name$Id  { get; set; }
[ForeignKey(nameof($name$Id))]
public $name$ $name$ { get; set; }
```

#### OnModelCreating Method
* Shortcut: onModelCreating
* Reformat: Checked

##### Template:

```
public static void OnModelCreating(ModelBuilder modelBuilder) {
    $END$
}
```
