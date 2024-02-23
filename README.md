# tmux
tmux มี 3 layer คือ
### 1. Session
วิธีเข้าคือ (สร้าง session ใหม่ขึ้นเรื่อยๆ)
```
tmux
```
เข้า session ล่าสุดที่เพิ่งออกมา
```
tmux a
```
เข้าใน session ใหม่ พร้อมตั้งชื่อ (ตั้งชื่อว่า test)
```
tmux new -s test
```
เข้าใน session ที่ตัองการ (เข้าไปใน session test)
```
tmux a -t test
```
วิธีออกคือ `Ctrl B` แล้วกด `D` เพื่อ detach   
เช็ค session ที่มีอยู่
```
tmux ls
```
ดูรายการ session ที่มี แล้วเลือกเข้า session ที่ต้องการ กด `Ctrl B` แล้วกด `S`
ลบ session (ลบ session test)
```
tmux kill-session -t test
```
### 2. Window
* สร้าง window ใหม่กด `Ctrl B` แล้วกด `C`
* เลื่อนไป window ถัดไปด้านขวากด `Ctrl B` แล้วกด `N`
* ไป window ที่ต้องการกด  `Ctrl B` แล้วกดหมายเลข index ของ window ที่ต้องการไป
* เปลี่ยนชื่อ window ปัจจุบัน กด `Ctrl B` แล้วกด `,`
* ดูรายการ window ในแต่ละ sessoin แล้วเลือกว่าจะเข้าไปใน pane ไหน กด  `Ctrl B` แล้วกด `W` ในนี้ยังสามารถเลือกแล้วกด `X` เพื่อลบ screen หรือ window ได้
* ลบ window ปัจจุบัน กด `Ctrl B` แล้วกด `&`
### 3. Panes
* สร้าง pane แนวตั้งใหม่ กด `Ctrl B` แล้วกด `%`   
* สร้าง pane แนวนอนใหม่ กด `Ctrl B` แล้วกด `"`   
* ใน pane ที่ใช้งานอยู่จะมีกรอบสีเขียนขึ้น   
* เช็ค index ของ pane กด `Ctrl B` แล้วกด `Q`   
* ย้ายใน pane อื่น กด `Ctrl B` แล้วกดเครื่องหมายลูกศร บน-ล่าง-ซ้าย-ขวา เพื่อไป pane ที่ต้องการ หรือ กด `Ctrl B` แล้วกด `q ตามด้วยindexที่ต้องการไป`
* ลบ pane ปัจจุบัน กด `Ctrl B` แล้วกด `X` 
* กำหนดรูปแบบ pane กด  `Ctrl B` แล้วกด `Alt ตัวเลข` (ตัวเลขมีให้เลือกตั้งแต่ 1ถึง5)
