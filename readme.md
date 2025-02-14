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

