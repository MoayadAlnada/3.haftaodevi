/*Ödeviniz Windows Form uygulaması geliştirmek. Bunun için; Textboxa istenilen kadar girilen sayıların sıralamasını yapan bir form uygulaması istenmektedir. Form da bir textbox, 3 buton (sayı Ekle, Küçükten büyüğe ve büyükten küçüğe) ve 2 listbox olacaktır. Her rakamdan sonra sayı ekleye basılır ve listboxa eklenir. Sırala butonlarına basıldığında 2. listbox da gösterilir. Visual Studio 2019 C# */
![سء](https://user-images.githubusercontent.com/76546216/137385403-9f00aa32-354a-4f0c-8b52-796d7e867d14.PNG)

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
