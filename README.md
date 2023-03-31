# transaksiPBO1
/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Classes/Main.java to edit this template
 */
package transaksipbo;
import java.util.Scanner;
/**
 *
 * @author ravertz
 */
public class TransaksiPBO {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int harga_32gb=50000;
        int harga_64gb=75000;
        
        int jumlah_32gb= 0;
        int jumlah_64gb= 0;
        
        int total_harga = 0;
        
        do{
        System.out.println("Pilih barang yang ingin dibeli: ");
        System.out.println("1. Flashdisk 32 Gb (Rp. 50.000,)");
        System.out.println("2. Flashdisk 64 Gb (Rp. 75.000,)");
        int pilihan_barang = input.nextInt();
        
        switch (pilihan_barang){
            case 1:
                jumlah_32gb++;
                total_harga += harga_32gb;
                break;
            case 2:
                jumlah_64gb++;
                total_harga += harga_64gb;
                break;
            default: 
                    System.out.println("Maaf pilihan yang anda masukkan salah!");
                break;
        }
        
        System.out.println("Jumlah barang yang ingin dibeli: ");
        System.out.println("- Flashdisk 32gb: "+ jumlah_32gb);
        System.out.println("- Flashdisk 32gb: "+ jumlah_64gb);
        System.out.println("Total harga: Rp. "+ total_harga);
        System.out.println("Lanjutkan Transaksi (Y/N)");
        char lanjutkan = input.next().charAt(0);
        
        if (lanjutkan == 'n'){
                break;
            }
        
        }while(true);   
        System.out.println("Total harga keseluruhan: Rp. " + total_harga);
        System.out.println("Terima kasih telah berbelanja!");
    }
    
}
