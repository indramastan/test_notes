Computer Graphics

# Chapter One

Overview of Computer Graphics

# INTRODUCTION

![](/images/3Z6_Image_1.png)
** \
**With a computer, we can and usually do lot of things. We create documents and presentations.

- For example, consider the screenshot in Fig. 1.1 that was taken during the preparation of this book with MS Word.

# INTRODUCTION (Cont?)

- Next, consider Fig. 1.2, which is an interface of a Computer-aided Design (CAD) tool.

- It shows the design of some machinery parts on a computer screen, along with some control buttons on the right-hand side.

- An engineer can specify the properties of those individual components and try to assemble them virtually on the computer screen, to check if there is any problem in the specifications.

![](/images/eo7_Image_2.png)

# INTRODUCTION (Cont?)

![](/images/SUy_Image_3.png)
** \
**Figure 1.3 shows two instances of visualization, another useful activity done with computers.

# INTRODUCTION (Cont?)

- This fundamental question can further be broken down into a set of four basic questions.

1. Imagery is constructed from its constituent parts. How to represent those parts?

2. How to synthesize the constituent parts to form a complete realistic imagery?

3. How to allow the users to manipulate the imagery constituents on-screen?

4. How to create the impression of motion?

# HISTORICAL DEVELOPMENT OF THE FIELD

- The term computer graphics was first coined by William Fetter of Boeing Corp. in  1960. Sylvan Chasen of Lockheed Corp. in 1981 proposed phase-wise classification of the development of the field. He mentioned four distinct phases in the development process.

1. Conception to birth or the gestational period (1950?1963)

2. Childhood (1964?1970)

3. Adolescence (1970?1981)

4. Adulthood (1981?)

# Major developments in computer graphics

![](/images/6IK_Image_4.png)

# MAJOR ISSUES AND CONCERNS IN COMPUTER GRAPHICS

- In the formative stages of the field, primary concern was generation of 2D scenes.

- Although still in use, 2D graphics is no longer the thrust area. Its place has been taken over by 3D graphics and animations. Consequently, there are three primary concerns in computer graphics today.

- Modeling: Creating and representing the geometry of objects in the 3D world.

- Rendering: Creating and displaying a 2D image of the 3D objects.

- Animation: Describing how the image changes over time.

# MAJOR ISSUES AND CONCERNS IN COMPUTER GRAPHICS (Cont?)

Hardware-related issues While these are primarily issues that are addressed in graphics software, there are many hardware-related issues such as the following:



1. The quality and cost of the display technology, with the trade-off between the two being an important consideration

2. The selection of the appropriate interaction devices (what type of input devices should we have to make the interaction intuitive)

3. Design of specialized graphic devices to speed up the rendering process

# PRELIMINARIES: BASICS OF GRAPHICS SYSTEM

- In computer graphics, what do we do? We synthesize a 2D image that can be displayed on a screen.

- Figure 1.7 shows the schematic of a generic system architecture that is followed by modern-day graphics system.

![](/images/k7j_Image_5.png)

# Graphic Devices

- Graphic devices can be divided into two broad groups, based on the method used for rendering (or excitation of pixels):

- Vector scan devices In vector scan (also known as random-scan, stroke-writing, or calligraphic), an image is viewed as composed of continuous geometric primitives such as lines and curves.

- Raster scan devices In contrast, in raster scan devices, the image is viewed as represented by the whole pixel grid. In order to render a raster image, it is therefore necessary to consider all the pixels. This is achieved by considering the pixels in sequence (typically left to right, top to bottom).

# This difference between the two rendering methods

![](/images/RXE_Image_6.png)

# CRT Displays

- The CRT technology, invented in 1885 ruled the computer displays till recently. We are all familiar with it.

- A typical CRT display is shown in Fig. 1.9, with a schematic of the working of the technology. As the figure shows, CRT displays contain a long funnel-shaped vacuum tube (that gives them the bulky shape). At

![](/images/BsW_Image_7.png)

# GRAPHICS PIPELINE: STAGES OF RENDERING PROCESS

- In the preceding discussion, we were talking about the color values stored in the frame buffer. How are these values obtained?

- As we mentioned, the display processor computes these values in stages. These stages together are known as the graphics pipeline.

- Object representation

- Modeling/Transformation

- Lighting

- Viewing pipeline/transformation

- Scan conversion

# Stages of 3D graphics pipeline

![](/images/oZF_Image_8.png)

# ROLE OF GRAPHIC LIBRARIES

- In the preceding discussions, we outlined the theoretical background of computer graphics.

- Examples of graphic libraries include OpenGL (stands for Open source Graphics Library) and DirectX (by Microsoft).

- These APIs are essentially predefined sets of functions, which, when invoked with the appropriate arguments, perform the specific tasks.

- Graphics applications such as painting systems, CAD tools, video games, or animations are developed using these functions.

