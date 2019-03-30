# JFrame
```java
// initialize JFrame
JFrame jf = new JFrame("TITLE");

// JFrame methods
jf.setTitle("changed title")     // sets new title
jf.setVisible(true);             // make JFrame visible
jf.setSize(width, heigth);       // set size of canvas	
jf.setResizable(false);          // JFrame can be resized by user (Y/N?)
jf.setLocation(xPos, yPos);      // set location of JFrame on the users screen!
jf.setLocationRelativeTo(null);  // JFrame will appear in the middle of the screen. 
                                 // Must be called after setting the size, but 
                                 // before setting visible
// set closing parameter (end program when user closes JFrame!)
jf.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE)	
```
