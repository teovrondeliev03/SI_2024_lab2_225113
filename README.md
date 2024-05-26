# Втора лабораториска вежба по Софтверско инженерство
## Teo Vrondeliev, бр. на индекс 225113
# SI_2024_lab2_225113
### Control Flow Graph
![finalv2](https://github.com/teovrondeliev03/SI_2024_lab2_225113/blob/master/SI_lab2.jpg)
### 3. Ciklomatskata kompleksnost
Ciklomatskata kompleksnost na kodot, presmetana so metodot na broenje predikatni jazli (P+1 kade sto P e 9), e 9+1=10.
### 4. Every Branch
   -allItems==nul Za da go pokrieme prviot exception -allItems[null,"0123",301,0.1] , 0 So ova se pokriva if-ot za name==null, if-ot za validen barcode, if-ot za discount pogolem od 0, if-ot za item.getPrice() > 300 && item.getDiscount() > 0 && item.getBarcode().charAt(0) == '0' i if-ot sum <= payment koj vrakja true. -allItems["name",null,200,0.1] , 0 Ovoj test case kje sluzi za da go pokrieme isklucokot za barcode ako e null. -allItems["name","12a",200,0.1] , 0 Test primerov sluzi za da se pokrie frlanjeto na exepcion za nevaliden karakter vo barcode. -allItems["name","123",200,0] , 0 Go pokrivame posledniot if (sum <= payment), else-ot kje vrati false.
### 5. Multiple Condition
if(item.getPrice()>300 && item.getDiscount()>0 && item.getBarcode().charAt(0)=='0') 2^3 => 8 test cases T || X || X koga price > 300 F || T || X koga price <= 300, a discount > 0 F || F || T koga price <= 300 i discount <= 0 i prvata cifra na barcode e 0 F || F || F koga price <= 300 i discount <= 0 i prvata ne e 0
