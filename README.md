# Telecom_Custom_Churn
# 1.1 Mô tả tập dữ liệu
Tập dữ liệu lưu trữ thông tin về khách hàng của một công ty cung cấp các dịch vụ viễn thông. 
Tập dữ liệu bao gồm 7043 bản ghi, tương ứng 7043 khách hàng, mỗi khách hàng có 21 thuộc tính; chia thành 3 nhóm sau:

## A. Thông tin chung của khách hàng
  1. customerID: Mã khách hàng
  2. gender: Giới tính (male|female)
  3. SeniorCitizen: Giới hạn tuổi (0:trẻ - 1:già)
  4. Partner: Khách hàng có đối tác không (No|Yes)
  5. Dependents: Khách hàng có người phụ thuộc không (No|Yes)
  6. tenure: Số tháng khách hàng gắn bó với công ty (int)
## B. Thông tin các dịch vụ khách hàng đăng ký sử dụng  
  7. PhoneService: Khách hàng có sử dụng dịch vụ điện thoại không (Yes|No)
  8. MultipleLines: Khách hàng có sử dụng nhiều line điện thoại không (Yes|No|No phone)
  9. InternetService: Dịch vụ Internet của khách hàng (DSL, Fiber optic, No)
  10. OnlineSecurity: Khách hàng có sử dụng dịch vụ bảo mật online không (Yes|No|No Internet)
  11. OnlineBackup: Khách hàng có sử dụng dịch vụ dự phòng online không (Yes|No|No Internet)
  12. DeviceProtection: Khách hàng có sử dụng dịch vụ bảo vệ thiết bị không (Yes|No|No Internet)
  13. TechSupport: Khách hàng có sử dụng dịch vụ hỗ trợ kỹ thuật không (Yes|No|No Internet)
  14. StreamingTV: Khách hàng có sử dụng dịch vụ truyền hình trực tuyến không (Yes|No|No Internet)
  15. StreamingMovies:Khách hàng có sử dụng dịch vụ xem phim trực tiếp không (Yes|No|No Internet)
## C. Thông tin hợp đồng của khách hàng:
  16. Contract: thời hạn hợp đồng của khách hàng (Month-to-month|One year|two year)
  17. PaperlessBilling: khách hàng thanh toán có sử dụng hóa đơn giấy không (Yes|No)
  18. PaymentMethod: Phương thức thanh toán của khách hàng (Electronic check|Mailed check|Bank transfer|Credit card)
  19. MonthlyCharges: Số tiền mà khách hàng phải trả hàng tháng (int)
  20. TotalCharges: Tổng số tiền khách hàng phải trả
  21. Churn: Tình trạng khách hàng rời bỏ hay không (Yes|No)

# 1.2 Mô tả bài toán
  - Khách hàng rời bỏ (Customer churn) được định nghĩa là khách hàng hocawj người đanngư ký ngưng kinh doanh với một công ty hoặc dịch vụ
  - Khách hàng trong ngành viễn thông có thể lựa chọn từ nhiều nhà cung cấp dịch vụ khác nhau. và khách hàng có thể dễ dàng chuyển đổi từ nhà cung cấp này sang nhà cung cấp khác.
  - Trong thị trường cạnh tranh cao của ngành viễn thông tỷ lệ rời bỏ khách là một thước đo quan trọng. Việc giữ chân một khách hàng hiện tại sẽ ít tốn kém hơn nhiều so với việc thu hút khách hàng mới

# 1.3 Mục tiêu
  - Phân tích tập dữ liệu để thấy được chân dung khách hàng đăng ký sử dụng dịch vụ của công ty.
  - Tập trung vào nhóm khách hàng đã rời bỏ, xác định các yếu tố quan trọng ảnh hưởng tới việc rời bỏ của khách hàng.
  - Đưa ra các khuyến nghị để công ty xem xét, cải thiện các yếu tố giúp giữ chân khách hàng.
