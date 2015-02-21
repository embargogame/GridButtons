# GridButtons
import java.awt.*; 
import java.awt.event.*; 
import javax.swing.*; 

public class gridTester extends JFrame
{
  
   JButton[][] gridButtons; // Grid of Button
   
   public static void main(String [] args)
   {
      //makes new ButtonGrid with 2 parameter
      new gridTester(3,3); 
   }
   
   public gridTester(int width,int length)
   {
      setLayout(new GridLayout(width, length));
      
      //allocate the size of grid
      gridButtons = new JButton[width][length]; 
      
      for (int y=0; y<length; y++){
         for(int x=0; x<length; x++){
         
            //creates new buttons
            gridButtons[x][y] = new JButton("("+x+","+y+")"); 
            
            //adding buttons to grid 
            add(gridButtons[x][y]); 
         }
      } 
      setDefaultCloseOperation(EXIT_ON_CLOSE); 
      setSize(300,300);  
      setVisible(true); 
      
   }
}
