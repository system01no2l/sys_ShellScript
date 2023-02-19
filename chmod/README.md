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
