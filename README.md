# Threeverse
A **threejs** virtual experience engine library that allows loading of gltf/glb/fbx assets in threeverse

**Installation**
  
    import{threeverse}from'./assets/js/threeverse.js'
  
    let engine=new threeverse()

Download threeverse and import threeverse.js in your project to create a new virtual experience engine

**Threejs FPS**

![Screenshot 2023-12-31 100303](https://github.com/VeinSyct/Threeverse/assets/106228791/02310a1f-8f4d-4c45-8c77-7b51c76cb63f)

Get model from threejs example [FPS first person shooter](https://threejs.org/examples/?q=fps#games_fps)

**Usage**

    if(engine.create({id:'canvas-window',url:'https://realengine.web.app'})){
      engine.load({id:'canvas-window',url:'https://realengine.web.app',assets:[
        {
          name:'https://firebasestorage.googleapis.com/v0/b/virtual-55d5e.appspot.com/o/THREEVERSE%2Fprototypbody.glb?alt=media&token=b9c873b9-af9b-40fc-a407-df2270f3ef06',
          type:'trimesh',loader:'glb',
          x:[0],y:[-5],z:[0],o:[{x:0,y:0,z:0}],s:[1000],kg:[0],ds:120
        },
        {
          name:'https://firebasestorage.googleapis.com/v0/b/virtual-55d5e.appspot.com/o/THREEVERSE%2Fprototyp.glb?alt=media&token=e68b649a-a8dc-487e-98d0-857b05d8a433',
          type:'objectmesh',loader:'glb',
          x:[0],y:[-5],z:[0],o:[{x:0,y:0,z:0}],s:[1000],kg:[0],ds:120,select:'navigatable'
        }
      ],
      origin:{
        spawn:[
          {x:10,y:5,z:-50,o:0,s:2.5}
        ],
        respawn:[
          {x:10,y:5,z:-50,o:0,s:2.5,cost:'10-500'}
        ]
      },delay:2400})
    }else console.log('No internet!')

Call function create in the engine and start loading your GLTF/FBX assets in threeverse virtual experience engine.

The assets must be shared [CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) allow all to be able for the threeverse engine to load from cross origin.

**Game Level**

A game level assets are GLT/FBX 3d models that will be seen in the scene and the invible collision mesh that will prevent your avatar, vehicles and other dynamic mesh from passing through wall or each other.

Visible Mesh
  1. type:'objectmesh'
  2. type:'object'

Invisible Physics Mesh
  1. type:'trimesh'
  2. type:'plyhedron'

**Demo [Trench Terrain]**

![Screenshot 2024-01-02 205430](https://github.com/VeinSyct/Threeverse/assets/106228791/7dacc71b-32d4-4673-9450-1864bb21c8f8)

[Dowload](https://virtualtour.web.app/#tours=trenchterrain)

**Demo [Toy car driving]**

![Screen Shot 2024-01-23 at 2 37 21 PM](https://github.com/VeinSyct/Threeverse/assets/106228791/2c8dde8a-7ba7-43b3-be67-c7fb4507931f)

[Dowload](https://virtualtour.web.app/#tours=rtih)

**Resources:**

[Download Source](https://sukinatin.web.app/#rvnkzxk)


