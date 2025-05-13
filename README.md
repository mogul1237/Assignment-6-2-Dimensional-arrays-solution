# Assignment-6-2-Dimensional-arrays-solution

Download Here: [Assignment #6: 2-Dimensional arrays solution](https://jarviscodinghub.com/assignment/assignment-6-2-dimensional-arrays-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

How to hand in your work
Submit the file ImageManipulate.java in the Assignment #6 link on connex.
Learning outcomes
When you have completed this assignment, you will understand:
 How to pass parameters and return values using static methods.  How to pass arguments from the command-line to the String[] args array  How to use two-dimensional (2D) arrays.  How to orient yourself with and extend previously written code.  How to indent and document a Java program.
One well-known set of tasks for computers today is the manipulation of images. Your work for this assignment is to add additional methods to the program ImageManipulate.java. Each execution of the program will perform either one output transformation (ASCII-art version of image) or an image manipulation (i.e., reflect across x-axis; reflect across y-axis; tile an image; invert image, rotate image).
For this assignment, you will be using the command-line interface to pass in the names of the input and output files, as well as the image manipulation operation information. Solutions must not use a Scanner object, or require any other interaction from the user during execution.

Page 2 of 10
To illustrate how the data in an image file is represented in a 2D array of integers, consider the very small image below that is 10 pixels wide by 10 pixels high below:

If we really zoom in on this image, we can see that the image is a matrix of pixels, each representing some shade of gray. A 2D array of integers with values ranging from 0 to 255 to represent the above image could be constructed in our program. Given the image above named “example.png”, using the readGrayscaleImage method provided, we could create a 2D array with the same values shown above.
int[][] image = readGrayscaleImage(“example.png”);
The above statement would create an array with the same values as the following:
int[][] image = { {255, 255, 255, 255, 255, 255, 255, 000, 195, 126}, {255, 255, 255, 255, 255, 255, 255, 000, 195, 126}, {255, 000, 253, 255, 000, 255, 255, 000, 195, 126}, {255, 000, 255, 255, 000, 255, 255, 000, 195, 126}, {255, 255, 255, 255, 255, 255, 255, 000, 195, 126}, {255, 255, 255, 255, 255, 255, 255, 000, 195, 126}, {255, 000, 255, 255, 000, 255, 255, 000, 195, 126}, {255, 000, 255, 255, 000, 255, 255, 000, 195, 126}, {255, 255, 000, 000, 253, 255, 255, 000, 195, 126}, {255, 255, 255, 255, 255, 255, 255, 000, 195, 126} };
As you can see in the 2D array of integers above, all of the black pixels in the image have a value of 0, all of the white pixels in the image have a value of 255, and all the gray pixels have a value in between, depending on how light or dark they are.
Page 3 of 10
Recommended steps to follow in order
1. Similar to Assignments 4 & 5, the specification document outlines all of the required methods for this assignment. Appendix A illustrates some examples of how to call and test the methods in your ImageManipulate.java program.
2. In this assignment the args array in the main method specifies the name of the input image file to read and output image file to create. It also specifies which method to run. Complete the main method first, by calling the readGrayscaleImage method, which creates a 2D array of integers from an image file. The array is what you will use in the manipulation methods.
3. Now start working on the manipulation methods. Start with the invert method. This method returns a 2D array back to main with all values inverted. When this is complete, you can pass the resulting 2D array into the writeGrayscaleImage method, and see the inverted image!
Marking
Your mark will be based on the following criteria:
 Your code must compile and run. Some examples of how to test your methods, along with expected output, are outlined in Appendix A.  Your code must conform to all the requirements mentioned in the specification document.  Test each of the required methods to ensure each one functions correctly.  Your code must follow the guidelines outlined in Style_Guidelines.pdf, found through the Lectures & Stuff link in the Lab Resources folder on connex. You may notice that the specification document provides some very nice comments you are welcome to borrow.
Page 4 of 10
Appendix A – Testing your code
Getting started setting up the main method:
All of the information needed by the program will be passed in through the args array when the program is executed, there will be no use of Scanners. Let’s assume the user compiled and executed the program the following way:
This will put the following contents into the args array in the main method:
args: {“example.jpg”,”invertTest.jpg”,”invert”} args.length: 3
This command tells your program to use the data in the example.jpg file, invert it, and create a new image file invertTest.jpg with the inverted values.
example.jpg invertTest.jpg
The program will always be executed in the same fashion:
java ImageManipulate
