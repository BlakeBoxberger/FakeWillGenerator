/**
*Text genereted by Simple GUI Extension for BlueJ
*Main program coded by Uhmmmm
*/
import javax.swing.UIManager.LookAndFeelInfo;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.KeyAdapter;
import java.awt.event.KeyEvent;
import java.awt.event.MouseAdapter;
import java.awt.event.MouseEvent;
import java.awt.event.MouseWheelEvent;
import java.awt.event.MouseWheelListener;
import javax.swing.border.Border;
import javax.swing.*;
import java.util.ArrayList;


public class GUI_project extends JFrame {

    private JComboBox combobox1;
    private JButton enterbutton;
    private JLabel playersAliveLabel;
    private JLabel playersDeadLabel;
    private JTextArea lastwillgenerated;
    private JTextField nameinput;
    private JTextField mynameinput;
    private JButton nightsbutton;
    private JList playersalive;
    private JList playersdead;
    private Players arrayListOfPlayers;

    //Constructor 
    public GUI_project(){

        this.setTitle("GUI_project");
        this.setSize(505,345);

        //pane with null layout
        JPanel contentPane = new JPanel(null);
        contentPane.setPreferredSize(new Dimension(505,345));
        contentPane.setBackground(new Color(192,192,192));

        String[] roleclaimsComboBox = {"Select claim...", "Veteran", "Vigilante", "Lookout", "Sheriff", "Investigator", "BodyGuard", "Doctor", "Escort", "Medium", "Retributionist", "Transporter", "Survivor"};
        combobox1 = new JComboBox(roleclaimsComboBox);
        combobox1.setBounds(238,300,120,35);
        combobox1.setBackground(new Color(214,217,223));
        combobox1.setForeground(new Color(0,0,0));
        combobox1.setEnabled(true);
        combobox1.setFont(new Font("sansserif",0,12));
        combobox1.setVisible(true);
        //Set methods for mouse events
        //Call defined methods        
        combobox1.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent actionEvent) {
                roleclaimSelected(actionEvent);
            }
        });


        enterbutton = new JButton();
        enterbutton.setBounds(145,300,90,35);
        enterbutton.setBackground(new Color(214,217,223));
        enterbutton.setForeground(new Color(0,0,0));
        enterbutton.setEnabled(true);
        enterbutton.setFont(new Font("sansserif",0,12));
        enterbutton.setText("Enter");
        enterbutton.setVisible(true);

        //Set methods for mouse events
        //Call defined methods
        enterbutton.addMouseListener(new MouseAdapter() {
            public void mouseClicked(MouseEvent evt) {
                clickedEnter(evt);
            }
        });


        playersAliveLabel = new JLabel();
        playersAliveLabel.setBounds(37,2,90,25);
        playersAliveLabel.setBackground(new Color(214,217,223));
        playersAliveLabel.setForeground(new Color(0,0,0));
        playersAliveLabel.setEnabled(true);
        playersAliveLabel.setFont(new Font("sansserif",0,12));
        playersAliveLabel.setText("Players Alive");
        playersAliveLabel.setVisible(true);
        
        playersDeadLabel = new JLabel();
        playersDeadLabel.setBounds(169,2,90,25);
        playersDeadLabel.setBackground(new Color(214,217,223));
        playersDeadLabel.setForeground(new Color(0,0,0));
        playersDeadLabel.setEnabled(true);
        playersDeadLabel.setFont(new Font("sansserif",0,12));
        playersDeadLabel.setText("Players Killed");
        playersDeadLabel.setVisible(true);

        lastwillgenerated = new JTextArea();
        lastwillgenerated.setBounds(283,25,210,272);
        lastwillgenerated.setBackground(new Color(255,255,255));
        lastwillgenerated.setForeground(new Color(0,0,0));
        lastwillgenerated.setEnabled(true);
        lastwillgenerated.setFont(new Font("sansserif",0,12));
        lastwillgenerated.setText("Generated Last Will:");
        lastwillgenerated.setBorder(BorderFactory.createBevelBorder(1));
        lastwillgenerated.setVisible(true);

        nameinput = new JTextField();
        nameinput.setBounds(10,300,132,35);
        nameinput.setBackground(new Color(255,255,255));
        nameinput.setForeground(new Color(0,0,0));
        nameinput.setEnabled(true);
        nameinput.setFont(new Font("sansserif",0,12));
        nameinput.setText("Enter names...");
        nameinput.setVisible(true);
        nameinput.addMouseListener(new MouseAdapter() {
            public void mouseClicked(MouseEvent evt) {
                clearNameInput(evt);
            }
        });
        
        mynameinput = new JTextField();
        mynameinput.setBounds(283,1,210,25);
        mynameinput.setBackground(new Color(255,255,255));
        mynameinput.setForeground(new Color(0,0,0));
        mynameinput.setEnabled(true);
        mynameinput.setFont(new Font("sansserif",0,12));
        mynameinput.setText("Type your name...");
        mynameinput.setVisible(true);
        mynameinput.addMouseListener(new MouseAdapter() {
            public void mouseClicked(MouseEvent evt) {
                clearMyNameInput(evt);
            }
        });

        nightsbutton = new JButton();
        nightsbutton.setBounds(361,300,45,35);
        nightsbutton.setBackground(new Color(214,217,223));
        nightsbutton.setForeground(new Color(0,0,0));
        nightsbutton.setEnabled(true);
        nightsbutton.setFont(new Font("sansserif",0,12));
        nightsbutton.setText("N1");
        nightsbutton.setVisible(true);
        //Set methods for mouse events
        //Call defined methods
        nightsbutton.addMouseListener(new MouseAdapter() {
            public void mouseClicked(MouseEvent evt) {
                addNights(evt);
            }
        });


        playersalive = new JList();
        playersalive.setBounds(10,25,130,272);
        playersalive.setBackground(new Color(255,255,255));
        playersalive.setForeground(new Color(0,0,0));
        playersalive.setEnabled(true);
        playersalive.setFont(new Font("sansserif",0,12));
        playersalive.setVisible(true);
        playersalive.addMouseListener(new MouseAdapter() {
            public void mouseClicked(MouseEvent evt) {
                playerKilled(evt);
            }
        });

        playersdead = new JList();
        playersdead.setBounds(147,25,130,272);
        playersdead.setBackground(new Color(255,255,255));
        playersdead.setForeground(new Color(0,0,0));
        playersdead.setEnabled(true);
        playersdead.setFont(new Font("sansserif",0,12));
        playersdead.setVisible(true);
        playersdead.addMouseListener(new MouseAdapter() {
            public void mouseClicked(MouseEvent evt1) {
                playerRevived(evt1);
            }
        });

        //adding components to contentPane panel
        contentPane.add(combobox1);
        contentPane.add(enterbutton);
        contentPane.add(playersAliveLabel);
        contentPane.add(playersDeadLabel);
        contentPane.add(lastwillgenerated);
        contentPane.add(nameinput);
        contentPane.add(mynameinput);
        contentPane.add(nightsbutton);
        contentPane.add(playersalive);
        contentPane.add(playersdead);

        //adding panel to JFrame and seting of window position and close operation
        this.add(contentPane);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        this.setLocationRelativeTo(null);
        this.pack();
        this.setVisible(true);
        
        //Creating Players object
        arrayListOfPlayers = new Players();
    }
    
    //Method mouseClicked for combobox1
    private void roleclaimSelected (ActionEvent actionEvent) {
            String roleclaim = (String)combobox1.getSelectedItem();
            roleclaim = roleclaim.toUpperCase();
            arrayListOfPlayers.setMyName(mynameinput.getText());
            String nightsString = nightsbutton.getText();
            int nights = Integer.parseInt(nightsbutton.getText().substring(1));
            Roleclaim r = new Roleclaim();
            r.claimRole(roleclaim, arrayListOfPlayers, nights);
            String setJTextArea = "";
            for(String line: r.getWill())
            {
                if(line != null)
                    setJTextArea += line + "\n";
            }
            lastwillgenerated.setText(setJTextArea);
    }
    
    private void playerKilled (MouseEvent evt){
        int index = (int) playersalive.getSelectedIndex();
        arrayListOfPlayers.swapPlayer(arrayListOfPlayers.getAlive().get(index), "KILLED");
        playersalive.setListData(arrayListOfPlayers.getAlive().toArray());
        playersdead.setListData(arrayListOfPlayers.getDead().toArray());
    }
    
    private void playerRevived (MouseEvent evt){
        int index = (int) playersdead.getSelectedIndex();
        arrayListOfPlayers.swapPlayer(arrayListOfPlayers.getDead().get(index), "REVIVED");
        playersalive.setListData(arrayListOfPlayers.getAlive().toArray());
        playersdead.setListData(arrayListOfPlayers.getDead().toArray());
    }
    
    private void clearNameInput (MouseEvent evt){
        nameinput.setText("");
    }
    
    private void clearMyNameInput (MouseEvent evt){
        mynameinput.setText("");
    }


    //Method mouseClicked for enterbutton
    private void clickedEnter (MouseEvent evt) {
            String str = nameinput.getText();
            nameinput.setText("");
            arrayListOfPlayers.addPlayer(str);
            playersalive.setListData(arrayListOfPlayers.getAlive().toArray());
    }

    //Method mouseClicked for nightsbutton
    private void addNights (MouseEvent evt) {
            String str = nightsbutton.getText();
            int intInSTR = Integer.parseInt(str.substring(1));
            intInSTR++;
            nightsbutton.setText("N" + intInSTR);
    }


     public static void main(String[] args){
        System.setProperty("swing.defaultlaf", "com.sun.java.swing.plaf.nimbus.NimbusLookAndFeel");
        javax.swing.SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                new GUI_project();
            }
        });
    }

}
