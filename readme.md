# Realtime operating system
## About RTOS

Về cơ bản OS cũng là một phần mềm. Một số hệ điều hành lớn (GPOS) khi đó nguwoif dùng không cần phải quan tâm đến HW. 
```text
    APP
    ---
    GPOS
    ---
    HW(GPOS)
```
Với các tác vụ đơn giản:
```
    SW
    ---
    HW
```
Các tác vụ phức tạp hơn:
```
    SW <-> OS (aka RTOS/Embedded OS)
    ---------
    HW
```
VD bên trong USB:
```
    |flash|MCU| <-> (USB prototype)
```
Bên trong MCU có chứa hệ điều hành.


**Summary**:

Chương trình đơn nhiệm (như MCU thông thường) khác với đa tác vụ khi dùng OS.

Note: 1x Word = 4bytes (depend on ISA).

Liên quan tới OS:
-   CPU: Tốc độ chạy
-   Flash: Chứa code, OS
-   RAM: Cấp bộ nhớ cho các task
-   

| OS    | HW                    | E.g                                   |
| :--:  | :--:                  | :--:                                  |
| nope  | Nhỏ(mem)/Yếu(speed)   | 2KByte RAM, 16MHz, 32KByte Flash      |
| RTOS  | Lớn vừa/Mạnh vừa      | ESP32 (VĐK) - dualcore <br> (240MHz, 520KByte, 4MByte(spi)) |
