import java.util.Scanner;
import java.util.List;
import java.util.ArrayList;
import java.text.SimpleDateFormat;
import java.util.Date;

public class Main {
    public static void main(String[] args) throws java.text.ParseException {
        Scanner hsm = new Scanner(System.in);
        PenyewaanPerlengkapanCamp penyewaan = null;
        String username;
        String password;
        //login
        akun login = new akun();
        boolean loggedIn = false;
        
        do {
            System.out.print("Masukan Username = "); String inputUsername = hsm.next();
            System.out.print("Masukan Password = "); String inputPassword = hsm.next();
            
            loggedIn = login.cekLogin(inputUsername, inputPassword);
            
            if (!loggedIn) {
                System.out.println("Username atau Password salah. Coba lagi");
            }
        } while (!loggedIn);
        
        int choice;
        System.out.println("\nPerlengkapan yang Tersedia = ");
        System.out.println("1. Sewa Perlengkapan");
        System.out.println("2. Lihat Nota Penyewaan");
        System.out.println("3. Keluar");
        
        List<PerlengkapanCamp> daftarPerlengkapan = new ArrayList<>();
        daftarPerlengkapan.add(new PerlengkapanCamp("Tenda Kapasitas 2 Orang",50.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Tenda Kapasitas 4 Orang",75.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Tenda Kapasitas 6 Orang",120.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Paket Tenda 2 Orang",200.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Paket Tenda 4 Orang",240.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Paket Tenda 6 Orang",280.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Nesting",30.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Sleeping Bag",80.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Kompor",50.0));
        daftarPerlengkapan.add(new PerlengkapanCamp("Gas",25.0));

        do {    
            System.out.print("Pilih menu (1/2/3) = ");
            choice = hsm.nextInt();
    }
}
