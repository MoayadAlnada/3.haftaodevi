<h2>This code has been written by Visual Studio 2019 via C#.</h2>

<h3>3.hafta ödevi 14/11/2021 ödev açıklaması => Ödeviniz Windows Form uygulaması geliştirmek. Bunun için; Textboxa istenilen kadar girilen sayıların sıralamasını yapan bir form uygulaması istenmektedir. Form da bir textbox, 3 buton (sayı Ekle, Küçükten büyüğe ve büyükten küçüğe) ve 2 listbox olacaktır. Her rakamdan sonra sayı ekleye basılır ve listboxa eklenir. Sırala butonlarına basıldığında 2. listbox da gösterilir.</h3>

![سء](https://user-images.githubusercontent.com/76546216/137386869-87f514bd-15ac-4e71-aadf-72f135cb7578.PNG)




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
