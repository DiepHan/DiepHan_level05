# BÁO CÁO HỌC CON TRỎ  
- Biến con trỏ là biến có chứa địa chỉ của một vùng trong bộ nhớ và có kiểu xác định  
- Mỗi biến khi được khai báo đều được cấp phát cho một vùng nhớ nhất định ở những nơi(địa chỉ)khác nhau  
- Khai báo con trỏ:Với mỗi kiểu dữ liệu ta có tương ứng một biến con trỏ có kiểu đó.
  - Cú pháp: `Kiểu * Tên biến con trỏ;`
  - VD: int *x;
        char *a;  
- Quy định vùng trỏ tới của con trỏ: `Tên con trỏ = &biến;`  
- Cách truy xuất: Với con trỏ px ta có 2 phép tuy xuất là  
  - px : Lấy địa chỉ mà nó lưu giữ (trỏ tới)  
  - *px : Lấy giá trị trong vùng nhớ mà nó trỏ tới.  
Sử dụng con trỏ:  
  - Toán tử "*"
   Lấy giá trị tại địa chỉ đã nào đó.

        Ví dụ:	
        ` gán a = giá trị tại vị trí mà p trỏ vào.//    
        a=*p;`

  - Toán tử "&"
    Cho địa chỉ của biến nào đó.  

        Ví dụ:
        `con trỏ p trỏ vào biến a.     
         p=&a;   
         //a và *p là tương đương. 

## Con trỏ và mảng  
### **Mảng 1 chiều**  
 Trong C có mối quan hệ chặt chẽ giữa con trỏ và mảng, các thành phần của mảng có thể được xác dịnh nhờ chỉ số thông qua con trỏ  
- Phép lấy địa chỉ 
  - Áp dụng được cho các phần tử của mảng một chiều.
    - `double a[20];`
    - khi đó phép toán   
    - `&a[i]`  
    - với i trong khoảng [0,19] cho địa chỉ của phần tử a[i]
- Tên mảng là một hằng địa chỉ    
    - `float a[10];`  
    - Máy sẽ bố trí cho mảng a 10 khoảng nhớ liên tiếp (mỗi khoảng nhớ là 4 byte)   
    - `a` tương đương `&a[0]`  
    - `a+1` tương đương `&a[i]`  
    - `*(a+i)` tương đương `a[i]`  
    - Nếu con trỏ pa trỏ tới một phần tử thứ` a[k]` nào đó thì:  
    - `pa + i` trỏ tới phần tử thứ i sau `a[k]` , tức là `a[k+i]`    
    - `pa - i` trỏ tới phần tử thứ i trước `a[k]` , tức là` a[k-i]`    
    - `*(pa+i)` tương đương với `pa[i]`  


### **Mảng 2 chiều** (tương tự 1 chiều)  
![](http://2.bp.blogspot.com/-X3h8ONrV0SE/U-sj56xBHrI/AAAAAAAABpU/eOvM2HxUcik/s1600/matran.png)





        
