
# 🧠 Git & GitHub Workflow Notes

## 🚀 เริ่มต้นโปรเจกต์ (Initial Setup)

```bash
git init
```

สร้าง Git repository ในเครื่อง

> ⚠️ แนะนำ: สร้าง `.gitignore` ก่อน `git add .`  
> โดยเฉพาะโปรเจกต์ Next.js / Node.js เพื่อไม่ให้ push ไฟล์ที่ไม่จำเป็น

```bash
git add .
git commit -m "first commit"
git branch -M main
git remote add origin <REPO_URL>
git push -u origin main
```

📌 หรือถ้ามีโปรเจกต์อยู่แล้วบน GitHub:

```bash
git clone <REPO_URL>
```

---

## ⚙️ ตั้งค่า Git ครั้งแรก (Global Config)

```bash
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

---

## 🔄 Workflow การทำงานประจำวัน (Daily Workflow)

```bash
git status
```

เช็คสถานะไฟล์

```bash
git add .
```

เพิ่มไฟล์เข้า staging

```bash
git commit -m "your message"
```

บันทึกการเปลี่ยนแปลง

```bash
git push origin <branch>
```

ส่งโค้ดขึ้น GitHub

---

## 🔁 การ Sync ข้อมูล (Update Code)

```bash
git fetch
```

ดูว่ามีอะไรอัปเดต (ยังไม่ merge)

```bash
git pull
```

ดึง + merge อัตโนมัติ

---

## 🌿 การจัดการ Branch

```bash
git branch
```

ดู branch ทั้งหมด

```bash
git checkout -b <branch>
```

สร้างและสลับ branch

```bash
git checkout <branch>
```

สลับ branch

```bash
git merge <branch>
```

รวม branch

```bash
git branch -d <branch>
```

ลบ branch

---

## ❗ Best Practice (สำคัญมาก)

❌ **ห้ามทำงานบน `main` ตรงๆ**

✅ ใช้ feature branch เช่น:

```bash
git checkout -b feature/login-page
git checkout -b feature/navbar
```

---

## 🧩 Workflow การทำงานเป็นทีม

### 1. ก่อนเริ่มงาน

```bash
git checkout main
git pull origin main
git checkout -b feature/<feature-name>
```
### 2. เมื่อทำงานเสร็จ

```bash
git add .
git commit -m "feat: add login page"
git push origin feature/<feature-name>
```
### 3. เปิด Pull Request (PR)

- เข้า GitHub
    
- กด **Compare & pull request**
    
- Review code
    
- Merge เข้า branch เป้าหมาย
     feature/login -> dev

---

## 🏗️ โครงสร้าง Branch ที่แนะนำ

```
main      → production (stable)
dev       → รวมงานทั้งหมด
feature/* → งานย่อย
```

```
main
 └── dev
      ├── feature/login
      ├── feature/navbar
      └── feature/dashboard
```

---

## 🔧 การใช้งาน dev branch

### สร้าง dev ครั้งแรก

```bash
git checkout main
git checkout -b dev
git push -u origin dev
```

---

### Workflow การทำงาน

#### 1. แตก branch จาก dev

```bash
git checkout dev
git pull origin dev
git checkout -b feature/login
```

---

#### 2. ทำงาน + push

```bash
git add .
git commit -m "feat: add login"
git push origin feature/login
```

---

#### 3. Merge เข้า dev

- เปิด PR: `feature/login → dev`
    
- Test ผ่าน → merge
    

---

#### 4. Deploy

- เมื่อ `dev` stable → merge เข้า `main`
    

---

## 🧰 คำสั่งเสริม

```bash
git log
git log --oneline
```

ดู commit history

```bash
git remote -v
```

ดู remote URL

```bash
git reset --hard
```

ย้อนกลับทั้งหมด (⚠️ อันตราย)

---

## ⏪ ย้อนเวอร์ชัน

```bash
git checkout <commit-id>
```

เช่น:

```bash
git checkout 69e3vt5
```

กลับไปล่าสุด:

```bash
git switch -
```

---

## 💡 Tips เพิ่มเติม

- ใช้ commit message แบบมีมาตรฐาน เช่น:
    
    - `feat:` ฟีเจอร์ใหม่
        
    - `fix:` แก้ bug
        
    - `refactor:` ปรับโครงสร้าง
        
    - `docs:` แก้เอกสาร
        
- อย่าใช้ `git add .` เสมอไป → บางทีควรเลือกไฟล์:
    

```bash
git add file.js
```

- ใช้ `.gitignore` ให้ดี เช่น:
```
node_modules
.env
.next
dist
```
