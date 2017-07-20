README.md
=====

# Demo

http://syuhei176.github.io/clooca-diagram-editor/dist/index.html

### Custom Shape

http://syuhei176.github.io/clooca-diagram-editor/dist/custom.html


# Example

```
<script src="diagram-editor.js"></script>
<script>
  window.addEventListener('load', function(e) {
    var diagramEditor = new CloocaDiagramEditor.DiagramEditor("main");
    var toolpallet = diagramEditor.createToolPallet();
    toolpallet.addItem('select', 'selectIcon')
    toolpallet.addItem('rect', 'rectIcon')
    diagramEditor.on('addNode', function() {

    })
    var node1 = diagramEditor.addNode({
      bound:{
        x : 100,
        y : 100,
        w : 100,
        h : 50
    }});
    node1.setPos(120, 120)
    var node2 = diagramEditor.addNode({
      bound:{
        x : 200,
        y : 100,
        w : 100,
        h : 50
    }});
  diagramEditor.addConnection(node1, node2, {/*options*/})
  node1.updateText('Book\n-----\n+ title:string')
  node2.updateText('Order\n-----\n+ id:string')
  });
</script>
<div id="main"></div>
```

![ScreenShot](http://syuhei176.github.io/clooca-diagram-editor/ss/ss1.png "ScreenShot")