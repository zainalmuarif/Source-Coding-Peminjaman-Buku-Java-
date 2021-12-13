# Source-Coding-Peminjaman-Buku-Java-

import java.awt.EventQueue;

import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JOptionPane;

import java.awt.Font;
import javax.swing.JPanel;
import javax.swing.border.TitledBorder;
import javax.swing.JTextField;
import java.awt.Color;
import javax.swing.JButton;
import java.awt.event.ActionListener;
import java.awt.event.ActionEvent;

public class Program_APK_JavaGUI {

	private JFrame frame;
	private JTextField txtJudulBuku;
	private JTextField txtPenulis;
	private JTextField txtEdisi;

	/**
	 * Launch the application.
	 */
	public static void main(String[] args) {
		EventQueue.invokeLater(new Runnable() {
			public void run() {
				try {
					Program_APK_JavaGUI window = new Program_APK_JavaGUI();
					window.frame.setVisible(true);
				} catch (Exception e) {
					e.printStackTrace();
				}
			}
		});
	}

	/**
	 * Create the application.
	 */
	public Program_APK_JavaGUI() {
		initialize();
	}

	/**
	 * Initialize the contents of the frame.
	 */
	private void initialize() {
		frame = new JFrame();
		frame.getContentPane().setBackground(Color.WHITE);
		frame.setBounds(100, 100, 634, 385);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.getContentPane().setLayout(null);
		
		JLabel lblNewLabel = new JLabel("Stat'20 BookStore");
		lblNewLabel.setFont(new Font("Tahoma", Font.BOLD, 28));
		lblNewLabel.setBounds(185, 25, 264, 45);
		frame.getContentPane().add(lblNewLabel);
		
		JPanel panel = new JPanel();
		panel.setBackground(Color.ORANGE);
		panel.setBorder(new TitledBorder(null, "Registrasi", TitledBorder.LEADING, TitledBorder.TOP, null, null));
		panel.setBounds(41, 93, 528, 190);
		frame.getContentPane().add(panel);
		panel.setLayout(null);
		
		JLabel lblNewLabel_1 = new JLabel("Judul Buku");
		lblNewLabel_1.setFont(new Font("Tahoma", Font.BOLD, 14));
		lblNewLabel_1.setBounds(21, 35, 155, 30);
		panel.add(lblNewLabel_1);
		
		JLabel lblNewLabel_1_1 = new JLabel("Penulis");
		lblNewLabel_1_1.setFont(new Font("Tahoma", Font.BOLD, 14));
		lblNewLabel_1_1.setBounds(21, 86, 155, 30);
		panel.add(lblNewLabel_1_1);
		
		JLabel lblNewLabel_1_2 = new JLabel("Edisi");
		lblNewLabel_1_2.setFont(new Font("Tahoma", Font.BOLD, 14));
		lblNewLabel_1_2.setBounds(21, 135, 155, 30);
		panel.add(lblNewLabel_1_2);
		
		txtJudulBuku = new JTextField();
		txtJudulBuku.setBounds(172, 42, 297, 23);
		panel.add(txtJudulBuku);
		txtJudulBuku.setColumns(10);
		
		txtPenulis = new JTextField();
		txtPenulis.setColumns(10);
		txtPenulis.setBounds(172, 93, 297, 23);
		panel.add(txtPenulis);
		
		txtEdisi = new JTextField();
		txtEdisi.setColumns(10);
		txtEdisi.setBounds(172, 142, 297, 23);
		panel.add(txtEdisi);
		
		JButton btnNewButton = new JButton("Tampilkan");
		btnNewButton.addActionListener(new ActionListener() {
			public void actionPerformed(ActionEvent e) 
			{
				String judul = txtJudulBuku.getText();
				String penulis = txtPenulis.getText();
				String edisi = txtEdisi.getText();
				JOptionPane.showMessageDialog(null, "Judul Buku : " + judul);
				JOptionPane.showMessageDialog(null, "Penulis : " + penulis);
				JOptionPane.showMessageDialog(null, "Edisi : " + edisi);
			}
		});
		btnNewButton.setBounds(241, 294, 146, 41);
		frame.getContentPane().add(btnNewButton);
	}

}
