# 3.haftaodevi
3. Hafta ödevi 201601716
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace _3.Ödev_1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
            
        }
        private List<int> Numbers = new List<int>();
        private void button1_Click(object sender, EventArgs e)
        {
            int sayi = (0);
            int.TryParse(textBox1.Text, out sayi);
            Numbers.Add(sayi);
            Sırasız.DataSource = null;
            Sırasız.Items.Add(textBox1.Text);


        }

        private void button2_Click(object sender, EventArgs e)
        {
            Sıralı.DataSource = null;
            Sıralı.DataSource = Numbers.OrderByDescending(s => s).ToList();
        
        }

        private void button3_Click(object sender, EventArgs e)
        {
            
        }

        private void listBox1_SelectedIndexChanged(object sender, EventArgs e)
        {

        }

        private void button3_Click_1(object sender, EventArgs e)
        {
            Sıralı.DataSource = null;
            Sıralı.DataSource = Numbers.OrderBy(s => s).ToList();
        }
    }
}
