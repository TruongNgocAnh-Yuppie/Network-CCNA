# Static MAC

## 1. Đề bài

![1](/image/2023-03-10-1.png)

- Đặt địa chỉ IP cho Router: 
        
| Router | Cổng | Địa chỉ |       
| -- | ---- | -------- |        
| R1 | e0/0 | 10.1.2.1 |
|    | Lo0 | 1.1.1.1 |
| R2 | e0/0 | 10.1.2.2 |
|    | e0/1 | 10.2.3.2 |
|    | e0/2 | 10.2.4.2 |
|    | Lo0 | 2.2.2.2 |
| R3 | e0/0 | 10.2.3.3 |
|    | e0/1 | 10.3.5.3 |
|    | Lo0 | 3.3.3.3 |
| R4 | e0/0 | 10.4.5.4 |
|    | e0/1 | 10.2.4.4 |
|    | Lo0 | 4.4.4.4 |
| R5 | e0/0 | 10.3.5.5 |
|    | e0/1 | 10.4.5.5 |
|    | Lo0 | 5.5.5.5 |
|    | Lo1 | 55.55.55.55 | 

- Định tuyến trên các Router: ip route `địa chỉ (vùng) mạng đích` `subnetmask` `ip next hop/cổng ra` 
- R1: 

![2](/image/2023-03-10-2.png)

- R2:
 
![3](/image/2023-03-10-3.png)

- R3: 

![4](/image/2023-03-10-4.png)

- R4: 

![5](/image/2023-03-10-5.png)

- R5: 

![6](/image/2023-03-10-6.png)

### Default Route tại R1 và R2 mà đang lỗi nên route trực tiếp từ R1 đến các vùng mạng con. Đọc lại thì phải khắc phục được lỗi này.

- Traceroute từ R1 đến các vùng Lo của Router5

![7](/image/2023-03-10-7.png)
