[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23572393&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student ID:** AI20K-0346
**Student Email:** vuquangphuc55@gmail.com
**Name:** Vu Quang Phuc

---

## Mo ta

Day 10 lab nay xay dung mot ETL pipeline don gian de doc du lieu JSON, kiem tra chat luong du lieu, transform thong tin san pham, va luu ket qua ra CSV. Bai lam tap trung vao hai muc tieu chinh: xu ly du lieu dung quy tac va bo sung observability co ban de de dang theo doi so record hop le, so record bi loai, va thoi diem xu ly.
---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas pytest
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python generate_garbage.py
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

Pipeline doc 5 records tu `raw_data.json`, giu lai 3 records hop le va loai 2 records khong hop le do gia `<= 0` hoac `category` rong. File ket qua `processed_data.csv` chua them cot `discounted_price` va `processed_at`, giup pipeline vua dung business logic vua co dau vet de quan sat qua trinh xu ly du lieu.
