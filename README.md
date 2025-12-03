# UKL6FIX

         package com.mycompany.ukl;

        import java.util.Scanner;

       /**
     *
    * @author LOQ
    */
     public class UKL6 {

    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        // Input data
        System.out.print("Nama peminjam: ");
        String nama = input.nextLine();

        System.out.print("Judul buku: ");
        String judul = input.nextLine();

        System.out.print("Kategori buku (A/B/C): ");
        String kategori = input.nextLine().toUpperCase();

        System.out.print("Lama peminjaman (hari): ");
        int lama = input.nextInt();

        // Tarif per kategori
        int tarif = 0;

        switch (kategori) {
            case "A":
                tarif = 2000;
                break;
            case "B":
                tarif = 1500;
                break;
            case "C":
                tarif = 1000;
                break;
            default:
                System.out.println("Kategori tidak valid!");
                return;
        }

        // Hitung biaya awal
        int biayaAwal = tarif * lama;

        // Hitung denda
        int denda = 0;
        if (lama > 7) {
            int hariTerlambat = lama - 7;
            denda = hariTerlambat * 500;
        }

        // Total akhir
        int totalAkhir = biayaAwal + denda;

        // Output
        System.out.println("\n===== STRUK PEMINJAMAN =====");
        System.out.println("Nama Peminjam       : " + nama);
        System.out.println("Judul Buku          : " + judul);
        System.out.println("Kategori Buku       : " + kategori);
        System.out.println("Lama Peminjaman     : " + lama + " hari");
        System.out.println("Biaya Peminjaman    : Rp " + biayaAwal);
        System.out.println("Denda Keterlambatan : Rp " + denda);
        System.out.println("Total Biaya Akhir   : Rp " + totalAkhir);
    }
}

<img width="1063" height="619" alt="Screenshot 2025-12-03 233435" src="https://github.com/user-attachments/assets/e3a51cc9-5484-4b2e-956e-f2caf059bacd" />



