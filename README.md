# ReportGit_ChinhHanh
This is my ReportGit

2. Các lệnh cơ bản của git
 + Để khởi tạo Git trong một repository (repo), bạn chỉ cần gõ câu lệnh sau. Nếu bạn không khởi tạo Git, bạn không thể sử dụng bất kì các câu lệnh Git nào cả.
    Cú pháp : git init


 + Sao chép (clone) một repository
   - Để clone 1 repository có sẵn ở trên máy cục bộ, bạn hãy sử dụng dòng lệnh sau:
      Cú pháp : git clone /đường-dẫn-đến/repository/

   - Nếu repository đó ở máy chủ khác thì bạn hãy gõ dòng lệnh sau:
      Cú pháp : git clone tênusername@địachỉmáychủ:/đường-dẫn-đến/repository


  + Trên máy local, kho mã nguồn của bạn sẽ chứa 3 cây “trees” được quản lý bởi git.1)thứ nhất chính là thư mục làm việc của bạn Working Directory, mà chứa các file bạn làm việc. 2) thứ 2 là bộ chỉ mục Index mà nó chứa các giai đoạn phát triển các phiên bản và 3) cuối cùng là Head trỏ đến phiên bản mà bạn đánh dấu lần cuối cùng.
       
    ![gitadd](https://user-images.githubusercontent.com/35051952/34571463-35d5ff14-f1a1-11e7-97cf-3b45a2236460.PNG)

     Để đánh dấu thay đổi và đưa mã nguồn vào bộ Index, sử dụng:
       Cú pháp: git add <tên-tập-tin>
     hoặc
       Cú pháp : git add *

   - Để thật sự commit những thay đổi, bạn sử dụng:
     Cú pháp: git commit -m "Ghi chú Commit"
 Cú pháp: git commit -m "Ghi chú Commit"
  
  + Thay đổi của bạn hiện đang nằm tại HEAD của bản sao cục bộ đang làm việc. Để gửi những thay đổi đó đến repository remote, bạn thực thi
      Cú pháp : git push origin master
    Thay đổi master bằng bất cứ nhánh nào mà bạn muốn đầy những thay đổi đến.
    Nếu bạn chưa clone một repository hiện có và muốn kết nối repository của bạn đến máy chủ remote, bạn phải thêm nó với
     Cú pháp: git remote add origin <máy-chủ>
    Bây giờ bạn đã có thể đẩy các thay đổi của mình vào máy chủ đã chọn
  + Các nhánh (branches) được dùng để phát triển tính năng tách riêng ra từ những nhánh khác. Nhánh master là nhánh "mặc định" khi bạn tạo một repository. Sử dụng các nhánh khác tri đang trong giai đoạn phát triển và merge trở lại nhánh master một khi đã hoàn tất.
  
 ![branch](https://user-images.githubusercontent.com/35051952/34571447-2f5927c4-f1a1-11e7-8e75-95de0c336da7.PNG)

    - Tạo một nhánh mới và đặt tên là "dev" và chuyển qua nhánh đó (từ master) bằng cách 
     Cú pháp: git checkout -b dev
    - Trở lại nhánh master
     Cú pháp: git checkout master
    - Và xóa nhánh dev đó lần nửa
     Cú pháp: git branch -d dev
    - Một nhánh không có giá trị với các nhánh khác trừ khi bạn đẩy nhánh đó đến remote repository
     Cú pháp: git push origin <nhánh>
  + Cập nhật và trộn (update & merge)
    - Để cập nhật repository cục bộ của bạn và commit mới nhất, thực thi
       Cú pháp: git pull
      trong thự mục đang làm việc để lấy về (fetch) và trộn (merge) các thay đổi ở remote.
    - Để trộn một nhánh khác vào nhánh đang hoạt động (vd: master), sử dụng
       Cú pháp: git merge <nhánh>
    - Trong cả hai trường hợp, git cố gắng trộn tự động (auto-merge) các thay đổi. Không may, điều này không phải lúc nào cũng làm được và thường dẫn đến xung đột. Trách nhiệm của bạn là trộn các xung đột đó thủ công bằng cách chỉnh sửa các tập tin được hiển thị bởi git. Sau khi thay đổi, bạn phải đánh dấu chúng là đã được trộn (merged) với lệnh
       Cú pháp: git add <tên-tập-tin>
    - Trước khi trộn các thay đổi, bạn có thể xem trước chúng bằng cách
       Cú pháp: git diff <nhánh_nguồn> <nhánh_mục_tiêu>
  + Thay thế các thay đổi cục bộ 
    - Trong trường hợp bạn làm sai điều gì đó, bạn có thể thay thế các thay đổi cục bộ bằng lệnh 
       Cú pháp: git checkout -- <tên-tập-tin>
      Lệnh này thay thế những thay đổi trong "tree" đang làm việc với nội dung mới nhất của HEAD. Các thay đổi đã được thêm vào chỉ mục, kể cả các tập tin mới, điều này sẽ được giữ lại.
4. Cách sử dụng Sourcetree
 + Có nhiều công cụ để làm trung gian vận chuyển source code giữa các thành viên trong Team. Một công cụ có hiệu quả cao trong đó phải nói đến là Source Tree.
  - Đầu tiên, bạn cần tải phần mềm Source Tree về cài đặt và đăng nhập vào để có thể sử dụng. Dưới đây là giao diện chính của Source Tree.

   ![sc1](https://user-images.githubusercontent.com/35051952/34571489-45ce0ac4-f1a1-11e7-9173-66357fd27280.PNG)

 + Kéo dự án về ( Clone project )
  – Bạn click vào Clone/new tab sẽ hiện ra
 
  ![sc2](https://user-images.githubusercontent.com/35051952/34571473-3b447264-f1a1-11e7-9ff3-c952e3129420.PNG)

  - Một cách khác chỉ cần copy đường dẫn rồi paste vào Source Url sẽ tự sinh ở destination path, nếu để tự sinh thì nó sẽ được lưu vào thư mục mặc định nên bạn cần thay đổi lại đường dẫn Destination Path trỏ vào một thư mục rỗng( bạn phải chắc chắn thư mục đó là rỗng ). Sau đó click vào clone lúc này thư mục cho dự án đã được kéo về máy tính cá nhân của bạn.
    
   ![sc3](https://user-images.githubusercontent.com/35051952/34571492-47df1a6a-f1a1-11e7-855a-a30a4c794a47.PNG)

   Giao diện chương trình sau khi lấy code về

   ![sc4](https://user-images.githubusercontent.com/35051952/34571502-4a3b6430-f1a1-11e7-89f4-a9f85e64e798.PNG)

 + Đẩy code lên( push code )
    Đây là việc cần thiết khi có sự thay đổi trong source code, trước khi push được bắt buộc phải click vào push trên toolbar của source tree. Việc làm này phải được thực hiện thường xuyên khi có sự thay đổi về code để người quản lý có thể quản lý được công việc cũng như là các thành viên khác có thể nắm bắt được sự thay đổi.
  
 ![sc5](https://user-images.githubusercontent.com/35051952/34571512-4f2de72e-f1a1-11e7-995f-5e8637a01307.PNG)

 + Kéo code về( pull code )
    Cũng giống như Push code lên tuy nhiên việc bây giờ chỉ là lấy code về bao gồm những thay đổi mà thành viên khác đã push lên. Bạn chỉ cần click vào Pull ở trên toolbar của source tree
  
 ![sc6](https://user-images.githubusercontent.com/35051952/34571530-593e3156-f1a1-11e7-8065-3d48c8c3a980.PNG)
