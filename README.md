NAMA        : SARIPUDIN  
KELAS       : TI22B1  
NIM         : 312210077  
MATA KULIAH : PEMOGRAMAN OREANTASI OBJEK  

# INHERINTANCE_C#

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Tugas4Pert7
{
    public class Pegawai
    {

        // SARIPUIDN 312210077 
        private string nama;
        private double gajiPokok;

        public void setNama(string nama)
        {
            this.nama = nama;
        }
        public string getNama() { return this.nama; }

        public double getGajiPokok() { return this.gajiPokok; }

        public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

        public void cetakinfo()
        {

            Console.WriteLine("Nama : " + this.nama);
            Console.WriteLine("Gapok : " + this.gajiPokok);
        }
    }


    public class manager : Pegawai
    {

        private double tunjangan;

        public void setTunjangan(double tunjangan) { this.tunjangan = tunjangan; }
        public double getTunjangan() { return this.tunjangan; }

        public new void cetakinfo()
        {

            base.cetakinfo();
            this.cetakTunjangan();
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + this.tunjangan);

        }
    }

    public class Programmer : Pegawai
    {
        private double bonus;


        public void setBonus(double bonus) { this.bonus = bonus; }

        public double getBonus() { return this.bonus; }

        public new void cetakinfo()
        {
            base.cetakinfo();
            this.cetakBonus();
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus : " + this.bonus);


        }

    }
    class program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("==== PEGAWAI PTT/PT ====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("saripudin");
            pegawai.setGajiPokok(6000000);
            pegawai.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== MANAGER SBU  ====");
            manager Manager = new manager();
            Manager.setNama("andi setiawan");
            Manager.setGajiPokok(9000000);
            Manager.setTunjangan(90000000);
            Manager.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== PROGRAMMER SI ====");
            Programmer programer = new Programmer();
            programer.setNama("yusup");
            programer.setGajiPokok(10000000);
            programer.setBonus(100000000);
            programer.cetakinfo();
            Console.WriteLine();


            Console.WriteLine("press anykey");
            Console.ReadKey();
        }
    }
}

```
# HASIL NYA

![Screenshot (174)](https://github.com/ariep1993/inherintance_c-/assets/115473865/a62cabed-34de-43fe-ad0d-b4b6c74ae2f7)
