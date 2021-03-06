# Project-3 - Robocar tracking line.
Robocar is following black line
# Mô tả 
Thực hiện được những yêu cầu sau:  
- Xe chạy đúng theo đường vạch kẻ  
- Tăng tốc độ của xe mà không bị văng khỏi đường đi  
- Dừng lại khi có vật cản. 

# Linh kiện sử dụng
 - Vi điều khiển Pic16f877a
 - Cảm biến thu-phát hồng ngoại (5 cặp led )
 - Module Cảm biến HC-SR04
 - Module điều khiển động cơ DC L298.
 - Động cơ dc 12v x2
 
# Nguyên lý hoạt động:   
Robocar dò đường sẽ di chuyển theo vạch màu(đen – trắng) nhờ các cảm biến hồng ngoại phát hiện vật cản. 
Dựa vào nguyên lý phạn xạ của tia hồng ngoại do led phát(IR transmitter) phát ra, 
nếu gặp vật  cản sẽ phản xạ lại và được led thu(IR Receiver) thu lại. 
Khi ko có vật cản thì led thu(IR Receiver) sẽ không nhận được tia phản xạ từ led phát(IR Transmitter).
Dùng bề mặt trắng để có thể phản xạ lại tia hồng ngoại do led phát phát ra.
Khi đó led thu sẽ nhận được tia từ led phát nhờ phản xạ lên bề mặt màu trắng. Dùng bề mặt đen để hấp thụ tia được phát ra giống như không có vật cản.  
![Khi không có vạch](https://hackster.imgix.net/uploads/attachments/496036/Concept-of-White-Line-Follo.gif?auto=compress&gifq=35&w=1280&h=960&fit=max)  
Khi không có vạch thì IR nhận sẽ nhận được tín hiệu từ IR phát  
![Khi có vạch](https://hackster.imgix.net/uploads/attachments/496035/Concept-of-Black-Line-Follo.gif?auto=compress&gifq=35&w=1280&h=960&fit=max)  
Khi có vạch IR nhận không nhận được tín hiệu từ IR phát  
  
Xe có thể dừng lại khi gặp vật cản: 
- khi đến khoảng cách nhất định, cảm biến SR04 sẽ do được, so sánh với khoảng cách cài sẵn trong chương trình. Khi đó xe sẽ dừng lại
- Khi ko có vật sẽ tiếp tục đi.     
  
![Khi có vật cản](https://user-images.githubusercontent.com/67089995/176749051-c77ae928-1c6e-4f36-8578-f7765234b133.jpg)

# Demo

Click vào link để xem demo - >> https://youtu.be/d63bywc6ar8  

[![Watch the video](https://user-images.githubusercontent.com/67089995/176743694-0d32e567-f0b3-44de-84c1-7b63ee6d9949.png)](https://youtu.be/d63bywc6ar8)
