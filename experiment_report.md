# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-0346
**Name:** Vu Quang Phuc
**Date:** 2026-04-15

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | `Agent: Based on my data, the best choice is Laptop at $1200.` | 9 | Ket qua hop ly vi du lieu co cau truc dung, category dong nhat, va khong co record gay nhieu. |
| Garbage Data (`garbage_data.csv`) | `Agent: Based on my data, the best choice is Nuclear Reactor at $999999.` | 2 | Ket qua sai nghiem trong do du lieu co outlier, duplicate ID, sai kieu du lieu, va gia tri null. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Agent trong bai nay khong "hieu" du lieu theo cach con nguoi hieu, ma no dua vao bang du lieu de tim record phu hop nhat theo logic don gian. Khi dung clean data, bang da duoc loc bo cac loi co ban nen thao tac tim san pham electronics gia cao nhat tra ve Laptop, mot ket qua hop ly. Khi dung garbage data, agent khong co lop phong ve nao de nhan ra rang record `Nuclear Reactor` voi gia `999999` la mot outlier phi thuc te. Ngoai ra, duplicate ID lam giam do tin cay cua du lieu, wrong data type nhu `ten dollars` co the gay loi hoac lam sai phep tinh, con null values lam mat ngu canh cho category va price. Dieu quan trong la mo hinh hoac agent co prompt tot den dau cung se dua ra ket qua kem neu nguon du lieu dau vao bi ban. Quan sat nay cho thay data validation va observability phai xuat hien truoc ca cac buoc suy luan AI.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

Dong y. Prompt tot giup agent dien dat ro rang hon, nhung neu du lieu dau vao sai, prompt van chi dan den cau tra loi sai mot cach tu tin. Du lieu chat luong cao la nen tang de agent truy xuat, suy luan, va tra loi dung hon.
