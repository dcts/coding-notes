# Robot

- class can control keyboard and mouse of computer

```java
// import needed classes
import java.awt.Robot;
import java.awt.event.KeyEvent;
import java.awt.event.InputEvent;
```

```java
// Initialization
Robot robot = new Robot();
```

### Keyboard Controller
- [KeyListener](https://docs.oracle.com/javase/tutorial/uiswing/events/keylistener.html)
- [KeyEvent Documentation](https://docs.oracle.com/javase/7/docs/api/java/awt/event/KeyEvent.html)
```java
// PRESSING THE KEYBOARD
// with key codes! -> use KeyListener to find out int value of each key!
robot.keyPress(10)    // press "enter" (enter keycode = 10)
robot.keyRelease(10)  // release "enter"

// with KeyEvent class
robot.keyPress(KeyEvent.VK_ESCAPE);   // presses ESC
robot.keyRelease(KeyEvent.VK_ESCAPE); // releases ESC

// some Keys
// see full documentation for KeyEvent for all keys
KeyEvent.VK_ENTER;   // enter
KeyEvent.VK_ESCAPE;  // ESC

KeyEvent.VK_UP;      // arrow: up
KeyEvent.VK_DOWN;    // arrow: down 
KeyEvent.VK_LEFT;    // arrow: left
KeyEvent.VK_RIGHT;   // arrow: right

KeyEvent.VK_PERIOD;  // .
KeyEvent.VK_EQUALS;  // =

KeyEvent.VK_ALT;     // alt
KeyEvent.VK_SHIFT;   // shift
KeyEvent.VK_CONTROL; // crtl ? (not sure)

KeyEvent.VK_NUMPAD0; // NUMPAD0 - NUMPAD9
KeyEvent.VK_F1;   // F2,F3,F4,F5,F6,F7,F8,F9,F10,F11,F12
```

### Mouse Clicker
- [InputEvent Documentation](https://docs.oracle.com/javase/7/docs/api/java/awt/event/InputEvent.html)
```java
// CLICKING MOUSE
robot.mousePress(InputEvent.BUTTON1_MASK);   // press leftclick
robot.mouseRelease(InputEvent.BUTTON1_MASK); // release leftclick

InputEvent.BUTTON1_MAST; // leftclick
InputEvent.BUTTON2_MAST; // middlemouse
InputEvent.BUTTON3_MAST; // rightclick

robot.mouseWheel(1);  // scroll down
robot.mouseWheel(3);  // scroll down (faster)
robot.mouseWheel(-1); // scroll up 
robot.mouseWheel(-3); // scroll up (faster)
```


