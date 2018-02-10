import java.awt.Color;
import java.awt.Graphics;
import javax.swing.*;

public class digitalAstronomy extends JPanel
{
  final Color VIOLET = new Color(128, 0, 128);
  final Color INDIGO = new Color(75, 0, 132);
  final Color LIGHTBLUE = new Color(15, 95, 200);

  private Color colors[] = {LIGHTBLUE, LIGHTBLUE, VIOLET, INDIGO,
  Color.BLUE, Color.GREEN, Color.YELLOW, Color.ORANGE, Color.RED};

  public digitalAstronomy()
  {
    setBackground(Color.BLACK);
  }

  public void paintComponent(Graphics g)
  {
    super.paintComponent(g);

    int radius = 20;

    int centerX = getWidth() / 2;
    int centerY = getHeight() - radius-80;

    int centerX_2 = getWidth();
    int centerY_2 = getHeight();

    //Sky
    g.setColor(LIGHTBLUE);
    g.fillRect(0, 0, centerX_2, centerY_2);

    //Rainbow
    for(int c = colors.length; c > 0; c--)
    {
      g.setColor(colors[c-1]);

      g.fillArc(centerX - c * radius, centerY - c * radius,
      c * radius * 2, c * radius * 2, 0, 180);
    }

    //Grass
    g.setColor(Color.GREEN);
    g.fillRect(centerX_2-centerX_2, centerY_2-114, centerX_2, centerY_2);

    //Sun
    g.setColor(Color.YELLOW);
    g.fillOval(centerX_2 - 100, centerY_2 - 450, 30, 30);
  }
}

class digitalAstronomyExe
{
  public static void main(String[]args)
  {
    JFrame app = new JFrame();

    digitalAstronomy panel = new digitalAstronomy();

    app.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

    app.setBackground(Color.BLACK);
    app.add(panel);
    app.setSize(500, 500);
    app.setVisible(true);
  }
}
