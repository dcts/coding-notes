# ScreenCapture

- example that reads each pixel of the screen
- input: each pixed
- output: manipulated pixels (overlay structure)
  - converts pixel into black and white.
  - red border to show manipulated pixels!

```java
import java.awt.*;
import java.awt.image.*;

public class Test {

	public static void main(String[] args) throws AWTException {
		int xLen = 1000;    // width of the layer
		int yLen = 1000;    // height of the layer
		Robot r = new Robot();
		BufferedImage img = r.createScreenCapture(new Rectangle(0,0,xLen,yLen));

		// create overlayer Window
		Window w=new Window(null) {
			@Override
			public void update(Graphics g) {
				paint(g);
			}
			@Override
			public void paint(Graphics g) {
				// compute for each pixel corresponding greyscale
				for (int x=0; x<xLen; x++) {
					for (int y=0; y<yLen; y++) {
						// search for border-pixels!
						if (x==0 || y==0 || x==xLen-1 || y==yLen-1) {
							g.setColor(Color.RED);  // set borderColor to RED (255,0,0)
						} else {
							int rgb   = img.getRGB(x, y);
							int red   = (rgb >> 16) & 0xFF;
							int green = (rgb >>  8) & 0xFF;
							int blue  = (rgb      ) & 0xFF;
							int grey  = ((red+green+blue)/3);
							g.setColor(new Color(grey, grey, grey));
						}
						// paint pixel 
						// (@toDo: check if method for painting single pixel exists)
						g.fillRect(x, y, 1, 1);		
					}
				}
			}
		};
		w.setAlwaysOnTop(true);
		w.setBounds(w.getGraphicsConfiguration().getBounds());
		w.setBackground(new Color(0, true));
		w.setVisible(true);
	}
}
```
