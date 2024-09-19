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

#### Hướng dẫn nạp SKUs Windows: ###
1. Sao chép nội dung trong thư mục SKUs tương ứng với phiên bản muốn chuyển đến:
   - [Windows 10 LTSB 2015](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-10-LTSB-2015.rar), download về giải nén ta được thư mục SKUs-Windows-10-LTSB-2015, chép toàn bộ nội dung này (nếu bạn muốn chuyển bản Windows của mình sang bản Windows 10 LTSB 2015).
   - [Windows 10 LTSB 2016](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-10-LTSB-2016.rar), download về giải nén ta được thư mục SKUs-Windows-10-LTSB-2016, chép toàn bộ nội dung này (nếu bạn muốn chuyển bản Windows của mình sang bản Windows 10 LTSB 2016).
   - [Windows 10 LTSC 2019](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-10-LTSC-2019.rar), download về giải nén ta được thư mục SKUs-Windows-10-LTSC-2019, chép toàn bộ nội dung này (nếu bạn muốn chuyển bản Windows của mình sang bản Windows 10 LTSC 2019).
   - [Windows 10 LTSC 2021](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-10-LTSC-2021.rar), download về giải nén ta được thư mục SKUs-Windows-10-LTSC-2021, chép toàn bộ nội dung này (nếu bạn muốn chuyển bản Windows của mình sang bản Windows 10 LTSC 2021).
   - [SKU Windows 10 khác](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-10.rar)
   - [SKU Windows 11](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-11.rar)
   - [SKUs Windows Server 2016](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-Server-2016.rar)
   - [SKUs Windows Server 2019](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-Server-2019.rar)
   - [SKUs Windows Server 2022](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKUs-Windows-Server-2022.rar)
   - [SKUS Windows 7 Professional](https://raw.githubusercontent.com/BsNgChiThanh/ChuyenDoiWindows/IMP/SKU%20Windows%207%20Professional.rar)
   - Demo:
     - ![image](https://github.com/user-attachments/assets/4a9be6de-c3f9-423c-9ec9-76c432477f07)

2. Dán vào thư mục C:\Windows\System32\spp\tokens\skus của Windows hiện tại.

   - ![image](https://github.com/user-attachments/assets/faffb740-e200-4cce-ad31-1dd07bc453db)

3. Bước này:
   - Bạn gõ cmd vào ô tìm kiếm Windows, nhấn chuột phải vào Command Prompt chọn Run as administrator để mở nó lên. Đảm bảo xuất hiện C:\Windows\system32>.
   - Sau đó sao chép nội dung tương ứng với phiên bản Windows muốn chuyển qua vào CMD là được (nhấn chuột quét toàn bộ rồi sao chép lại, sau đó nhấn chuột phải vào CMD là nó tự động dán nội dung vào).
   - Nếu muốn chuyển Win hiện tại qua Windows 10/11 Pro:
     ```php
     cscript.exe %windir%\system32\slmgr.vbs /rilc
     cscript.exe %windir%\system32\slmgr.vbs /upk >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /ckms >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /cpky >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /ipk VK7JG-NPHTM-C97JM-9MPGT-3V66T
     sc config LicenseManager start= auto & net start LicenseManager
     sc config wuauserv start= auto & net start wuauserv
     clipup -v -o -altto c:\
     echo
     ```
   - Nếu muốn chuyển Win hiện tại qua Windows 10/11 Home:
     ```php
     cscript.exe %windir%\system32\slmgr.vbs /rilc
     cscript.exe %windir%\system32\slmgr.vbs /upk >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /ckms >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /cpky >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /ipk YTMG3-N6DKC-DKB77-7M9GH-8HVX7
     sc config LicenseManager start= auto & net start LicenseManager
     sc config wuauserv start= auto & net start wuauserv
     clipup -v -o -altto c:\
     echo
     ```
   - Nếu muốn chuyển Win hiện tại qua Windows 10 LTSC 2021:
     ```php
     cscript.exe %windir%\system32\slmgr.vbs /rilc
     cscript.exe %windir%\system32\slmgr.vbs /upk >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /ckms >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /cpky >nul 2>&1
     cscript.exe %windir%\system32\slmgr.vbs /ipk M7XTQ-FN8P6-TTKYV-9D4CC-J462D
     sc config LicenseManager start= auto & net start LicenseManager
     sc config wuauserv start= auto & net start wuauserv
     clipup -v -o -altto c:\
     echo
     ```
   - Tương tự các bản Windows khác, bạn chỉ cần thay Key KMS trong dòng lệnh: **cscript.exe %windir%\system32\slmgr.vbs /ipk <Key KMS>** là được.
   - Chờ CMD chạy xong, bạn khởi động lại máy tính là thành công ạ!
      
 ## KÍCH HOẠT BẢN QUYỀN VĨNH VIỄN: ##

 Tham khảo [tại đây](https://github.com/BsNgChiThanh/Kich-hoat-Windows)
