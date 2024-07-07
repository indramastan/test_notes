# Computer Graphics

# Chapter Two

# Object Representation

# Techniques

# INTRODUCTION

- In a computer-generated scene, objects of different shapes and sizes are present.

- In order to generate scenes where all these disparate objects are present, we first need to have some way to represent them.

- Any representation will not work as we seek answers to the following two questions.

1. How can we represent all these different objects with their characteristic complexities so that those can be rendered realistically in a synthesized environment?



2. How can we have a representation that makes the process of rendering efficient (i.e., can we perform the operations of the different stages of the pipeline in ways that optimize space and time complexities)?

# CATEGORIZATION OF REPRESENTATION TECHNIQUES \


![](/images/lt5_Image_1.png)
A large number of techniques are in use in computer graphics to represent objects. We can categorize them along the following types.

- Point-sample rendering

- Boundary representation

- Space partitioning

- Sweep representation

# Different object representation techniques used in 3D computer graphics

# BOUNDARY REPRESENTATION TECHNIQUES \


- There are several ways in which an object can be represented in terms of its bounding surfaces.

- The most basic technique is to use polygons to represent surfaces.

- Polygonal surfaces are represented using vertex/edge lists that store the information about all the vertices/edges on the surface and their relationships. For polyhedral objects (i.e., objects with polygonal surfaces), such lists are used, as shown in Fig. 2.4.

![](/images/WRU_Image_2.png)

# Quadric Surfaces \


- Objects, which (or the surface of which) are described with second-degree equations (i.e., quadratic equations), are generally termed as quadric surfaces.

- Spheres are the most commonly used among all quadric surfaces.

# Blobby Objects \


- There are some objects whose shapes show a certain degree of fluidity. That means, these objects change their shape during motion or when they come closer to other objects.

- Although the objects have curved surfaces, we can not use standard shapes to represent them.

- This is since the standard shapes fail to represent the surface fluidity in a realistic way. Such obejcts are generally referred to as blobby objects.

# SPLINE REPRESENTATIONS \


- In order to generate complex shapes, we need to represent curves. Before we proceed further, we should note that representation here refers to the parametric representation.

![](/images/TnW_Image_3.png)

# Continuity Conditions \


- Since we are joining several polynomials in order to create a spline representation, it is important to ensure that they join smoothly so that the resulting curve looks smooth.

- The objective can be achieved if we can make the splines conform to the continuity conditions.

- Continuity conditions are of two types, namely, (a) parametric continuity and (b) geometric continuity.

# Types of Splines \


- While conforming to the parametric or geometric continuity conditions can ensure smooth curves, we also need to keep in mind the fact that the overall design should support local controllability.

- In order to address these issues, different types of splines are used in computer graphics. Such splines are broadly of the following two types.

- Interpolating splines

- Approximating splines

![](/images/Myt_Image_4.png)

# Representation by Basis Matrix \


![](/images/jqi_Image_5.png)
The above derivation demonstrates that the basis matrix for an interpolating polynomial that satisfies the parameterization conditions (constraints) is fixed.

- Hence, it can be used to uniquely characterize the polynomial. Since a spline is made up of polynomial pieces, if each of these pieces are made from the same type of polynomial (i.e., degree and constraints

are the same), then the overall spline can be uniquely characterized by the basis matrix of the polynomial pieces.

- That is the basis matrix representation of splines.

# Representation by Blending Functions \


- If we expand the right-hand side of the above equation, we get a weighted sum of polynomials with the control points being the weights.

- For our specific example (of a linear polynomial), the expansion will result in following equation.

![](/images/yik_Image_6.png)

- The individual polynomials in the weighted sum, such as the terms 1 ? u and u in Eq. 2.8, are called the basis/blending functions.

- The compact representation of a curve in terms of blending functions is shown below, where n + 1 is the number of control points.

![](/images/qtF_Image_7.png)

