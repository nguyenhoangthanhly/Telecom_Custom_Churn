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
![Gender](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/cd5b8469-e91a-4de4-bb49-d7c80794ea4e) 
![Tron_Gender](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/6ef04470-8b0c-4b30-8341-13026b007956)
![SeniorCitizen](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/8481ea7b-042c-414f-ba97-c238b2c89f8b)
![Tron_SeniorCitizen](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/b5a22b75-ae10-4099-8d8b-4d8663bf4529)
![Dependents](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/4beacda1-68a9-4622-9af6-feda15eb79c5)
![Tron_Dependents](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/1d59f8cf-addf-4f80-8ad6-7641900ba593)
![Contract](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/bcff6386-ace7-446b-9d20-216f4a953273)
![Tron_Contract](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/98dac770-1837-410d-965e-b5fd231e9483)
![PaymentMethod](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/fe95ceb3-fa5c-46d6-9a3f-377cf6a89aaf)
![Tron_PaymentMethod](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/72e5f7dd-0dee-4d7a-ad11-ed8017e78f84)
![Phone Service](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/86cffb7d-72fc-482d-ad93-b65adbed407a)
![Tron_Phone Service](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/50ea1a0b-8f49-473a-9b6f-865b18081533)
![Multiple Lines](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/ab8ab432-b039-4466-9d7d-2d60014a4cfe)
![Tron_Multiple Lines](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/3f1e2f2d-a5d6-456a-8d5c-ffef1a049667)
![Internet Service](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/3c93a46d-7e94-4b4c-8120-c4a5086e8399)
![Tron_Internet Service](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/0553e75c-eda4-46b5-965c-bcb124e920c5)
![Online Security](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/2eb3a0de-fdf6-4873-8afa-5253199f3492)
![Tron_Online Security](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/46d4b437-acf0-4e5a-8d83-bda4db037dfe)
![Online Backup](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/2febc1c3-cbeb-4540-9389-81f94e2ee1d7)
![Tron_Online Backup](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/f07297e6-a1da-49d5-9356-798c2d080426)
![Device Protection Plan](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/479d2507-5258-4480-8554-6abb1236096d)
![Tron_Device Protection Plan](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/da98d3cc-9082-4906-820e-544979a30633)
![Premium Tech Support](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/9a93e26d-1234-41b8-970d-b91462c93e36)
![Tron_Premium Tech Support](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/ae82911a-c018-4396-99c5-339c5d8fc6b6)
![Streaming TV](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/9f033047-7a7d-4382-9471-d991ae7a3bc8)
![Tron_Streaming TV](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/3c492fad-0506-4639-a1f3-f1adbc67c29b)
![Streaming Music](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/b0d314e6-3cdf-485f-92f4-aed1955f7616)
![Tron_Streaming Music](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/99ec6316-9451-4385-8120-8d4984da3a96)
![Streaming Movies](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/16dfdc95-1055-46cb-9d21-a5a38d2bc126)
![Tron_Streaming Movies](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/2263f255-c616-4607-9a22-92e1f875353e)
# 2.2 Tỷ lệ khách hàng rời bỏ
  - Customer Churn Rate là một trong những chỉ số quan trọng đối với doanh nghiệp. Chỉ số này phản ánh chất lượng sản phẩm, dịch vụ trong mắt người tiêu dùng và thái độ của người tiêu dùng đối với sản phẩm, dịch vụ mà doanh nghiệp cung cấp.
![Customer Status](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/6a49e2a4-a0ad-4566-88b8-f499601a0f5c)
![Tron_Customer Status](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/37bc5972-9639-43e1-8122-6c634b497e9e)

## 2.2.1 Tỷ lệ khách hàng rời bỏ
![countplot_Gender](https://github.com/nguyenhoangthanhly/Telecom_Custom_Churn/assets/117055865/cc58bcdc-3201-4f3e-ba8d-8050ca3620b0)

# 3. Kết Luận
  - Tỷ lệ khách hàng rời bỏ công ty đang ở mức 26.5% đang ở mức khá cao ==> Cần đẩy mạnh các chiến lược để giữ chân khách hàng
  - Một số kiến nghị nên xem xét khi đưa ra chính sách, cải thiện dịch vụ hiện có để giữ chân khách hàng
      + Xem xét các dịch vụ, chính sách với nhóm khách hàng trung niên. Nhóm khách hàng trung niên của công ty chiếm tới 55% (3874/7043 khách hàng) nhưng có hơn 933 khách hàng rời bỏ chiếm tới gần 25%
      + Kiểm tra lại dịch vụ Internet cáp quang đang cung cấp, có hơn 3035/7043 khách hàng sử dụng Fiber Optic chiếm 43.09%. Trong đó, có 1236/3035 khách hàng đang sử dụng Fiber Optic lại chọn rời bỏ chiếm tới 40.7%
      + Có các chính sách phù hợp với khách hàng có hợp đồng Month-to-Month, marketing, khuyến mãi để chuyển sang hợp đồng lâu dài. Vì tỷ lệ khách hàng rời bỏ khi sử dụng hợp đồng Month-to-Month chiếm tới 45.84% trong 3610 khách hàng sử dụng Month-to-Month.
      + Rà soát cải thiện phương thức thanh toán "Bank Withdrawal" có đang gây khó khăn, bất tiện gì cho khách hàng hay không. Tỷ lệ khách hàng rời bỏ khi sử dụng phương thức thanh toán "Bank Withdrawal" chiếm tới 33.99%.
