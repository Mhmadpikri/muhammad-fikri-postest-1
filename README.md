//Muhammad fikri
//2109106010

#include <iostream>
using namespace std;

//membuat variabel saya menggunakan variable a dan b
//variabel a untuk menginput data
//variabel b untuk menginput banyaknya ruang yang tersedia buat data
//variabel af mendefinisikan a faktorial
//variabel bf mendefinisikan b faktorial
//variabel bkf mendefinisikan b - 1 faktorial

int main() {
	double a,b, af = 1, bf = 1, bkf = 1, hasil;
	int selection;
	bool loop = true, loop2;
	
	cout<<"== menentukan nilai permutasi atau kombinasi ==/n"<<endl;
//kemudian menggunakan while untuk pengulangan/ kondisi
	while(loop) {
		loop2 = true;
		cout<<"masukkan nilai a : "; cin>>a;
		cout<<"masukkan nilai b : "; cin>>b;
		cout<<endl;
//enggunakan if ntuk beberapa kondisi	
		if (a > b){
			while(loop2){
				cout<<"pilih salah satu\n 1.kombinasi \n 2.permutasi \n 3.ingin mencoba nilai lain? \n 4. exit \n"<<endl;
				cout<<"pilih lah : "; cin>>selection; cout<<endl;
//kemudian menggunakan switch untuk percabangan 				
				switch (selection){
					case 1 :
//kemudian menngunakan rumus kombinasi untuk di case 1
            			for (int x = a; x>0; x--){
             				 af = x*af;
            			}
            
            			for (int y = b; y>0; y--){
              				bf = y*bf;
            			}
            			
            			for (int y = b; y>0; y--){
              				bf = y*bf;
            			}
            
            			for (int z = a-b; z>0; z--){
              				bkf = bkf*z;
            			}
            			hasil = af/(bf*bkf);
            			cout<<"Hasil Kombinasinya adalah :  "<<hasil<<"\n"<<endl;
            			bf = 1, bf = 1, bkf=1;
            			break;
					case 2 :
//lalu menggunakan rumus permutasi untuk di case ke 2
						for (int x = a; x>0; x--){
							af = x*af;
						}
						for (int y = a - b; y>0; y--){
							bkf = y*bkf;
						}
						hasil = af/bkf;
            			cout<<" Hasil Permutasinya adalah "<<hasil<<"\n"<<endl;
            			af = 1, bkf = 1;
            			break;
            		case 3 :
//jika milih pilihan 3 untuk masuukan nilai yang baru
            			cout<<"....."<<endl;
            			loop2 = false;
           			 	break;
//pilihan ke 4 untuk keluar dari program  
           			case 4 :
            			cout<<"Terima Kasih semoga sesuai yang diinginkan";
            			loop = false;
           			 	loop2 = false;
            			break;
            			
            		default :
            			cout<<"pilihan yang anda masukkan tidak tersedia\nMOHON PILIH SESUAI DENGAN ANGKA YANG TERTERA!"<<endl;
            			continue;
				}
			}
		}
		else{
      	   cout<<"nilai a tidak boleh lebih kecil dari nilai b\nsilakan masukkan data kembali..."<<endl;
      }
    }
    return 0;
}
