# Flappy_Bird
# I-Hướng dẫn cài đặt.

- Game chạy bằng IDE Visual Studio (Tải tại đây https://visualstudio.microsoft.com/fr/)
- Download Zip. Giải nén.
- Chọn file FlappyBird.sln.
- Liên kết Project với thư viên SDL:
  +Ấn chuột phải vào project FlappyBird rồi chọn properties (Hoặc ấn tổ hợp alt+enter):
  
         . Vào mục VC++ Directories : 
                       Chọn Include Directories : add các đường link 
                             + $(SolutionDir)SDL2-2.0.8\include
                             + $(SolutionDir)SDL2_image-2.0.3\include
                             + $(SolutionDir)SDL2_mixer-2.0.2\include 
                             + $(SolutionDir)SDL2_ttf-2.0.14\include
                       Chọn Library Directories : add các đường link
                             + $(SolutionDir)SDL2_ttf-2.0.14\lib\x64
                             + $(SolutionDir)SDL2_image-2.0.3\lib\x64
                             + $(SolutionDir)SDL2_mixer-2.0.2\lib\x64
                             + $(SolutionDir)SDL2-2.0.8\lib\x64
                             
        . Vào mục Linker -> Input -> Additional Dependencies rồi add các file: SDL2.lib
                                                                               SDL2main.lib
                                                                               SDL2_image.lib
                                                                               SDL2_mixer.lib
                                                                               SDL2_ttf.lib 
        . Vào mục Settings trên window, search và chọn Edit environment variables for your account. Tại đây thêm vào path đường link đến thư mục Dll\x64
- Chạy code.

# II-Mô tả chung
- Thể loại: Phiêu lưu
- Quy tắc: Di chuyển chú chim qua khoảng trống giữa các cột được xếp ngẫu nhiên sao cho không chạm vào cột hoặc rơi xuống đất. Trò chơi chỉ kết thúc khi bạn vi phạm quy tắc trên.

# III-Mô tả các chức năng đã cài đặt

- Chú chim luôn có xu hướng rơi tự do.
- Sử dụng phím mũi tên hướng lên để di chuyển chú chim.
- Mỗi lần di chuyển qua 1 cột hệ thống sẽ ghi nhận của bạn 1 điểm.
- Xem mô tả chi tiết tại: https://youtu.be/7psZHRTi3k0

# IV-Các kĩ thuật lập trình được sử dụng
  <Game sử dụng ngôn ngữ lập trình C++>
  
+ Các kiểu, cấu trúc cơ bản:

                 . Cấu trúc rẽ nhánh
                 . Cấu trúc lặp
                 . Kiểu mảng
                 . Kiểu struct, class
                 . Kiểu con trỏ
                   ...
+ Các kĩ thuật xử lí đồ họa bằng thư viện SDL2:

                 . upload file ảnh
                 . Color key image (xóa phông cho đối tượng)
                 . Thêm âm thanh cho trò chơi
                 . Tạo các chuyển động cho đối tượng
                   ...
                   
# V-Hướng phát triển

  - Thêm phần điểm cao nhất sau mỗi lượt chơi
  - Tạo âm thanh xuyên suốt quá trình chơi
  - Cải thiện độ mượt mà của đối tượng khi di chuyển
  - Tăng độ khó cho game bằng cách tăng dần tốc độ di chuyển của chú chim mỗi khi tăng điểm số.
  
# VI-Kết luận

Do lần đầu trải nghiệm quy trình tạo ra một trò chơi đơn giản nên chắc hẳn sẽ không tránh khỏi những thiếu xót. 
Dù còn gặp nhiều khó khăn trong quá trình thực hiện nhưng sau cùng Flappy Bird cũng mang đầy đủ các chức năng cơ bản nhất mà một tựa game cần có.
Bản thân tự rút ra được rất nhiều kinh nghiệm quý báu: về quy trình làm game, cách xử lí tuần tự từng chức năng sao cho khoa học, tầm quan trọng của việc clean code...



                                                                             
