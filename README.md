# CHUYỂN ĐỔI WINDOWS #
  - Bạn đang sử dụng Windows 10 IoT Enterprise LTSC muốn chuyển qua windows 10 Pro thì đây sẽ là vấn đề tốt giúp bạn làm điều đó
  - key [KMS](https://github.com/BsNgChiThanh/KeyKMS) bản windows cần muốn chuyển tới.
 
## Giải pháp: ##
 
### CÁCH 1: ###

  - Chạy **cmd** bằng **Run as Administrator**

  ```php
  sc config LicenseManager start= auto & net start LicenseManager
  sc config wuauserv start= auto & net start wuauserv
  changepk.exe /productkey VK7JG-NPHTM-C97JM-9MPGT-3V66T
  exit
  ```

  - Dán code phía trên vào CMD rồi Enter. Chờ vài phút, máy tính sẽ tự động được khởi động lại và tự động nâng cấp lên Win 10 Pro.
  - **Lưu ý bạn muốn bản Windows này thì lấy key KMS của bản Windows đó thay vào đoạn mã code ở trên.**
    - Ví dụ bản Enterprise thì ta có đoạn mã: 
    
    ```php
    sc config LicenseManager start= auto & net start LicenseManager
    sc config wuauserv start= auto & net start wuauserv
    changepk.exe /productkey DPH2V-TTNVB-4X9Q3-TJR4H-KHJW4
    exit
    ```

### CÁCH 2: ###

  - Chạy **cmd** bằng **Run as Administrator**
  
  ```PHP
  slmgr.vbs /upk
  slmgr.vbs /ckms
  slmgr.vbs /cpky
  slmgr.vbs /rearm
  net stop sppsvc
  cd %windir%\system32\spp\store\2.0
  ren tokens.dat tokens.bar
  net start sppsvc
  cscript.exe %windir%\system32\slmgr.vbs /rilc
  exit
  ```

  - Dán code phía trên vào CMD. Chờ CMD chạy, nếu thấy thông báo thì cứ nhấn OK, cuối cùng nếu thấy hiện dòng C:\Windows\System32\spp\store\2.0>exit thì nhấn Enter, sau đó bạn khởi động lại máy tính rồi mở CMD lên nhập tiếp dòng lệnh sau vào:
    
  ```PHP
  cscript.exe %windir%\system32\slmgr.vbs /ipk VK7JG-NPHTM-C97JM-9MPGT-3V66T
  ```

  - Chờ vài phút, bạn khởi động lại máy tính để Win tự nâng cấp lên Win 10 Pro.

### CÁCH 3: ###

  - Nạp SKUs Windows. Đây là cách cuối cùng, đảm bảo thành công 100%. Bạn thảm khảo cách nạp Skus ở [Hướng Dẫn Nạp SKUs Để Thay Đổi Phiên Bản Windows](https://21ak22.com/huong-dan-nap-skus-de-thay-doi-ban-windows.html) ạ.

 ## KÍCH HOẠT BẢN QUYỀN VĨNH VIỄN: ##

 Tham khảo [tại đây](https://github.com/BsNgChiThanh/Kich-hoat-Windows)

  






    



