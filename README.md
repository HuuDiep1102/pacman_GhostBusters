Câu 1 
Cập nhật method observe trong ExactInference class của file inference.py 
triển khai cập nhật niềm tin cho Pacman dựa trên quan sát của pacman
// xác định các vị trí đầu tiên chúng ta sẽ kiểm tra xem có con ma nào bị bắt chưa noisyDistance
ngược lại thì chúng ta sử dụng 1 vòng for đi qua legalPositions ( tất cả các vị trí có thể có ma) 
sử dụng khoảng cachs mahatan để tính kcach giua pacman và các vị trí đó và sau mỗi lần bắt dk ma sẽ cập nhật lại niềm tin 

Câu 2: 
elapseTime trong  trong ExactInference class của file inference.py 
triển khai cập nhật niềm tin cho Pacman dựa trên kiến thức về di chuyênr của pacman là ma ko đi xuyên qua được tường và nhiều khoảng trống trong 1 bước thời gian
chúng ta sử dụng 1 vòng for đi qua legalPositions ( tất cả các vị trí có thể có ma) 
newPostDist ứng với mỗi p trong vòng lặp thể hiện vị trí mới của ma sau đó cập nhật lại niềm tin 

Câu 3 
Implement the chooseAction method in GreedyBustersAgent in bustersAgents.py
Đầu tiên tính toán vị trí có khả năng xảy ra nhất của mỗi con ma có chưa được nắm bắt, sau đó chọn một hành động mang lại Pacman gần bóng ma nhất
livingGhostPositionDistributions  là danh sách các niềm tin vị trí phân phối cho từng bóng ma vẫn còn sống.
gameState.getLivingGhosts (), danh sách các boolean, mỗi boolean một tác nhân, cho biết tác nhân còn sống hay không. Ghi chú pacman luôn là tác nhân 0, vì vậy các bóng ma là tác nhân 1, trở đi (giống như trước đây).
self.ghostBeliefs, danh sách các bản phân phối niềm tin cho mỗi của những hồn ma 

Câu 4:
Thực hiện các chức năng initializeUniformly, getBeliefDistribution và observe cho các ParticleFilterlớp trong inference.py.
Đầu tiên trong initializeUniformly sẽ khởi tạo danh sachs các hạt
Tiếp theo ở  observe cập nhật niềm tin quan sát khoảng cách đã cho nếu các hạt có trọng lượng bằng 0 thì sẽ lấy lại các hạt
khi pacman bắt dk ma thì các hạt sẽ được cập nhật để cho ma vào phòng giam 

Câu 5: 
Implement the elapseTime function for the ParticleFilter class in inference.py
sử dụng vòng lặp để lất ra vị trí của tất cả ma rồi lấy mẫu 1 số vị trí cho hạt
