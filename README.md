# PraktikumBreak1
## Menentukan kecepatan processor pada smartphone

```

#include <iostream>

using namespace std;

struct productT {
  int no;
  string merk;
  int ram;
  string processor;
  int core;
};

int main() {

  productT product[] = {
    {
      1,
      "Samsung",
      8,
      "Exynos",
      8
    },
    {
      2,
      "Huawei",
      12,
      "kirin",
      8
      
    },
    {
      3,
      "Apple",
      8,
      "Bionic",
      12
    },
    {
      4,
      "Realme",
      4,
      "Unisoc",
      6
    },
    {
      5,
      "Asus",
      8,
      "SnapDragon",
      8
    }
  };

  int JumlahCoreTerlambat = 4;
  int CoreYangSama = 8;
  int JumCore = 0;
  
  product[2].merk = "Apple";

  cout<< " Merk Smartphone dengan jumlah core processor yang sama : \n ";
  while (JumCore <= 5){
  	if (product[JumCore].core == CoreYangSama){
  		cout << " Merk Smartphone " << product[0].merk << ", " << product[1].merk << " dan " << product[4].merk << " memiliki jumlah core processor yang sama !!! \n";
  		JumCore++;
      	break;
	  }
  	}
  	cout<<" "<<endl;
  	
  
  for (int i = 0; i < 5; i++)
   {
	
    if (product[i].no == JumlahCoreTerlambat) {
      cout << " " <<endl;
      cout<<" Merk Smartphone dengan processor yang lambat : \n ";
      cout << " Merk Smartphone " << product[i].merk << " memiliki processor yang lambat !!! \n";
      break;
    }
	
	cout <<" Merk Smartphone Dengan Spesifikasi Lengkap : \n ";
    cout << " Merk Smartphone " << product[i].merk << " RAM " << product[i].ram << " GB " << " Jenis Processor " << product[i].processor << " Jumlah Core "<< product[i].core << "\n";
    
  }

}

```

# PraktikumContinue1
## Menentukan harga smartphone dari yang affordable sampai flagship

```
#include <iostream>
using namespace std;

struct productT {
    int no;
    string merk;
    string processor;
    int harga;
};

int main() {
    
    int hargaTerjangkau = 2500000;
    
    productT product[] = {
        {1, "Samsung", "Exynos", 15000000},
        {2, "Huawei", "Kirin", 13000000},
        {3, "Iphone", "Bionic", 17000000},
        {4, "Realme", "Unisoc", 1900000},
        {5, "Asus", "SnapDragon", 2300000},
    };
    
	
    for(int i = 0; i < 5; i++) {
        
        if(product[i].harga > hargaTerjangkau) {
            continue;
        }
        
        cout << " Rekomendasi Merk Smartphone Affordable : \n ";
        cout << " Rekomendasi Smartphone Terjangkau " << product[i].merk << " Dengan Processor " << product[i].processor << " Pilihan Terbaik !! " "\n";
    }
    
    cout<<" " <<endl;
    int flagship = 0;
    
    while (flagship < 5){
    	if(product[flagship].harga < hargaTerjangkau){
    		continue;
		}
		cout << " Rekomendasi Smartphone mid range dan flagship : \n ";
		cout << " Merk " << product[flagship].merk << " Dengan Processor " << product[flagship].processor << " Pilihan Terbaik !! \n ";
		flagship++;
		
	}
    
}

```
