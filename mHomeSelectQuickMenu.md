## Keywords
- [mHomeSelectQuickMenu](#mhomeselectquickmenu)

### Description
`mHomeSelectQuickMenu` ใช้สำหรับการเลือก Quick Menu ในหน้า Home โดยรับ [Arguments] 2 ตัว ได้แก่:

- **`${QuickMenu}`**: ชื่อเมนู (19 เมนู) ตอนส่งให้ส่งเป็น EN เช่น
  - Pay/Top-up, My Bill, Usage, Net/Call, Roaming, AIS Fibre, Online Store, myNetwork, Support, Receipt, Other Bills,
  - Convert to Postpaid, Move to AIS, Activate SIM, AIS PLAY, Game, Insurance, Finance, Wellness
- **`${TimeOut}`** (optional): ระยะเวลาที่จะรอ element ปรากฏ (ค่าเริ่มต้นคือ `${GeneralTimeOut}`)

### Exampleq
```
mHomeSelectQuickMenu | ${QuickMenu} |
```

### Validate
ตรวจสอบการกดปุ่ม Quick Menu ตาม [Arguments] ที่ใส่เข้ามา จากนั้นกดเลือก Quick Menu

### Test Steps
1. เปิดหน้า Home
2. หาปุ่ม Quick Menu ที่จะกด
3. กดปุ่ม Quick Menu

<p align="center">
  <img src="https://github.com/user-attachments/assets/aac35b96-06f7-4567-a875-9ee025a1b41b" width="400">
</p>

---

## mHomeSelectNavigateBar

### Description
`mHomeSelectNavigateBar` ใช้สำหรับการเลือก Navigate Bar โดยรับ [Arguments] 2 ตัว ได้แก่:

- **`${MenuNavigateBar}`**: ชื่อเมนู ได้แก่
  - Home, Privileges, Package, Profile
- **`${TimeOut}`** (optional): ระยะเวลาที่จะรอ element ปรากฏ (ค่าเริ่มต้นคือ `${GeneralTimeOut}`)

### Example
```
mHomeSelectNavigateBar | ${MenuNavigateBar} |
```

### Validate
ตรวจสอบการกดปุ่ม Navigate Bar ตาม [Arguments] ที่ใส่เข้ามา จากนั้นกดเลือก Navigate Bar

### Test Steps
1. เปิดหน้า Main ของ Home, Profile, Privileges, Package
2. หาปุ่ม Navigate Bar ที่จะกด
3. กดปุ่ม Navigate Bar

---

### Additional Notes
- **Owner:** patipan.w@entronica.co.th
- รองรับภาษา EN / TH
- อนาคตจะใช้ CoreLang แต่ปัจจุบัน Net/Call ยังหาไม่เจอ ใช้วิธีดึง Variables ตรงไปก่อน (03/02/2025)
- มีการตรวจสอบและ Log Messages เมื่อไม่พบเมนูที่ต้องการเลือก
