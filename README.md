<h1 align="center">
    Atic Compiler
</h1>

<div align="center">
  <strong>
        The Atic Compiler written in itself
  </strong>
</div>
<br />

## Basic Syntax:


```Rust
fn Main() {
    let files: List<string> = newList();
    forFile("C:\\",files);

    forEach(files, fn (ref: string) -> void {
        print(ref);
    });
}

fn recursiveFileSearch(file: string, list: List<string>) {
    if isDirectory(file) {
        let files: List<string> = listFiles(file);
        forEach(files,fn (ref: string) -> void {
            recursiveFileSearch(ref,list);
        });
    } else {
        insert(list,file);
    }
}
```