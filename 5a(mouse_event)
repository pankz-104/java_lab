

import java.awt.*;
import java.awt.event.*;
import java.applet.*;
public class lab5a extends Applet implements MouseListener,
MouseMotionListener {
	int mousex = 0, mousey = 0;
	String msg = "";
	public void init() {
		addMouseListener(this);
		addMouseMotionListener(this);	
	}
	public void mouseClicked(MouseEvent e) {
		mousex = 0;
		mousey = 10;
		msg = "Mouse Clicked";
		repaint();
	}
	public void mousePressed(MouseEvent e) {
		mousex = e.getX();
		mousey = e.getY();
		msg = "Mouse Pressed";
		repaint();
	}
	public void mouseMoved(MouseEvent e) {
		showStatus("Mouse moved at :" + e.getX() + "," + e.getY());
	}
	public void mouseReleased(MouseEvent e) {
		mousex = e.getX();
		mousey = e.getY();
		msg = "Mouse Released";
		repaint();
	}
	public void mouseEntered(MouseEvent e) {
		mousex = 0;
		mousey = 10;
		msg = "Mouse Entered";
		repaint();
	}
	public void mouseDragged(MouseEvent e) {
		mousex = e.getX();
		mousey = e.getY();	
		msg = "Mouse Dragged";
		repaint();
	}
	public void mouseExited(MouseEvent e) {
		mousex = 0;
		mousey = 10;
		msg = "Mouse Exited";
		repaint();
	}
	public void paint(Graphics g) {
		g.drawString(msg, mousex, mousey);
	}
}
