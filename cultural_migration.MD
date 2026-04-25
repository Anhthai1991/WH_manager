# ROLE

Bạn là:
- Senior Excel System Architect
- Warehouse Operations Consultant
- Management Control System Designer

Nhiệm vụ:
Thiết kế file Excel vận hành warehouse theo tư duy giống Notion/ERP mini.

Mục tiêu:
- quản lý công việc
- kiểm soát vận hành
- escalation rõ ràng
- tracking issue
- KPI visibility
- accountability
- quản trị bằng dữ liệu

QUAN TRỌNG:
Toàn bộ giao diện, sheet, cột, button, hướng dẫn phải dùng TIẾNG VIỆT hoàn toàn.

Người dùng:
- nhân viên warehouse
- supervisor
- manager
- kỹ năng Excel trung bình/yếu
- yếu tiếng Anh

File phải:
- cực dễ dùng
- trực quan
- ít thao tác
- không cần training nhiều

---

# BUSINESS CONTEXT

Environment:
- Warehouse operation
- Team có conflict nội bộ
- Có informal power structure
- Manager mới đang cải tổ hệ thống
- Chưa có ERP/Notion
- Hiện đang quản lý bằng Excel thủ công

Current Problems:
- Task giao miệng
- Không rõ owner
- Không tracking escalation
- Họp không có action rõ
- Không có incident log
- KPI không visible
- Khó kiểm soát delay
- Quá phụ thuộc con người

Goal:
Biến Excel thành:
- mini operating system
- command center cho manager
- source of truth cho operation

---

# FILE REQUIREMENTS

Tạo file Excel chuyên nghiệp gồm:

1. Dashboard Tổng Quan
2. Quản Lý Công Việc Hằng Ngày
3. Theo Dõi Sự Cố
4. Review Tuần
5. Quản Lý Nhân Sự
6. Theo Dõi KPI
7. Theo Dõi Cải Tiến
8. Escalation Tracking
9. Báo Cáo Quản Lý
10. Hướng Dẫn Sử Dụng

---

# IMPORTANT DESIGN PRINCIPLES

## 1. SIMPLE FIRST

Ưu tiên:
- dễ dùng
- tốc độ nhập liệu
- nhìn là hiểu

KHÔNG làm:
- dashboard quá fancy
- macro phức tạp
- nhiều popup
- giao diện rối

---

## 2. OPERATIONAL CONTROL

Mọi task phải có:
- người phụ trách
- deadline
- trạng thái
- mức ưu tiên

---

## 3. MANAGEMENT VISIBILITY

Manager mở file lên phải biết ngay:
- task nào trễ
- issue nào critical
- ai đang quá tải
- KPI đang tốt/xấu

Trong vòng 30 giây.

---

# SHEET 1 — DASHBOARD TỔNG QUAN

Tên sheet:
"DASHBOARD"

Thiết kế:
- hiện KPI chính
- task critical
- task overdue
- issue mở
- escalation
- OT
- productivity

Yêu cầu:
- dùng màu trực quan
- có biểu đồ đơn giản
- có filter nhanh

Sections:
1. KPI Hôm Nay
2. Công Việc Quá Hạn
3. Sự Cố Đang Mở
4. Escalation
5. Top Risk
6. Hiệu Suất Team

---

# SHEET 2 — QUẢN LÝ CÔNG VIỆC

Tên sheet:
"CONG_VIEC"

Required Columns:
- ID Công Việc
- Ngày
- Bộ Phận
- Nội Dung Công Việc
- Người Phụ Trách
- Mức Ưu Tiên
- Deadline
- Trạng Thái
- Đang Chờ Ai
- Nguyên Nhân Delay
- Hành Động
- Ghi Chú Manager

Dropdown:
- Priority
- Status
- Department

Status:
- Chưa Làm
- Đang Làm
- Blocked
- Hoàn Thành

Priority:
- Critical
- Cao
- Trung Bình
- Thấp

Yêu cầu:
- tự highlight overdue
- màu theo priority
- filter nhanh theo owner/status

---

# SHEET 3 — INCIDENT LOG

Tên sheet:
"SU_CO"

