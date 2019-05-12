# Bài tập nhóm 9 - Xây dựng mô hình uml cho phần mềm dự toán công trình

## Cấu trúc file nộp
  - Tạo thư mục tên là N9
  - Trong thư mục N9 gồm 2 dạng file
  - File word mô tả use case.(Datta_mssv.docx)
  - File mdl mô hình của hệ thống (rationalrose.mdl)
  - Gmail pttdhct@gmail.com
  - Sdt 0919063379

## Mô tả bài toán bằng lời
  1. Bóc tách công việc từ bảng thiết kế
  2. Định mức công việc phù hợp với bảng thiết kế
  3. Lập danh mục công việc
  4. Lập đơn giá công việc

## Liệt kê các chức năng của phần mềm (UC)
  1. Xác định actor
    - Người dự toán
  2. Xác định UC
    - Đăng nhập
    - Cập nhật công trình
    - Cập nhật : nhân công, vật liệu, máy thi công
    - Cập nhật giá nhân công, vật liệu, máy thi công
    - Cập nhật hệ số chi phí trực tiếp khác, chi phí chung, chi phí thu nhập chịu thuế tính trước, thuế VAT
    - Tính tổng chi phí công trình

  3. Xây dựng UC diagram


  4. Đặt tả UC
    - Đăng nhập
      * Tóm tắt định danh
        + Tiêu đề: Đăng nhập hệ thống Dự toán công trình
        + Tóm tắt: use case này yêu cầu người dùng đăng nhập thì mới có thể sử dụng hệ thống
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái chưa đăng nhập
        + Kịch bản thường
          1. Người dùng đăng nhập vào hệ thống
          2. Hệ thống kiểm tra tài khoản
          3. Hiển thị giao diện chính của hệ thống
        + Kịch bản thay thế
          - A1 - Tài khoản không hợp lệ
          <br> chuỗi A1 bắt đầu từ bước 2 của kịch bản thường
            3. Hệ thống thông báo tài khoản không đúng
            Trở về bước 1 của kịch bản thường

    -Cập nhật công trình
    * Tóm tắt định danh
      + Tiêu đề: Cập nhật công trình.
      + Tóm tắt: use case này cho phép người dùng tạo mới công trình hoặc chỉnh sửa, xóa những công trình đã có.
      + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
      + Ngày tạo :20/4/2019
      + Ngày cập nhật :12/05/2019
      + Version :1.0
      + Chịu trách nhiệm: Võ Thanh Hiền
    * Mô tả scenario
      + Điều kiện tiên quyết
        - Hệ thống đang trong trạng thái đã đăng nhập thành công
      + Kịch bản thường
        1. Người dùng chọn tạo mới
        2. Hệ thống hiển thị form yêu cầu thông tin công trình mới
        3. Người dùng nhập thông tin công trình mới
        4. Người dùng chọn lưu công trình mới
        5. Hệ thống kiểm tra hợp lệ dữ liệu
        6. Hệ thống insert thông tin vào cơ sở dữ liệu
        7. Hệ thống thông báo đã lưu công trình
      + Kịch bản thay thế
        - A1 - Chỉnh sửa công trình
        <br> chuỗi A1 bắt đầu từ bước 0 của kịch bản thường
          1. Người dùng chọn mở công trình
          2. Hệ thống yêu cầu chọn công trình
          3. Người dùng chọn công trình cần chỉnh sửa
          4. Hệ thống hiển thị form thông tin công trình đã chọn
          5. Người dùng chỉnh sửa công trình
          6. Người dùng chọn lưu công trình
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống update thông tin vào cơ sở dữ liệu
          8. Hệ thống thông báo đã cập nhật thành công
        - A2 - Xóa công trình
        <br> chuỗi A2 bắt đầu từ bước 4 của kịch bản A1
          5. Người dùng chọn xóa công trình
          6. Hệ thống xóa công trình đã chọn khỏi cơ sở dữ liệu
          7. Hệ thống thông báo đã xóa công trình
      + Kịch bản lỗi
        - E1 - Dữ liệu không hợp lệ
          Chuỗi E1 bắt đầu từ bước 5 của kịch bảng thường
          6. Hệ thống thông báo dữ liệu không hợp lệ
          Trở về bước 3 của kịch bản thường
    - Cập nhật : nhân công
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật nhân công
        + Tóm tắt: use case này cho phép người dùng thêm, chỉnh sửa hoặc xóa nhân công trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab nhân công
          2. Hệ thống hiển thị bảng nhân công trong cơ sở dữ liệu
          3. Người dùng chọn thêm nhân công
          4. Hệ thống hiển thị form yêu cầu nhập thông tin nhân công mới
          5. Người dùng nhập thông tin nhân công mới
          6. Người dùng chọn lưu
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống insert thông tin vào cơ sở dữ liệu
          9. Hệ thống thông báo đã lưu thành công
        + Kịch bản thay thế
          - A1 - Chỉnh sửa nhân công
          <br> chuỗi A1 bắt đầu từ bước 2 của kịch bản thường
          3. Người dùng chọn một nhân công cần chỉnh trong bảng nhân công
          4. Người dụng chọn sửa nhân công
          5. Hệ thống hiển thị form các thông tin của nhân công được chọn
          5. Người chỉnh sửa thông tin nhân công
          6. Người dùng chọn lưu
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống update thông tin vào cơ sở dữ liệu
          9. Hệ thống thông báo đã chỉnh sửa thành công
          - A2 - Xóa nhân công
          <br> chuỗi A2 bắt đầu từ bước 3 của kịch bản A1
            5. Người dùng chọn xóa nhân công
            6. Hệ thống delete nhân công đã chọn khỏi cơ sở dữ liệu
            7. Hệ thống thông báo đã xóa thành công
        + Kịch bản lỗi
          - E1 - Dữ liệu không hợp lệ
            Chuỗi E1 bắt đầu từ bước 7 của kịch bảng thường
            6. Hệ thống thông báo dữ liệu không hợp lệ
            Trở về bước 5 của kịch bản thường
    - Cập nhật máy thi công
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật máy thi công
        + Tóm tắt: use case này cho phép người dùng thêm, chỉnh sửa hoặc xóa máy thi trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab máy thi công
          2. Hệ thống hiển thị bảng máy thi công trong cơ sở dữ liệu
          3. Người dùng chọn thêm máy thi công
          4. Hệ thống hiển thị form yêu cầu nhập thông tin máy thi công mới
          5. Người dùng nhập thông tin máy thi công mới
          6. Người dùng chọn lưu
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống insert thông tin vào cơ sở dữ liệu
          9. Hệ thống thông báo đã lưu thành công
        + Kịch bản thay thế
          - A1 - Chỉnh sửa máy thi công
          <br> chuỗi A1 bắt đầu từ bước 2 của kịch bản thường
          3. Người dùng chọn một máy thi công cần chỉnh trong bảng nhân công
          4. Người dụng chọn sửa máy thi công
          5. Hệ thống hiển thị form các thông tin của máy thi công được chọn
          5. Người chỉnh sửa thông tin máy thi công
          6. Người dùng chọn lưu
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống update thông tin vào cơ sở dữ liệu
          9. Hệ thống thông báo đã chỉnh sửa thành công
          - A2 - Xóa máy thi công
          <br> chuỗi A2 bắt đầu từ bước 3 của kịch bản A1
            5. Người dùng chọn xóa máy thi công
            6. Hệ thống delete máy thi công đã chọn khỏi cơ sở dữ liệu
            7. Hệ thống thông báo đã xóa thành công
        + Kịch bản lỗi
          - E1 - Dữ liệu không hợp lệ
            Chuỗi E1 bắt đầu từ bước 7 của kịch bảng thường
            6. Hệ thống thông báo dữ liệu không hợp lệ
            Trở về bước 5 của kịch bản thường
    - Cập nhật vật liệu
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật vật liệu
        + Tóm tắt: use case này cho phép người dùng thêm, chỉnh sửa hoặc xóa vật liệu trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab vật liệu
          2. Hệ thống hiển thị bảng vật liệu trong cơ sở dữ liệu
          3. Người dùng chọn thêm vật liệu
          4. Hệ thống hiển thị form yêu cầu nhập thông tin vật liệu mới
          5. Người dùng nhập thông tin vật liệu mới
          6. Người dùng chọn lưu
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống insert thông tin vào cơ sở dữ liệu
          9. Hệ thống thông báo đã lưu thành công
        + Kịch bản thay thế
          - A1 - Chỉnh sửa máy thi công
          <br> chuỗi A1 bắt đầu từ bước 2 của kịch bản thường
          3. Người dùng chọn một vật liệu cần chỉnh trong bảng nhân công
          4. Người dụng chọn sửa vật liệu
          5. Hệ thống hiển thị form các thông tin của vật liệu được chọn
          5. Người chỉnh sửa thông tin vật liệu
          6. Người dùng chọn lưu
          7. Hệ thống kiểm tra hợp lệ dữ liệu
          8. Hệ thống update thông tin vào cơ sở dữ liệu
          9. Hệ thống thông báo đã chỉnh sửa thành công
          - A2 - Xóa máy thi công
          <br> chuỗi A2 bắt đầu từ bước 3 của kịch bản A1
            5. Người dùng chọn xóa vật liệu
            6. Hệ thống delete vật liệu đã chọn khỏi cơ sở dữ liệu
            7. Hệ thống thông báo đã xóa thành công
        + Kịch bản lỗi
          - E1 - Dữ liệu không hợp lệ
            Chuỗi E1 bắt đầu từ bước 7 của kịch bảng thường
            6. Hệ thống thông báo dữ liệu không hợp lệ
            Trở về bước 5 của kịch bản thường
    - Cập nhật giá nhân công
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật giá nhân công
        + Tóm tắt: use case này cho phép người dùng cập nhật giá nhân công vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab nhân công
          2. Hệ thống hiển thị bảng nhân công trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật giá
          4. Hệ thống load các báo giá nhân công của thị trường ở các tỉnh, các định mức giá nhân công mới nhất của chính phủ.
          5. người dùng chọn cập nhật giá
          6. Hệ thống load tất cả dữ liệu vào vùng bảng giá nhân công tạm thời
          7. Người dùng chỉnh sửa
          8. Người dùng chọn lưu
          9. Hệ thống kiểm tra hợp lệ dữ liệu
          10. Hệ thống insert thông tin vào cơ sở dữ liệu
          11. Hệ thống thông báo đã lưu thành công
        + Kịch bản lỗi
          - E1 - Dữ liệu không hợp lệ
            Chuỗi E1 bắt đầu từ bước 9 của kịch bảng thường
            6. Hệ thống thông báo dữ liệu không hợp lệ
            Trở về bước 7 của kịch bản thường
    - Cập nhật giá vật liệu
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật giá vật liệu
        + Tóm tắt: use case này cho phép người dùng cập nhật giá vật liệu vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab vật liệu
          2. Hệ thống hiển thị bảng vật liệu trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật giá
          4. Hệ thống load các báo giá vật liệu của thị trường ở các tỉnh, các định mức giá vật liệu mới nhất của chính phủ.
          5. người dùng chọn cập nhật giá
          6. Hệ thống load tất cả dữ liệu vào vùng bảng giá vật liệu tạm thời
          7. Người dùng chỉnh sửa
          8. Người dùng chọn lưu
          9. Hệ thống kiểm tra hợp lệ dữ liệu
          10. Hệ thống insert thông tin vào cơ sở dữ liệu
          11. Hệ thống thông báo đã lưu thành công
        + Kịch bản lỗi
          - E1 - Dữ liệu không hợp lệ
            Chuỗi E1 bắt đầu từ bước 9 của kịch bảng thường
            6. Hệ thống thông báo dữ liệu không hợp lệ
            Trở về bước 7 của kịch bản thường
    - Cập nhật giá máy thi công  
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật giá máy thi công
        + Tóm tắt: use case này cho phép người dùng cập nhật giá máy thi công vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab máy thi công
          2. Hệ thống hiển thị bảng máy công trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật giá
          4. Hệ thống load các báo giá máy thi công của thị trường ở các tỉnh, các định mức giá nhân công mới nhất của chính phủ.
          5. người dùng chọn cập nhật giá
          6. Hệ thống load tất cả dữ liệu vào vùng bảng giá máy thi công tạm thời
          7. Người dùng chỉnh sửa
          8. Người dùng chọn lưu
          9. Hệ thống kiểm tra hợp lệ dữ liệu
          10. Hệ thống insert thông tin vào cơ sở dữ liệu
          11. Hệ thống thông báo đã lưu thành công
        + Kịch bản lỗi
          - E1 - Dữ liệu không hợp lệ
            Chuỗi E1 bắt đầu từ bước 9 của kịch bảng thường
            6. Hệ thống thông báo dữ liệu không hợp lệ
            Trở về bước 7 của kịch bản thường
    - Cập nhật hệ số các chi phí trực tiếp khác
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật hệ số chi phí trực tiếp khác
        + Tóm tắt: use case này cho phép người dùng cập nhật hệ số chi phí trực tiếp khác vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab hệ số chi phí trực tiếp trong  menu hệ số chi phí
          2. Hệ thống hiển thị bảng các hệ số chi phí trực tiếp khác trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật hệ số
          4. Hệ thống load hệ số của chi phí trực tiếp khác mới nhất của chính phủ.
          5. Người dùng chọn cập nhật hệ số
          6. Hệ thống load tất cả dữ liệu vào vùng bảng hệ số tạm thời
          7. Người dùng chọn hệ số
          8. Người dùng chọn lưu
          9. Hệ thống insert thông tin vào cơ sở dữ liệu
          10. Hệ thống thông báo đã lưu thành công
    - Cập nhật hệ số chi phí chung
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật hệ số chi phí chung
        + Tóm tắt: use case này cho phép người dùng cập nhật hệ số chi phí chung vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab hệ số chi phí chung trong  menu hệ số chi phí
          2. Hệ thống hiển thị bảng các hệ số chi phí chung trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật hệ số
          4. Hệ thống load hệ số của chi phí chung mới nhất của chính phủ.
          5. Người dùng chọn cập nhật hệ số
          6. Hệ thống load tất cả dữ liệu vào vùng bảng hệ số tạm thời
          7. Người dùng chọn hệ số
          8. Người dùng chọn lưu
          9. Hệ thống insert thông tin vào cơ sở dữ liệu
          10. Hệ thống thông báo đã lưu thành công
    - Cập nhật hệ số chi phí thu nhập chịu thuế tính trước
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật hệ số chi phí thu nhập chịu thuế tính trước
        + Tóm tắt: use case này cho phép người dùng cập nhật hệ số chi phí thu nhập chịu thuế tính trước vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab hệ số chi phí thu nhập chịu thuế tính trước trong  menu hệ số chi phí
          2. Hệ thống hiển thị bảng các hệ số chi phí thu nhập chịu thuế tính trước trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật hệ số
          4. Hệ thống load hệ số của chi phí thu nhập chịu thuế tính trước mới nhất của chính phủ.
          5. Người dùng chọn cập nhật hệ số
          6. Hệ thống load tất cả dữ liệu vào vùng bảng hệ số tạm thời
          7. Người dùng chọn hệ số
          8. Người dùng chọn lưu
          9. Hệ thống insert thông tin vào cơ sở dữ liệu
          10. Hệ thống thông báo đã lưu thành công
    - Cập nhật hệ số chi phí thuế VAT
      * Tóm tắt định danh
        + Tiêu đề: Cập nhật hệ số chi phí thuế VAT
        + Tóm tắt: use case này cho phép người dùng cập nhật hệ số chi phí thuế VAT vào trong cơ sở dữ liệu.
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dùng chọn tab hệ số chi phí tthuế VAT trong  menu hệ số chi phí
          2. Hệ thống hiển thị bảng các hệ số chi phí thuế VAT trong cơ sở dữ liệu
          3. Người dùng chọn cập nhật hệ số
          4. Hệ thống load hệ số của chi phí thuế VAT mới nhất của chính phủ.
          5. Người dùng chọn cập nhật hệ số
          6. Hệ thống load tất cả dữ liệu vào vùng bảng hệ số tạm thời
          7. Người dùng chọn hệ số
          8. Người dùng chọn lưu
          9. Hệ thống insert thông tin vào cơ sở dữ liệu
          10. Hệ thống thông báo đã lưu thành công
    - Tính tổng chi phí công trình
      * Tóm tắt định danh
        + Tiêu đề: Tính tổng chi phí công trình
        + Tóm tắt: use case này cho phép người dùng tính được tổng chi phí của công trình
        + Actor: Nhà thầu hoặc người được giao nhiệm vụ lập dự toán
        + Ngày tạo :20/4/2019
        + Ngày cập nhật :12/05/2019
        + Version :1.0
        + Chịu trách nhiệm: Võ Thanh Hiền
      * Mô tả scenario
        + Điều kiện tiên quyết
          - Hệ thống đang trong trạng thái đã đăng nhập thành công
        + Kịch bản thường
          1. Người dụng chọn công trình mới.
          2. Hệ thống hiển thị bảng bảng tiên lượng của công trình đó.
          3. Người dùng chọn các công việc cần thực hiện trong công trình
          4. Hệ thống tự động bốc tách vật liệu, nhân công, Máy thi công từ công việc
          5. Người dùng nhập khối lượng ước tính cho từng công việc
          6. Người dùng chọn lưu lại
          7. Hệ thống tự động tạo bảng đơn giá chi tiết và đơn giá chung và tổng đơn giá.
          8. Người dùng chọn lưu lại
          7. Hệ thống thông báo đã lưu lại

## Chọn 1 chức năng xây dựng mô hình tuần tự và tương tác
  Tính tổng chi phí công trình


## Xây dựng mô hình lớp thực thể

## Xây dựng mô hình cài đặt
