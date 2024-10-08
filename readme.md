ใช้งาน package
เมื่อทุกอย่างเสร็จสิ้น คุณสามารถใช้งาน package ของคุณในโปรเจ็กต์ Go อื่น ๆ ได้โดยการนำเข้า:

```
import "github.com/yourusername/mypackage"

func main() {
    fmt.Println(mypackage.HelloWorld())
}

```
ตรวจสอบเอกสารและตัวอย่าง
คุณสามารถตรวจสอบเอกสารของ package และดูตัวอย่างการใช้งานได้จาก pkg.go.dev หลังจากที่ทุกอย่างพร้อมแล้ว

ทำตามขั้นตอนเหล่านี้เพื่อสร้างและเผยแพร่ Go package ของคุณบน pkg.go.dev!

ใช้เวอร์ชันที่มีแท็ก: หาก repository ของคุณไม่มี tag ที่ระบุเวอร์ชัน (v0.1.0 หรือสูงกว่า) ให้คุณสร้าง tag ใหม่ตาม semantic versioning

วิธีเพิ่ม tag:

ใน command line ให้รันคำสั่ง
bash
Copy code
git tag v0.1.0
git push origin v0.1.0
Go Module พร้อมใช้งาน: ตรวจสอบว่า project ของคุณมีไฟล์ go.mod ซึ่งเป็นไฟล์ที่ใช้บ่งบอกว่าเป็น Go module และระบุ dependencies ต่างๆ ให้ชัดเจน

ถ้ายังไม่มีไฟล์ go.mod ให้รันคำสั่งนี้ใน root ของ project:

bash
Copy code
go mod init github.com/noom1009/ospframeworks
ใช้คำสั่ง go list เพื่อเช็คการใช้งาน: คุณสามารถใช้คำสั่งนี้เพื่อดูว่า module ของคุณทำงานได้ถูกต้องหรือไม่

bash
Copy code
go list -m github.com/noom1009/ospframeworks
ตรวจสอบบน pkg.go.dev: ไปที่เว็บไซต์ pkg.go.dev แล้วค้นหาชื่อ package ของคุณ ถ้าเป็น public repository และมี tag version ที่เหมาะสม มันจะถูกดึงขึ้นโดยอัตโนมัติ