Purpose:
Track conflict, delay, process issue.

Required Columns:
- ID Sự Cố
- Ngày
- Người Liên Quan
- Loại Sự Cố
- Mô Tả Trung Tính
- Ảnh Hưởng
- Hành Động Ngay
- Người Theo Dõi
- Escalate Chưa
- Trạng Thái
- Evidence

Incident Types:
- Delay
- Conflict
- Inventory
- Safety
- Process Violation
- Communication

IMPORTANT:
Thiết kế phần hướng dẫn:
- mô tả phải trung tính
- không cảm xúc
- chỉ mô tả hành vi/sự kiện

---

# SHEET 4 — REVIEW TUẦN

Tên sheet:
"REVIEW_TUAN"

Required Sections:
1. KPI
2. Main Issues
3. Root Cause
4. Action Plan
5. Cost Impact
6. Risk

Required KPI:
- SLA
- Productivity
- OT
- Delay
- Accuracy
- Incident Count

---

# SHEET 5 — NHÂN SỰ

Tên sheet:
"NHAN_SU"

Required Columns:
- Tên
- Vai Trò
- Kỹ Năng
- Độ Tin Cậy
- Mức Ảnh Hưởng
- Khả Năng Hợp Tác
- Risk Level
- Điểm Mạnh
- Điểm Yếu
- Development Plan

Purpose:
Manager tracking only.

---

# SHEET 6 — KPI TRACKING

Tên sheet:
"KPI"

Track:
- Productivity
- OT
- Delay
- Inventory Accuracy
- Rework
- Incident Trend

Need:
- biểu đồ xu hướng
- so sánh tuần/tháng
- conditional formatting

---

# SHEET 7 — IMPROVEMENT

Tên sheet:
"CAI_TIEN"

Required Columns:
- Initiative
- Problem
- Current Impact
- Proposed Solution
- Owner
- Savings Potential
- Priority
- Status
- Deadline

Purpose:
Track operational improvement.

---

# SHEET 8 — ESCALATION

Tên sheet:
"ESCALATION"

Track:
- Escalation Level
- Issue
- Owner
- Trigger Date
- Escalated To
- Current Action
- Status
- Resolution

Levels:
- L1
- L2
- L3
- L4

---

# SHEET 9 — BAO CAO

Tên sheet:
"BAO_CAO"

Purpose:
Manager presentation.

Need:
- auto summary
- weekly snapshot
- monthly trend
- top issues
- cost impact

Format:
Executive style.

---

# SHEET 10 — HUONG_DAN

Tên sheet:
"HUONG_DAN"

Include:
- cách dùng file
- quy tắc update
- quy tắc escalation
- cách ghi incident
- quy định task management

IMPORTANT RULE:
"Không có trên hệ thống = chưa tồn tại"

---

# EXCEL FEATURES REQUIRED

Yêu cầu sử dụng:
- Conditional Formatting
- Dropdown Validation
- Pivot Table
- Simple Charts
- Freeze Pane
- Auto Filter
- Basic Formula

KHÔNG dùng:
- VBA quá phức tạp
- macro khó maintain
- script khó hiểu

---

# VISUAL DESIGN

Style:
- clean
- executive
- warehouse operation style

Color Logic:
- đỏ = critical/overdue
- vàng = warning
- xanh = completed/good

Font:
- dễ đọc
- chuyên nghiệp

---

# FINAL OBJECTIVE

File Excel phải khiến:
- manager có operational visibility
- team có accountability
- issue có traceability
- escalation rõ ràng
- conflict giảm cảm tính

Hệ thống phải giống:
- mini ERP
- warehouse command center

KHÔNG phải:
- file Excel ghi chú đơn giản.

---

# OUTPUT REQUIREMENT

Claude phải:
1. Thiết kế đầy đủ structure từng sheet
2. Tạo sample layout
3. Đề xuất công thức
4. Đề xuất conditional formatting
5. Đề xuất dropdown values
6. Thiết kế dashboard logic
7. Mô tả flow sử dụng
8. Tạo file theo chuẩn vận hành thực chiến

Toàn bộ bằng TIẾNG VIỆT.
