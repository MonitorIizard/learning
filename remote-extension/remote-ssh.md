# SSH extension

## มันคือ ?
extension ช่วยให้เเก้ไขไฟล์บน `hostremote` บน `vscode`ที่อยู่บนเครื่องเรา โดย ไม่ต้องใช้ `sftp` put file ขึ้น host 

ตัวอย่าง : https://www.youtube.com/watch?v=Y3qQk_URAzM


![alt text](extension.png)

## วิธีใข้

1. โหลด

2. connect to host โดยพิมพ์ `ctrl + p + > ` บน window, `cmd + p + >` บน mac
พิมพ์หา `remote-ssh: connet to host`
![text](command-prompt.png)

3. Add host
![alt text](add-host.png)

4. กรอก `username`@`ip` เเละกรอกรหัส

![alt text](host.png)

5. ใส่รหัสไป

6. เลือก folder ที่จะทำงาน
![alt text](choose-folder.png)

![alt text](choose-folder2.png)

![alt text](choose-folder3.png)

เเล้วคราวนี้พอเเก้ อะไีรในไฟล์ก็ตามก็เพียงเเค่ `save` -> `refresh` browser เเล้วก็จะได้หน้าเว็บใหม่โดยไม่ต้องพิมพ์ คำสั่ง `put`

cr: ผู้ค้นพบ ชื่อเล่น fuse