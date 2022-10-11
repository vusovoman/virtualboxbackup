Bạn đang tìm cách gắn ổ cứng vật lý vào máy ảo VirtualBox?

Có một số điều bạn cần biết.

Trong màn hình Quản lý đĩa trong Windows, đặt đĩa thành 'ngoại tuyến' và ghi lại số đĩa, ví dụ: Đĩa # 2.

Trong dấu nhắc lệnh, được mở với tư cách quản trị viên, cd vào thư mục chương trình VirtualBox và chạy:

VBoxManage internalcommands createrawvmdk -filename "C:\temp\rawdiskaccessdisk2.vmdk" -rawdisk \\.\PhysicalDrive2

Thay thế số đĩa và đường dẫn nếu cần.

Sau đó đính kèm tệp VMDK vào VirtualBox VM. Để có khả năng tương thích tốt nhất, bạn có thể muốn sử dụng bộ điều khiển IDE.

Quan trọng: chạy chính VirtualBox với tư cách quản trị viên, bằng cách nhấp chuột phải và chọn 'chạy với tư cách quản trị viên'. Nếu không, bạn sẽ nhận được lỗi 'truy cập bị từ chối'.

Nhân tiện, phương thức tương tự cũng hoạt động trên VMware Workstation, nhưng bạn không cần phải chạy VMware với tư cách quản trị viên [Oracle VirtualBox backup](http://www.virtualboxbackup.ovh/).
