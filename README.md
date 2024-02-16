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
  19. MonthlyCharges
