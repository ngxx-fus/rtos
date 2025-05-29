# AMBA
## Giới thiệu về AMBA

AMBA là viết tắt của Advanced Microcontroller Bus Architecture (Kiến trúc Bus cho Vi điều khiển Nâng cao). Đây là một bộ đặc tả giao thức do Arm định nghĩa. 
AMBA xác định một tiêu chuẩn truyền thông trên chip nhằm mục đích thiết kế vi điều khiển nhúng hiệu năng cao. 

AMBA cung cấp các giải pháp để kết nối và quản lý các khối chức năng tạo nên một Hệ thống trên chip (SoC). Các ứng dụng của AMBA bao gồm việc phát triển các hệ thống nhúng với một hoặc nhiều bộ xử lý (CPU) hoặc bộ xử lý tín hiệu và nhiều thiết bị ngoại vi.

Một trong những mục tiêu của đặc tả AMBA là để độc lập với công nghệ, đảm bảo các macrocell ngoại vi và hệ thống có thể được tái sử dụng cao và di chuyển trên nhiều quy trình công nghệ IC khác nhau. Đặc tả chỉ chi tiết giao thức bus ở cấp độ chu kỳ xung nhịp, không bao gồm các đặc tính điện.

Trong phiên bản Đặc tả AMBA (Rev 2.0), AMBA định nghĩa ba loại bus riêng biệt:

- Advanced High-performance Bus (AHB): AHB được thiết kế cho các module hệ thống hiệu năng cao, tần số xung nhịp cao
- Advanced System Bus (ASB): ASB là thế hệ đầu tiên của bus hệ thống AMBA, hỗ trợ hoạt động pipeline và nhiều master bus
- Advanced Peripheral Bus (APB): APB được tối ưu hóa cho tiêu thụ điện năng tối thiểu và giảm độ phức tạp giao diện. APB thường hoạt động như một bus thứ cấp cục bộ, được đóng gói như một thiết bị slave AHB hoặc ASB duy nhất.

## Một vi điều khiển điển hình dựa trên AMBA

Hình bên dưới mô tả cấu trúc hệ thống bus của một vi điều kiển điển hình dựa trên AMBA.

![AMBA MCU based](image.png)

Trong đó:

-   High-performance ARM processor: Bộ xử lý ARM hiệu năng cao, được kết nối trực tiếp với bus hệ thống hiệu năng cao 
-   High-bandwidth on-chip RAM: Bộ nhớ RAM tích hợp trên chip băng thông cao, là khối bộ nhớ nằm trên cùng một chip với bộ xử lý và các thành phần khác của hệ thống AMBA điển hình.
-   High-bandwidth External Memory Interface: Giao diện bộ nhớ ngoài băng thông cao, là một khối chức năng trong hệ thống AMBA được sử dụng để kết nối các thành phần trên chip với bộ nhớ vật lý nằm ngoài chip.
-   DMA (**D**irect **M**emory **A**ccess) bus master:

Bộ xử lý tốc độ cao, on-chip RAM, off-chip RAM, DMA bus master được kết nối sử dụng giao thức tốc độ cao AHB/ASB. Trong khi đó các ngoại vi được kết nối thông qua giao thức tốc độ thấp hơn và kết nối với bus tốc độ cao thông qua cầu AHBP2APB hoặc APB2AHB.
