#  MultiMesh  
####**Inherits:** [Resource](class_resource)
####**Category:** Core

###  Brief Description  
Provides high perfomance mesh instancing.

###  Member Functions 
  * void  **[set&#95;mesh](#set_mesh)**  **(** [Mesh](class_mesh) mesh  **)**
  * [Mesh](class_mesh)  **[get&#95;mesh](#get_mesh)**  **(** **)** const
  * void  **[set&#95;instance&#95;count](#set_instance_count)**  **(** [int](class_int) arg0  **)**
  * [int](class_int)  **[get&#95;instance&#95;count](#get_instance_count)**  **(** **)** const
  * void  **[set&#95;instance&#95;transform](#set_instance_transform)**  **(** [int](class_int) arg0, [Transform](class_transform) arg1  **)**
  * [Transform](class_transform)  **[get&#95;instance&#95;transform](#get_instance_transform)**  **(** [int](class_int) arg0  **)** const
  * void  **[set&#95;instance&#95;color](#set_instance_color)**  **(** [int](class_int) arg0, [Color](class_color) arg1  **)**
  * [Color](class_color)  **[get&#95;instance&#95;color](#get_instance_color)**  **(** [int](class_int) arg0  **)** const
  * void  **[set&#95;aabb](#set_aabb)**  **(** [AABB](class_aabb) arg0  **)**
  * [AABB](class_aabb)  **[get&#95;aabb](#get_aabb)**  **(** **)** const
  * void  **[generate&#95;aabb](#generate_aabb)**  **(** **)**

###  Description  
MultiMesh provides low level mesh instancing. If the amount of [Mesh](class_mesh) instances needed goes from hundreds to thousands (and most need to be visible at close proximity) creating such a large amount of [MeshInstance](class_meshinstance) nodes may affect performance by using too much CPU or video memory. 
For this case a MultiMesh becomes very useful, as it can draw thousands of instances with little API overhead.
 As a drawback, if the instances are too far away of each other, performance may be reduced as every sigle instance will always rendered (they are spatially indexed as one, for the whole object).
 Since instances may have any  behavior, the AABB used for visibility must be provided by the user, or generated with [generate&#95;aabb](#generate_aabb).

###  Member Function Description  

#### <a name="set_mesh">set_mesh</a>
  * void  **set&#95;mesh**  **(** [Mesh](class_mesh) mesh  **)**

Set the [Mesh](class_mesh) resource to be drawn in multiple instances.

#### <a name="get_mesh">get_mesh</a>
  * [Mesh](class_mesh)  **get&#95;mesh**  **(** **)** const

Return the [Mesh](class_mesh) resource drawn as multiple instances.

#### <a name="set_instance_count">set_instance_count</a>
  * void  **set&#95;instance&#95;count**  **(** [int](class_int) arg0  **)**

Set the amount of instnces that is going to be drawn. Changing this number will erase all the existing instance transform and color data.

#### <a name="get_instance_count">get_instance_count</a>
  * [int](class_int)  **get&#95;instance&#95;count**  **(** **)** const

Return the amount of instnces that is going to be drawn.

#### <a name="set_instance_transform">set_instance_transform</a>
  * void  **set&#95;instance&#95;transform**  **(** [int](class_int) arg0, [Transform](class_transform) arg1  **)**

Set the transform for a specific instance.

#### <a name="get_instance_transform">get_instance_transform</a>
  * [Transform](class_transform)  **get&#95;instance&#95;transform**  **(** [int](class_int) arg0  **)** const

Return the transform of a specific instance.

#### <a name="set_instance_color">set_instance_color</a>
  * void  **set&#95;instance&#95;color**  **(** [int](class_int) arg0, [Color](class_color) arg1  **)**

Set the color of a specific instance.

#### <a name="get_instance_color">get_instance_color</a>
  * [Color](class_color)  **get&#95;instance&#95;color**  **(** [int](class_int) arg0  **)** const

Get the color of a specific instance.

#### <a name="set_aabb">set_aabb</a>
  * void  **set&#95;aabb**  **(** [AABB](class_aabb) arg0  **)**

Set the visibility AABB. If not provided, MultiMesh will not be visible.

#### <a name="get_aabb">get_aabb</a>
  * [AABB](class_aabb)  **get&#95;aabb**  **(** **)** const

Return the visibility AABB.

#### <a name="generate_aabb">generate_aabb</a>
  * void  **generate&#95;aabb**  **(** **)**

Generate a new visibility AABB, using mesh AABB and instance transforms. Since instance information is stored in the [VisualServer](class_visualserver), this function is VERY SLOW and must NOT be used often.
