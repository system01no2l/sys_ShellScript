# Overview
- Trong hệ điều hành Linux/Unix chmod là lệnh dùng để thay đổi quyền truy cập của người dùng vào file/folder.
# Syntax
```chmod [options] mode [mode] file1 file2 file3 ...```
+ options:
    + -R: Recursive, Áp dụng cho tất cả các file và folder bên trong
    + -f: force, set quyền tron trường hợp có lỗi
    + -v: verbose, hiển thị đối tượng đã xử lí
+ mode:

| #  | Permission  | rwx |
| -------------- | ------------- | ------------- |
| 7 | Read, Write, Excute | rwx  |
| 6 | Read, Write | rw-  |
| 5 | Read, Excute | r-x  |
| 4 | Read Only | r--  |
| 3 | Write, Excute | -wx  |
| 2 | Write Only | -w-  |
| 1 | Excute Only | --x  |
| 0 | None | ---  |

+ Example:
Với mode = 777 
    + Với file: -rwxrwxrwx
    + Với folder: drwxrwxrwx
    
 Từ bên phai sang thì kí tự:
 
 - ```-``` là đại diện cho file
 - ```d``` đại diện cho folder
 - 3 kí tự tiếp tương ứng với Read, Write, Excute của Owner (Người tạo folder/file)
 - 3 kí tự tiếp tương ứng với Read, Write, Excute của Owner Group (Group người tạo folder/file)
 - 3 kí t tiếp tương ứng với Read, Write, Excute của EveryOne (tất cả mọi người)

+ Check ```chmod```

    - Kiểm tra quyền: ```ls -l ~/path folder or path file```
    - Ví dụ quyền: 664 = -rw-r–r–
    - Phân quyền cho folder or file: ```chmod 664 ~/path folder or path file``` 
    - Phân cho cho các folder or file bên trong: ```chmod -R 664 ~/path folder or path file```
    - Để folder có thể mở được thì folder cần quyền thực thi, ta có thể thêm quyền thực thì bằng cách cộng mode x
      ```chmod +x ~/path folder```
    .Tương tự ta có thể +r, +w để thêm quyền đọc, ghi
