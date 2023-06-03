#Tóm tắt lý thuyết cần lưu ý và code mẫu.

1.  Lý thuyết.

a.  Biến và kiểu dữ liệu

```cpp
long long so_nguyen;
double So_Thuc;
long long MangA[1000];
bool check;
```

b. Mảng.

Mảng nên lưu từ phần tử 0 và nên được khai báo lớn hơn kích thương mong muốn một chút.

c. Thư viện.

```cpp
#include <bits/stdc++.h>
```
d. Câu lệnh điều kiện.
```cpp
if (DieuKien){
    CauLenh1;
    Caulenh2;
    CauLenh3;
    ...
}else{
    CauLenh4;
    CauLenh5;
    ...
}
Câu Lệnh 1 2 3 sẽ được thực hiện khi điều kiện đúng.
Câu lệnh 4 5 sẽ được thực hiện khi điều kiện sai.
```

2. Code mẫu.

a. **Bài tập kiểm tra số nguyên tố.**

```cpp
bool KiemTraSoNguyenTo(long long x){
     long long gioiHanKiemtra = sqrt(x);
     long long viTriBatDau = 2;
     if (x<2){
        return false;
     }
     for (int i = viTriBatDau ; i<= gioiHanKiemtra ; i++){
        if (x%i == 0){
            return false;
        }
     }
     return true;
}
```

cách sử dụng.

```cpp
int main()
{
    check = KiemTraSoNguyenTo(SoCanKiemTra);
    // ex: check = KiemTraSoNguyenTo(10);
}
```
Check sẽ nhập giá trị là true hoặc false. Nếu true thì số kiểm tra là số nguyên tố, false thì số kiểm tra không phải là số nguyên tố.

b. Sắp xếp:

sử dụng sắp xếp từ nhỏ đến lớn.

```cpp
int main()
{
    sort(MangA+1, MangA+1+n);
}
```

Trong đó MangA là mảng cần phải sắp xếp. *+1* vì mảng bắt đầu lưu ở vị trí 1. 
kết thúc là *+1+n* với *n* là số phần tử của mảng cần phải sắp xếp.


Tùy chỉnh điều kiện sắp xếp.
```cpp
bool DieuKienSapXep(long long trai, long long phai){
    return trai>phai;
}
int main()
{
    sort(MangA+1, MangA+1+n, DieuKienSapXep);
}
```

Ví dụ: Muốn sắp xếp mảng theo thứ tư giảm dần thì phần tử phía trước sẽ lớn hơn phần tử phía sau. khi đó ta có *trai*>*phai*

ex. Mảng kết quả là 5 4 3 2 1. Ta thấy phần tử lên trái lớn hơn phần từ bên phải. Khi đó điều kiện trả về của hàm sẽ là trai>phai.

Điều kiện nên được linh hoạt theo ý muốn của đề bài.

c. Tìm ước chung lớn nhất.

```c++
int main()
{
    long long ucln;
    ucln = __gcd(soThuNhat, soThuHai);
    //ex : ucln = __gcd(3,4)
}
```


3. Một số lưu ý.

a. Với các giá trị khởi tạo 
```cpp
Tong = 0; 
Tich =1;
GiaTriNhoNhat = 100000; // Hoặc một số nào đó đủ lớn là được.
GiaTriLonNhat = -1000000; // Hoặc một số nào đủ đủ nhỏ là được
```




