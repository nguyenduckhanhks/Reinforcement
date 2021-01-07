#Câu1 :
#init: khởi tạo trạng thái: với mỗi lần lặp; nếu state đó là điểm cuối thì nhận phần thưởng và tiến hành thoát.
	Ngược lại thì iterationvalue tại state đó được tính bằng cách lấy giá trị lớn nhất của Qvalue ứng với các action tại state đó.
#Cách tính Qvalue: tính state tiếp theo và  xác suất chuyển đổi sang  trạng thái đó của state ứng với action.
    Với mỗi trạng thái và xác xuất chuyển sang trạng thái đó; giá trị qvalue được tính bằng reward khi chuyển sang trạng thái này cộng với giá trị discount của việc chuyển dịch trạng thái

#Cách chọn action: chọn action có qvalue lớn nhất

Câu 4:
#Hàm computeValueFromQValues: được tính bằng cách lấy giá trị qvalue lớn nhất ứng với các action trong state đó
#Hàm computeActionFromQValues: được tính bằng cách sử dụng hàm random.choice() với tham số là action có qvalue lớn nhất
#Hàm upadate: update lại qvalue.

Câu 5:
Nếu Giá trị flipCoin(self.epsilon) (Xác xuất của self.epsilon) trả về true thì action được lấy ngẫu nhiên bằng hàm random.choice nếu không ta vẫn lấy hành động tốt nhất như bình thường bằng hàm computeActionFromQValues

Câu 8:
Hàm getQvalue: tính theo công thức 
Q(s,a)=fi(s,a)wi
Hàm update weight tính theo công thức đề bài đã cho:

difference = (reward + self.discount*(qValueNextState))- qValueCurrentState
self.weights[k] =  self.weights[k] + self.alpha*(difference)*feature[k]
