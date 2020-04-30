<h1 align="center">
  Visualizing & Manipulating RDF Graphs<br>within the Kanban Paradigm
</h1>

<p align="center">
  <strong>A Prototypical Implementation of an RDF Kanban Board</strong><br>
</p>

**👤 Author:** *Me*

**📥 Download** [PDF](https://raw.githubusercontent.com/Kalaschnik/Master-Thesis/7e6efe779a55ce52580d60a36a5d49af347da9bc/MA.pdf)

# Abstract
In the field of Semantic Web, much effort is invested in developing possible solutions for exploring and managing graph data in a visual context. eccenca’s *Corporate Memory*, an enterprise application suite, enables users to work with semantic models and allows intuitive data exploration. The current work uses eccenca’s software infrastructure to develop a novel approach to visualize RDF resources by mapping graph data in a Kanban board. Based on an RDF configuration graph, users can select the resources represented as the cards of the Kanban board, as well as the property used to represent the columns of the board. In addition to this visualization, the developed prototype allows to modify a resource by the prior selected column property when moving a card between columns on the board. Dropping a card to a novel column triggers the resource to update its property to the value of this column. Visualizing and manipulating knowledge data by relocating cards on a Kanban board represents an innovative approach in the field of semantic data exploration.

# Example Use Case: Ontology Management
## Manage [FOAF](https://en.wikipedia.org/wiki/FOAF_(ontology)) term statuses

FOAF terms can describe individuals in various ways. For example, terms like `foaf:name`, `foaf:depiction`, and `foaf:knows`, are typically used to describe individuals by their name, photo, and relations to other individuals. Each term contains several properties, and one property shared by all terms is `vs:term_status`. For example, the term `foaf:mbox` (describing a personal mailbox) has a status value of `stable` [\[1\]](#fn1), while the status value of `foaf:depiction` is `testing` [\[2\]](#fn2).

Regarding the use case, the first goal is to visualize all FOAF terms distributed over the board’s columns, depending on their inherent status value. The second goal is to change a term’s status value by dragging a card (i.e., a FOAF term) to another column. The user can easily change the status of the `depiction` resource from `testing` to `stable` by dragging the corresponding card. This will trigger a graph update, that makes changes persistent. The following image illustrates this idea.

![RDF Kanban Board](./img/demo.png)

------------

<a name="fn1">1</a>: Compare http://xmlns.com/foaf/spec/#term_mbox  
<a name="fn2">2</a>: Compare http://xmlns.com/foaf/spec/#depiction
