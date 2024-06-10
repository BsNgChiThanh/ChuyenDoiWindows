# CHUYỂN ĐỔI WINDOWS #
Bạn đang sử dụng Windows 10 IoT Enterprise LTSC muốn chuyển qua windows 10 Pro thì đây sẽ là vấn đề tốt giúp bạn làm điều đó

## Giải pháp: ##
  - Xóa sạch key Widows
  - Install key [KMS](https://github.com/BsNgChiThanh/KeyKMS) bản windows cần muốn chuyển tới.
  - Retart lại máy tính.
  - Dùng MASS Tools để kích hoạt windows là xong.

### Cụ thể: ###
  - Tôi đang sử dụng Windows 10 IoT Enterprise LTSC, tôi muốn chuyển quan widows 10 Pro, làm như sau:
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/f358d99c-f453-488e-be51-77a90c5186f1)
  - Chạy **cmd** bằng **Run as Administrator**.
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/318e3df7-7440-49a0-801c-3fc6b6894573)
  - Dán lần lượt 3 lệnh và bấm enter:

    ```php
    slmgr /upk
    slmgr /cpky
    slmgr /rearm
    ```
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/688ee126-b15e-401c-85fd-761b07a37a82)
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/0518f962-3f7a-4b14-8054-d15bf8380d80)
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/597e38bf-5cd0-4790-b4a0-5916e95e0e6b)
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/825b1e81-04d6-4b6e-8393-9301e2214a55)
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/adf64eed-9522-4ce4-bef4-156522357334)
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/3e7a5ce0-d723-4cf8-af2c-a28b9ba2d990)
  - Khởi động máy lại.
  - Bây giờ lấy key [KMS](https://github.com/BsNgChiThanh/KeyKMS) Windows 10 Pro nhận vào là xong.
  - Chạy **cmd** bằng **Run as Administrator**.
  - Dán toàn bộ câu lệnh sau đây vào và nhấn enter hoặc dán từng câu lệnh cũng được:
    ```php
    slmgr.vbs /ipk W269N-WFGWX-YVC9B-4J6C9-T83GX
    slmgr /skms kms.xspace.in
    slmgr.vbs /xpr
    slmgr /ato
    ```
  - W269N-WFGWX-YVC9B-4J6C9-T83GX là key KMS Windows 10 Pro.
  - ![image](https://github.com/BsNgChiThanh/ChuyenDoiWindows/assets/82578024/e8e31e3e-7d31-4a15-a82b-8f33377bc674)
  - ...
  - ...
  - Vậy bạn đã có một bản Windows 10 Pro dùng thử 180 ngày, muốn sử dụng vĩnh viễn bạn dùng key MAK hoặc retail để kích hoạt hoặc dùng https://github.com/BsNgChiThanh/MAS-TOOL để kích hoạt vĩnh viễn.
  - Done!

  






    



