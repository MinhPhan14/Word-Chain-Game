WORD CHAIN GAME – README (TIẾNG VIỆT)
I. GIỚI THIỆU

Word Chain Game là trò chơi nối từ tiếng Anh với giao diện đồ họa (GUI), xây dựng bằng Python (PyQt5).

Tính năng:

Chơi 2 người
Nối từ theo chữ cái cuối
Tính điểm theo ván
Giới hạn thời gian mỗi lượt
Tra nghĩa từ (online + offline)
Hiển thị trạng thái mạng
II. YÊU CẦU HỆ THỐNG

Bản EXE:

Windows 10/11
Không cần cài Python

Bản CODE:

Python 3.8+
Cài thư viện:
pip install PyQt5

III. CÁCH CHẠY

Cách 1 (khuyên dùng):

Mở:
WordChainGame.exe

Cách 2:

Mở CMD
Chạy:
python english_word_chain.py

IV. TRẠNG THÁI MẠNG

🟢 Online:

Có internet
API hoạt động

🟡 API lỗi:

Có internet
Server từ điển lỗi (502, timeout...)

🔴 Offline:

Không có internet

Lưu ý:

Game vẫn chơi được offline
Nghĩa từ dùng dữ liệu có sẵn nếu không có mạng

V. LUẬT CHƠI

Từ mới phải bắt đầu bằng chữ cái cuối của từ trước
Không được lặp từ
Hết thời gian → mất lượt

VI. LỖI THƯỜNG GẶP

App không mở:
→ chạy bằng CMD để xem lỗi

Không có nghĩa:
→ mất mạng hoặc API lỗi

Hiện API lỗi:
→ server từ điển đang lỗi (không phải lỗi app)

VII. BUILD EXE (CHO DEV)

pip install pyinstaller

pyinstaller --onefile --windowed ^
-n WordChainGame ^
--add-data "english_words_50000.csv;." ^
--add-data "english_words_50000_meanings.json;." ^
english_word_chain.py

VIII. GHI CHÚ

File EXE ~50–100MB là bình thường
Không cần thêm file ngoài
Lần đầu chạy có thể chậm

Chúc bạn chơi game vui vẻ!

============================================================

WORD CHAIN GAME – README (ENGLISH)
I. INTRODUCTION

Word Chain Game is a GUI-based English word game built with Python (PyQt5).

Features:

2-player local gameplay
Word chaining by last letter
Score tracking
Turn time limit
Word meaning lookup (online + offline)
Network status indicator
II. SYSTEM REQUIREMENTS

EXE version:

Windows 10/11
No Python required

Source version:

Python 3.8+
Install dependency:
pip install PyQt5

III. HOW TO RUN

Option 1 (recommended):

Open:
WordChainGame.exe

Option 2:

Open CMD
Run:
python english_word_chain.py

IV. NETWORK STATUS

🟢 Online:

Internet available
API working

🟡 API Error:

Internet available
Dictionary API failed (502, timeout, etc.)

🔴 Offline:

No internet connection

Note:

Game still works offline
Meanings will use local data if no internet

V. GAME RULES

Each word must start with the last letter of the previous word
No repeated words
Timeout → lose turn

VI. COMMON ISSUES

App won’t open:
→ run via CMD to see error

No word meanings:
→ no internet or API error

API error shown:
→ server issue, not app issue

VII. BUILD EXE (FOR DEVELOPERS)

pip install pyinstaller

pyinstaller --onefile --windowed ^
-n WordChainGame ^
--add-data "english_words_50000.csv;." ^
--add-data "english_words_50000_meanings.json;." ^
english_word_chain.py

VIII. NOTES

EXE size (~50–100MB) is normal (PyQt5)
No extra files required
First launch may be slower

Enjoy the game!