# Interpolating Splines: Natural, Hermite, and Cardinal Cubics \


- One of the first splines used in computer graphics is the natural cubic splines. As the name suggests, the spline is made up of pieces of third degree polynomials.

- Each of these pieces is defined by four control points (p0, p1, p2, and p3). The first and the last points denote the two boundary points (i.e., for u = 0 and u = 1) of the polynomial piece while the other two are the first and second derivatives at u = 0.

- A problem with the natural cubics is that it does not have local controllability (i.e., local changes require re-computing the whole curve).

# Approximating Splines: Cubic Bezier Curves and B-splines \


- Bezier curves are among the widely used representation techniques in computer graphics.

- Its name is derived from the name of the French engineer Pierre Bezier, who first used it to design Renault car bodies. Since a Bezier cubic is an approximating spline, the polynomial pieces do not pass through all the four control points (p0, p1, p2, and p3).

- The Bezier cubics can also be described in terms of the equivalent blending function representation, as we have seen before. The general form of the blending function based representation of a Bezier curve with n + 1 control points is shown below:

![](/images/CYt_Image_9.png)

# Types of B-Splines \


- Three types of B-splines are used in graphics. When the knots are uniformly spaced in the knot vector, we have uniform B-spline as in our example.

- If the spacing between consecutive knots in the knot vector is not same, we get non-uniform B-splines. A third type is called NURBS which stands for non-uniform rational B-spline.

- For our example, we can set up the basis matrix as,

# Displaying Spline Curves \


- In the preceding sections, we have discussed the general idea of splines.

- Let us come back to the basic problem: how to fit a spline curve to a given set of control points?

- The simplest way to do this is to determine (interpolate) new control points using the spline equation.

- Then, we shall join the control points using line segments.

- The blending function representation can be used for the purpose.

![](/images/xQD_Image_10.png)

The process of displaying a spline. In the process, new control points are computed using the blending function representation for different values of the parameter. Then, the points are joined with line segments.

# SPACE-PARTITIONING REPRESENTATION \


- Space partitioning methods, as we mentioned before, address the problem of object representation through the use of the space (volume) enclosed by the boundaries.

- The simplest of all such representations is the voxel. A voxel, simply put, is a 3D equivalent of pixel.

- Like pixel grid, we can create a voxel grid to represent a 3D space. The voxels in the grid are uniform-sized cubes/parallelepipeds. Each voxel carries information such as intensity, temperature, and so on, such that they uniquely describe a 3D scene.

- Binary space partitioning (BSP) is another way of representing space. Similar to the octree method, this method is also implemented as a recursive procedure.

# A 3D space represented as voxels (a) Voxel grid (b) Octree method \


![](/images/bvy_Image_11.png)

# A 3D space represented as voxels (a) Voxel grid (b) Octree method

![](/images/7Qe_Image_13.png)

a) 3D space (b) Represented as BSP tree

Illustration of the CSG method?The leaf nodes are the primitive shapes

# OTHER REPRESENTATIONS \


- The techniques we have discussed so far are useful to approximate objects of different shapes and sizes. However, for complex shapes, we can use more advanced techniques.

- Fractal Representation

- Particle System Representation

![](/images/Ua0_Image_14.png)

# OTHER REPRESENTATIONS (Cont?) \


- Skeletal Model Representation

- Scene Graph Representation

![](/images/uYn_Image_15.png)
(a) A skeleton model (b) Subsequent rendering of animate figure (kitten)

# ISSUES IN MODEL SELECTION \


- It should be apparent from the preceding discussions that there is a rich variety of techniques used to represent objects/scenes in computer graphics. An obvious question is, which technique to use and when?

- The answer depends on many factors. While we always want to represent things in the most realistic way, use of advanced techniques such as particle systems is not always possible.

- This is so since each technique comes with a cost. The cost may be computational or storage requirements or both. Depending on the resources available, we have to make the decision.
