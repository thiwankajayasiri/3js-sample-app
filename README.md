# 3js-sample-app
threejs sample application 

Exploring threejs ( JavaScript 3D library).
Author: Thiwanka Jayasiri (TJ), Date : 02.03.2021

Motivation ;

I started to explore threejs as part of getting an idea for a potential job that I recently applied for and getting to know the tech stack a bit better, as I’ve focused on Embedded hardware, AI/ML software development for the last 2 years. However, I had a bit of a background in front-end application development as a software engineer, haven’t had a chance to go through to the full depth of JavaScript. 
To start off, first, it’s essential to understand the structure of the basic threejs application. There are few parts, page structure HTML, page format CSS, and under scripts, you can bring in all the Javascript content. There are 3 parts to the main javascript content;  scene, camera, and render; in this small project, I tried to explore how to control a location, setting up a camera view, bringing in lighting conditions, and importing a 3D model to an application. Here I’m using the ‘.glTF’ file format, and there are other file formats, e.g., ‘.obj,’ where we could import .mat and define texture, etc. 

Here is the link to know more about glTF. 

I’m sticking to glTF format due to factors; fast load time, compact file sizes. It’s the file format probably be the go forward in 3D when the times come. We can use the GLTFloader.js to import this file format to the application. 

However, nothing complicated in the ‘.obj’ file handling, and feel free to try along the way, and here is an excellent tutorial on how to use the ‘.obj’ file.

Setting up your dev environment ;

With the Apple M1, I first install the Nodejs and then follow the instruction with the installation page of threeJs. And this may differ from your OS. 

Here are the package details, https://www.npmjs.com/package/three

Selecting your IDE ;

I used VS Code as the IDE, just to say I’m doing most of my work on PyCharm on AI/ML space; VS code seems bloody good, and I used LiveServer Plugin to run the app locally; handy! VS got some pretty good stuff over there, and if you are doing some profiling task, I don’t think VS is the IDE for that, but overall it’s pretty fair to build 

Selecting the browser for debugging purposes and all sorts of analysis work, it’s obvious the Chrome! 
Project directory structure 

> Main folder ( in my case 3js-sample project)
	>build 
		—three.module.js
	> texture ( folder containing the texture files for glTF object)
	—GLTFLoader.js
	—index.html
	—scene.bin(binary file)
	—scene.gltf (gilt file)
	—three.js

There are two ways to host a three.js library; static and CDN; I’m using both methods in my project. You can download free 3D models from SketchFab, and have used the school building as the model for this application. Keep in mind that you’ll have to change the camera.set parameters based on the model. 
Debugging Tips

GLTFLoader js, file handling using three.module.js,  I suggest looking at the GLTFLoader.js file after importing it from the three.js main repo and checking each file module that it’s calling to execute, where you’ll find clues to restructure your project’s folder setup. Which is essential when bringing in more complexity to the project. 

Constructor error: when creating constructors, always make sure to use ‘new’ and then followed by THREE; if the module import is using CDN, no need to use the THREE, but the ‘new’ has to be there. 
Further improvements

I’m looking forward to improving this application as a part of the learning process and further add more complexity to it moving forward. Some of the immediate goals are as follows,  
Add unit testing. 
Avoid CDN and use static loading (and get rid of the URL lines) or use the JSDELIVR, fast and reliable service to host the javascript files on CDN. 
Package and host it as an application, preferably Azure, or AWS. 

Tech-stack : HTML, JavaScript, Node, npm. 
Enjoy exploring more and, please feel free to leave a comment on the improvement areas and use this repo as a boilerplate to develop your threejs application. Happy coding!

