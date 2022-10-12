(render {ui} parent)

pass:
a DOM node(object) or a string for querySelector
a DOM node or DOM array or DOM string to be set
return:
node id being setted
# atomic UI
instead of writing big nested UI tree, writing small atomic UI node.
node store, all the setted UI nodes keyed by id.
children: [id1, id2 ...]
parent: id
above: id
dom: the dom rendered
render: 