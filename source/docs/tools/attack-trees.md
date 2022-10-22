# About attack trees 

There are DREAD, P.A.S.T.A., STRIDE and VAST methods. Using these makes us thing along structured lines, thinking
all is covered when we have used it, and confident we are secure. We prefer attack trees because it allows us to 
**think**.

Attack trees are the conceptual diagram showing how an asset, or target, might be attacked. These are multi-level 
diagrams consisting of one root node, leaves, and children nodes. Bottom to Top, child nodes are conditions that must 
be satisfied to make the direct parent node true. An attack is considered complete when the root is satisfied. 
Each node may be satisfied only by its direct child nodes. 

Suppose there is 1 grandchild below the root node. In such a case multiple steps must be taken to carry out an attack 
as first the grandchild’s conditions must be satisfied for the direct parent node to be true and then the direct parent 
node condition must be satisfied to make the root node true. It also has `AND` and `OR` options which represent 
alternatives and different steps towards achieving that goal.

## Modelling Attack trees

Commercial Tools like SecurITree, AttackTree+ and opensource tools like ADTool, Ent, SeaMonster can be used to model 
attack trees.

And since this is just about drawing boxes, a drawing tool will do. Also, writing the tree is very common and 
will suffice. 
