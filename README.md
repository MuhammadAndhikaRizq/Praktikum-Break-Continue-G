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
