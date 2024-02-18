# Telecom_Custom_Churn
# 1.1 Mô tả tập dữ liệu
Tập dữ liệu lưu trữ thông tin về khách hàng của một công ty cung cấp các dịch vụ viễn thông. 
Tập dữ liệu bao gồm 7043 bản ghi, tương ứng 7043 khách hàng, mỗi khách hàng có 37 thuộc tính; chia thành 3 nhóm sau:

## A. Thông tin chung của khách hàng
  1. customerID: Mã khách hàng
  2. gender: Giới tính (male|female)
  3. age: Tuổi của khách hàng (int)
  4. Married: Trạng thái hôn nhân của khách hàng (Yes|No)
  5. Number of Dependents: Số lượng người phụ thuộc vào khách hàng (int)
  6. City: Thành phố nơi khách hàng dang sinh sống
  7. Latitude: Vĩ độ
  8. Longtitude: Kinh độ
  9. Number of Referrals: Số lượng người đucợ khách hàng giới thiệu đến dịch vụ
## B. Thông tin các dịch vụ khách hàng đăng ký sử dụng  
 10. Tenure in Months: Số tháng mà khách hàng đã sử dụng dịch vụ
 11. Offer: Các ưu đãi đucợ cung cấp cho khách hàng.
  12. PhoneService: Khách hàng có sử dụng dịch vụ điện thoại không (Yes|No)
  13. MultipleLines: Khách hàng có sử dụng nhiều line điện thoại không (Yes|No|No phone)
  14. InternetService: Dịch vụ Internet của khách hàng (DSL, Fiber optic, No)
  15. OnlineSecurity: Khách hàng có sử dụng dịch vụ bảo mật online không (Yes|No|No Internet)
  16. OnlineBackup: Khách hàng có sử dụng dịch vụ dự phòng online không (Yes|No|No Internet)
  17. DeviceProtection: Khách hàng có sử dụng dịch vụ bảo vệ thiết bị không (Yes|No|No Internet)
  18. TechSupport: Khách hàng có sử dụng dịch vụ hỗ trợ kỹ thuật không (Yes|No|No Internet)
  19. StreamingTV: Khách hàng có sử dụng dịch vụ truyền hình trực tuyến không (Yes|No|No Internet)
  20. StreamingMovies:Khách hàng có sử dụng dịch vụ xem phim trực tiếp không (Yes|No|No Internet)
## C. Thông tin hợp đồng của khách hàng:
  21. Contract: thời hạn hợp đồng của khách hàng (Month-to-month|One year|two year)
  22. PaperlessBilling: khách hàng thanh toán có sử dụng hóa đơn giấy không (Yes|No)
  23. PaymentMethod: Phương thức thanh toán của khách hàng (Electronic check|Mailed check|Bank transfer|Credit card)
  24. MonthlyCharges: Số tiền mà khách hàng phải trả hàng tháng (int)
  25. TotalCharges: Tổng số tiền khách hàng phải trả
  26. Total Refunds (Tổng số tiền hoàn lại): Tổng số tiền mà khách hàng đã nhận được từ các khoản hoàn tiền hoặc giảm giá.
  27. Total Extra Data Charges (Tổng phí dữ liệu phụ): Tổng số tiền mà khách hàng phải trả cho dữ liệu phụ vượt quá hạn mức được quy định trong gói cước của họ.
  28. Total Long Distance Charges (Tổng phí cuộc gọi xa): Tổng số tiền mà khách hàng đã trả cho các cuộc gọi xa, tính trong một khoảng thời gian nhất định.
  29. Total Revenue (Tổng doanh thu): Tổng doanh thu mà công ty thu được từ khách hàng, bao gồm tất cả các khoản thanh toán từ khách hàng cũng như các khoản phí bổ sung.
  30. Customer Status (Trạng thái khách hàng): Trạng thái hiện tại của khách hàng trong hệ thống (ví dụ: active, inactive, pending, v.v.).
  31. Churn Category (Phân loại Churn): Phân loại lý do hoặc loại churn của khách hàng nếu họ đã rời bỏ dịch vụ (ví dụ: voluntary, involuntary).
  32. Churn Reason (Lý do Churn): Lý do cụ thể mà khách hàng đã rời bỏ dịch vụ (nếu có). Điều này có thể bao gồm các lý do như cạnh tranh, chất lượng dịch vụ, giá cả, v.v.

# 1.2 Mô tả bài toán
  - Khách hàng rời bỏ (Customer churn) được định nghĩa là khách hàng hoặc người đăng ký ngưng kinh doanh với một công ty hoặc dịch vụ
  - Khách hàng trong ngành viễn thông có thể lựa chọn từ nhiều nhà cung cấp dịch vụ khác nhau. và khách hàng có thể dễ dàng chuyển đổi từ nhà cung cấp này sang nhà cung cấp khác.
  - Trong thị trường cạnh tranh cao của ngành viễn thông tỷ lệ rời bỏ khách là một thước đo quan trọng. Việc giữ chân một khách hàng hiện tại sẽ ít tốn kém hơn nhiều so với việc thu hút khách hàng mới

# 1.3 Mục tiêu
  - Phân tích tập dữ liệu để thấy được chân dung khách hàng đăng ký sử dụng dịch vụ của công ty.
  - Tập trung vào nhóm khách hàng đã rời bỏ, xác định các yếu tố quan trọng ảnh hưởng tới việc rời bỏ của khách hàng.
  - Đưa ra các khuyến nghị để công ty xem xét, cải thiện các yếu tố giúp giữ chân khách hàng.

# 2.1 Chân dung khách hàng
![Gender](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/cd5b8469-e91a-4de4-bb49-d7c80794ea4e) ![Tron_Gender](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/6ef04470-8b0c-4b30-8341-13026b007956)


# 2.2 Tỷ lệ khách hàng rời bỏ
  - Customer Churn Rate là một trong những chỉ số quan trọng đối với doanh nghiệp. Chỉ số này phản ánh chất lượng sản phẩm, dịch vụ trong mắt người tiêu dùng và thái độ của người tiêu dùng đối với sản phẩm, dịch vụ mà doanh nghiệp cung cấp.
## 2.2.1 Tỷ lệ khách hàng rời bỏ theo giới tính
