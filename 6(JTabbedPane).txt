import javax.swing.*;
public class JTabbedPaneee extends JApplet {
	public void init() {
		try {
			SwingUtilities.invokeAndWait(new Runnable()
			{
				public void run() {
			    		makeGUI();
			}
	     	});
		} catch (Exception exc) {
			System.out.println("Can't create because of " + exc);
		}
        }
	private void makeGUI() {
		JTabbedPane jtp = new JTabbedPane();
		jtp.addTab("Cities", new CitiesPanel());
		jtp.addTab("Colors", new ColorsPanel());
		jtp.addTab("Flavors", new FlavorsPanel());
		add(jtp);
	}
}
class CitiesPanel extends JPanel {
	public CitiesPanel() {
		JButton b1 = new JButton("Mumbai");
		add(b1);
		JButton b2 = new JButton("Chennai");
		add(b2);
		JButton b3 = new JButton("Delhi");
		add(b3);
		JButton b4 = new JButton("Kolkata");
		add(b4);
	}
}
class ColorsPanel extends JPanel {
	public ColorsPanel() {
		JCheckBox cb1 = new JCheckBox("Black");
		add(cb1);
		JCheckBox cb2 = new JCheckBox("Purple");
		add(cb2);
		JCheckBox cb3 = new JCheckBox("Green");
		add(cb3);
	}
}
class FlavorsPanel extends JPanel {
	public FlavorsPanel() {
	JComboBox jcb = new JComboBox();
		jcb.addItem("Vanilla");
		jcb.addItem("Chocolate");
		jcb.addItem("Strawberry");
		add(jcb);
	}
}
