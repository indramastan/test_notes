**INTRODUCTION**

- In order to compose a scene, the objects need to be assembled together in the so called *scene/world *coordinate system. That means, at the time of defining the objects, the shape, size, and position of the object is not important. 

- Consequently, we have to perform operations to *transform *objects (from its *local *coordinate to the *scene/world *coordinate). The stage of the graphics pipeline in which this transformation takes place is known as the modeling transformation. Figure 3.1 illustrates the idea.

![](/images/z9V_Image_1.png)

- Modeling transformation effectively implies applying some *operations *on the object definition to transform them as a component of the world coordinate scene. 

- There are several such operations possible. However, all these operations can be derived from the following basic operations.

BASIC TRANSFORMATIONS

![](/images/IZ6_Image_2.png)
Among the four basic transformations, translation is the simplest.

- In order to translate a point *p*(*x*, *y*) to a new location *p*?(*x*?, *y*), we displace the point by an amount *tx *and *ty *along the X and Y directions, respectively, as shown in Fig. 3.2. 

- If the displacement is along the positive X-axis, it is positive displacement, otherwise the displacement is negative. The same is true for vertical displacements.

![](/images/HlG_Image_3.png)
