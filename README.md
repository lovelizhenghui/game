# game
function add(box,offset,size)
{
  let collider=box.addCompoment(cc.PhysicsBoxColllider)
box.offset=offset;
box.size.width=size.x;
box.size.height=size.y;
}
let bound=new cc.Node("bound");
bound.addCompoment(cc.RigidBody).Type=cc.RigidBody.Statis;

let width=this.node.width;
let height=this.node.height;

let bottom_offset=cc.p(0,-height/2);
let size=cc.p(width,20);
add(bound,bottom_offset,size);

let top_offset=cc.p(0,height/2);
add(box.top_offset,size);

let right_offset=cc.p(width/2,0);
size=cc.p(20,height);

let left_offset=cc.p(-width/2,20);
add(bound,left_offset,size);
this.node.addChild(bound);



