Download Link: https://assignmentchef.com/product/solved-comp1210-project-4-icosahedron-app
<br>
You will write a program this week that is composed of two classes: (1) one named Icosahedron that defines Icosahedron objects, and (2) the other, IcosahedronApp, which has a main method that reads in data, creates an Icosahedron object, and then prints the object.




<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">An <strong>Icosahedron</strong> has 20 equilateral triangle faces, 12 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective methods in the Icosahedron class described in this project.</td>

  </tr>

  <tr>

   <td width="200"> </td>

   <td width="182"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204">  </td>

  </tr>

  <tr>

   <td colspan="3" width="586"> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong> </strong>

<ul>

 <li><strong>Icosahedron.java </strong></li>

</ul>

<strong> </strong>

<strong>Requirements</strong>: Create an Icosahedron class that stores the label, color, and edge (i.e., length of an edge, <u>which must be greater than zero</u>).  The Icosahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface

to volume ratio of an Icosahedron object, and a method to provide a String value of an Icosahedron object (i.e., a class instance).







<strong>Design</strong>:  The Icosahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (instance variables): label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Icosahedron class, and <u>these should be the only instance variables in the class</u>.</li>

</ul>




<ul>

 <li><strong>Constructor</strong>: Your Icosahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn); Below are examples of how the constructor could be used to create Icosahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.</li>

</ul>




Icosahedron example1 = new Icosahedron(“Small”, “blue”, 0.01);




Icosahedron example2 = new Icosahedron(”    Medium    “, “orange”, 12.3);




Icosahedron example3 = new Icosahedron(“Large”, ”  white  “, 123.4);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Icosahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.

  <ul>

   <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

   <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

   <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.  o surfaceArea:  Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

   <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

   <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

   <li>toString: Returns a String containing the information about the Icosahedron object formatted as shown below, including decimal formatting (“#,##0.0#####”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method:</li>

  </ul></li>

</ul>

surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).

Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.    surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723




Icosahedron “Medium” is “orange” with 30 edges of length 12.3 units.    surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724




Icosahedron “Large” is “white” with 30 edges of length 123.4 units.

surface area = 131,874.537977 square units    volume = 4,099,581.395236 cubic units    surface/volume ratio = 0.032168







<strong>Code and Test</strong>: As you implement your Icosahedron class, you should compile it and then test it using interactions.  For example, as soon you have implemented and successfully compiled the constructor, you should create instances of Icosahedron in interactions (e.g., copy/paste the examples above).  Remember that when you have an instance on the workbench, you can unfold it to see its values.  You can also open a viewer canvas window and drag the instance from the Workbench tab to the canvas window.  After you have implemented and compiled one or more methods, create an Icosahedron object in interactions and invoke each of your methods on the object to make sure the methods are working as intended.  You may find it useful to create a separate class with a main method that creates an instance of Icosahedron then prints it out.  This would be similar to the IcosahedronApp class you will create below, except that in the IcosahedronApp class you will read in the values and then create and print the object.




<ul>

 <li><strong>IcosahedronApp.java </strong></li>

</ul>




<strong>Requirements</strong>: Create an IcosahedronApp class with a main method that reads in values for label, color, and edge length.  After the values have been read in, main creates an Icosahedron object and then prints a new line and the object.




<strong>Design</strong>:  The main method should prompt the user to enter the label, color, and edge.  After a value is read in for edge, if the value is less than or equal to zero, an appropriate message (see examples below) should be printed followed by a <em>return</em> from main.  Assuming that edge is positive, an Icosahedron object should be created and printed.   Below is an example where the user has entered a non-positive value for edge followed by an example using the values from the first example above for label, color, and edge.  Your program input/output should be <strong>exactly</strong> as follows.

<table width="637">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="582">Program input/output</td>

  </tr>

  <tr>

   <td width="55">12345 </td>

   <td width="582">Enter label, color, and edge length for an icosahedron.label: icosahedron with a bad edge value    color: yellow    edge: 0Error: edge must be greater than 0. </td>

  </tr>

 </tbody>

</table>




<table width="637">

 <tbody>

  <tr>

   <td width="55">Line #</td>

   <td width="582">Program input/output</td>

  </tr>

  <tr>

   <td width="55">123456789</td>

   <td width="582">Enter label, color, and edge length for an icosahedron.label: Small    color: blue    edge: 0.01 Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.    surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723</td>

  </tr>

 </tbody>

</table>




<strong>Code</strong>:  Your program should use the nextLine method of the Scanner class to read user input.  Note that this method returns the input as a String.  Whenever necessary, you can use the Double.parseDouble method to convert the input String to a double.  For example:

Double.parseDouble(s1) will return the double value represented by String s1.  For the printed lines requesting input for label, color, and edge, use a tab “t” rather than three spaces.  After you have created the object, it can be printed simply by using its variable name; i.e., when the object variable name is evaluated in the println statement, its toString() method is automatically called.  Thus, printing the object reference variable myObj is equivalent to printing the return value of the myObj.toString() method call.




<strong>Test</strong>:  You should test several sets of data to make sure that your program is working correctly.  Although your main method may not use all the methods in Icosahedron, you should ensure that all of your methods work according to the specification.  You can use interactions in jGRASP or you can write another class and main method to exercise the methods.  The viewer canvas should also be helpful, especially using the “Basic” viewer and the “toString” viewer for an Icosahedron object