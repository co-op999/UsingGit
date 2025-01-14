## Create and Push files by Git
(โปรดใช้วิจารณญาณในการอ่าน🤣 มีตรงไหนผิด แก้ได้เลยคั้บ หรือทัก discord: includna)
### Set git
- Open `Git Bash` or terminal
- cd เข้า folder ก่อน **For `git bash`ต้อง cd เข้าที่ละขั้น (copy ทั้ง path ทีเดียวเลยไม่ได้)
- fullname (ไม่ใช่ username นะ) & email ต้องเป็นอันที่ใช้สมัคร Github acc

```bash
git config --global user.name "<your full name>"
git config --global user.email "<your email>"
git config --global color.ui auto
git config --global merge.conflictstyle diff3
git config --list
```
- ถ้า list ไม่หยุด run ก็ kill ออก

##
#### VS code for commit massage
ไม่ซีเรียส เพราะใช้ git commit -m "your commit massage" ได้

```bash
git config --global core.editor "'<path to VS code>\code.exe' -n -w"
```
---
### Create Git repo
- เปิด project บน Eclipse **จำ path Workspace
- เปิด terminal cd เข้า path workspace นั้น แล้ว cd เข้า folder project
  *** ชื่อ folder project (ที่ข้างในมี files ที่จะเอาขึ้น github) ชื่อ folder ต้องตรงกับชื่อ repository ที่ใช้ส่งงาน เช่น test-submission-incluDna | folder เราก็ต้องชื่อ test-submission-incluDna `ไม่งั้นก็ ✨clone repoอันนั้น เปล่าๆมาเลย ลงในเครื่องเรา แล้วเอาโค้ดไปใส่ใน folder นั้น` *** `git clone https://github.com/.... .git` repoที่ส่งงาน
  
- ค่อยเริ่มตัว git 
```bash
git init
```
- ✨git clone (clone งานนอกมาเข้าเครื่องเรา *กรณีโค้ดเค้าให้มา อยู่ใน github)
```bash
git clone https://github.com/.... .git
```
- Import เข้า Eclipse
- cd เข้า folder ที่เอาเข้ามาแล้ว `git status` เช็คได้
### .gitignore
- [.gitignore for Eclipse](Eclipse.gitignore)
  (https://github.com/github/gitignore/blob/main/Global/Eclipse.gitignore)
- หรือ ดึง file .gitignore จาก complete project
  ```bash
  git clone https://github.com/2110215-ProgMeth/Git_Tutorial_Complete.git
  ```
 ## 
ไปแก้ code ทุกอย่างให้พร้อมเอาขึ้น😁👍
##
### Git commit
ส่วนตัวแนะนำ powershell
- cd เข้า folder ที่จะเอาขึ้น
- Add gitignore
```bash
git add .gitignore
```
- Check สถานะ (ไฟล์ที่มีอยู่...)
```bash
git status
```
- ใส่ commit massage (เวลาทำไรไป แล้วอยากโน้ตไว้)
  ```bash
  git commit
  ```
  ถ้า set VS code ไว้ จะมีหน้าต่าง vs code เด้งให้ใส่ massage -> ใส่เสร็จ -> ctrl+S -> กดออก(ปิด) vs code
or ใส่ massage ที่ command เลย
  ```bash
  git commit -m "add commit massage"
  ```
- Add งานขึ้นไป ถ้าง่ายๆแบบ เอาขึ้นไปหมดเลย
```bash
git add .
```
- อยาก undo
```bash
git checkout -- <path file>
```
### Set Up Remote repo (เอาขึ้น GitHub)
- ที่เราทำมาคือ local repo
- Remote มา
```bash
git remote add origin https://github.com/<url repo for sending work .git>
```
- Push ขึ้นไป
```bash
git push -u origin main
```
### Finish✨🙏
---
### Edit code
- check ก่อนว่า edit code ที่อยู่ในไฟล์ ที่เอาขึ้น github
- จากนั้น ใช้ commands ตามนี้
```bash
git add .
#check by
git status
#if OK
#commit massage
git commit -m "..."
git push
```
