# Teaser RUI Language Syntax Highlight

Extension VSCode cung cấp tính năng tô sáng cú pháp (Syntax Highlighting) cơ bản cho **RUI (Teaser RUI Language)**, một ngôn ngữ scripting custom được tạo ra như một dự án vui vẻ cá nhân.
> Lưu ý: Teaser RUI không dành cho mục đích nghiêm túc (hay **production**).


RUI được thiết kế để đơn giản và hiệu quả, phù hợp với các tác vụ scripting và logic tự động hóa nhẹ.

## 🚀 Tính năng

- Extension này hiện chỉ tập trung vào việc tô sáng chính xác các thành phần cơ bản của ngôn ngữ RUI:

- **Từ khóa Điều khiển:** `if`, `else`, `for`, `while`, `break`, `continue`, `try`, `catch`, `finally`, `exit`.

- **Lập trình Bất đồng bộ (MỚI):** `spawn` (thay cho `async`, khai báo hàm bất đồng bộ) và `defer` (thay cho `await`, chờ Promise).

- **Khai báo:** `fn` (Function), `class` (Class Definition).

- **Giá trị Ngôn ngữ:** `true`, `false`, `empty` (thay cho `null`), `this`.

- **I/O:** `say` (in ra console), `get` (tải module) và `in` (thay cho `from`).

- **Toán tử:** Hỗ trợ đầy đủ các toán tử gán (`+=`, `*=`...), so sánh, logic và bitwise.

- ****Bình luận:** Bình luận bắt đầu bằng `;;`.

## ⚙️ Cài đặt (Manual Installation)

Vì đây là một extension custom (và có thể không được publish lên VSCode Marketplace):

1. **Đóng gói:** Sử dụng công cụ vsce (Visual Studio Code Extension Manager) để đóng gói dự án của bạn:
```
npm install -g vsce
vsce package
```

2. **Cài đặt:** Mở VS Code, đi tới tab Extensions (Ctrl+Shift+X). Chọn menu `...` (More Actions) và chọn **Install from VSIX....**

3. Chọn file `.vsix` vừa được tạo.

## 📝 Cách sử dụng

Sau khi cài đặt, bất kỳ tệp nào có phần mở rộng là `.rui` sẽ tự động được áp dụng tính năng tô sáng cú pháp RUI.

**Ví dụ:**
```rui
;; Khởi tạo biến và định nghĩa class
fn main() {
    say("Welcome to RUI!")
    
    class MyAI {
        ;; Hàm khởi tạo (constructor) - PHẢI CÓ 'fn'
        fn init(name) {
            this.name = name
        }

        ;; Phương thức của class - PHẢI CÓ 'fn'
        fn run_check() {
            if (this.name == "Emmiery") {
                exit true
            }
            exit false
        }
    }

    ;; Khai báo biến (chỉ cần gán)
    bot = MyAI("Emmiery")
    
    if (bot.run_check()) {
        say("RUI bot is active!")
    } else {
        say("Check failed.")
    }
}

;; Chạy hàm main
main()
```

## 💖 Tác giả

Được tạo ra bởi **Teaserverse**

**Dự án Lõi:** Teaser RUI Language