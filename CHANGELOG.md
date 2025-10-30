# Change Log

All notable changes to the "rui-language-support" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [0.1.0] - 2025-10-30
**Added**
- Thêm F-String (String Interpolation) với cú pháp `f"Xin chào, ${name}!"`.
- Thêm cú pháp `when` (tương tự `elif`) cho câu lệnh `if`.
- Hỗ trợ Multi-line comments (bình luận nhiều dòng) với `;;* ... *;;`.

**Changed**
- Cập nhật `rui.tmLanguage.json` để tô sáng cú pháp cho các tính năng mới.
- Cập nhật `language-configuration.json` để hỗ trợ block comments (VS Code có thể dùng `Ctrl+/` để toggle comment).

## [0.0.3] - 2025-10-27
**Changed**
- Cập nhật cú pháp RUI để tạo điểm nhấn đặc biệt:
  + `async` đổi thành `spawn`
  + `await` đổi thành `defer`
  + `return` đổi thành `exit`
  + `null` đổi thành `empty`
- Cập nhật `rui.tmLanguage.json` và `README.md` để phản ánh các thay đổi từ khóa mới.

## [0.0.2] - 2025-10-26
**Added**
- Hỗ trợ tô sáng cú pháp cho các từ khóa bất đồng bộ mới: async và await.

- Cập nhật README.md với ví dụ về cú pháp async/await.

## [Unreleased]

- Initial release