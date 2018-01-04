# ReportGit_ChinhHanh
This is my ReportGit
<<<<<<< HEAD
<<<<<<< HEAD
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
=======
<<<<<<< HEAD

1. Sơ đồ tổng quan về hệ thống Git.
- Git là tên gọi của một Hệ thống quản lý phiên bản phân tán (Distributed Version Control System – DVCS) là một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay.
- DVCS nghĩa là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (clone) từ một kho chứa mã nguồn (repository), mỗi thay đổi vào mã nguồn trên máy tính sẽ có thể ủy thác (commit) rồi đưa lên máy chủ nơi đặt kho chứa chính. Và một máy tính khác (nếu họ có quyền truy cập) cũng có thể clone lại mã nguồn từ kho chứa hoặc clone lại một tập hợp các thay đổi mới nhất trên máy tính kia. Trong Git, thư mục làm việc trên máy tính gọi là Working Tree.
			![1](https://user-images.githubusercontent.com/35052781/34572684-9790d528-f1a4-11e7-929e-5f47d4d64f05.jpg)
>>>>>>> 2f06f164d02db6823db70336dfdde8c1825eea7c

- Tại sao nên sử dụng Git?
  Có rất nhiều lợi thế để bạn nên sử dụng Git trong việc lập trình ngay từ hôm nay, bất kể là lập trình cái gì đi chăng nữa.
  + Git dễ sử dụng, an toàn và nhanh chóng.
  + Có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều bằng việc kết hợp các phân nhánh (branch).
  + Bạn có thể làm việc ở bất cứ đâu vì chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa.
  + Dễ dàng trong việc deployment sản phẩm.
<<<<<<< HEAD


3. Cách sử dụng .gitignore
>>>>>>> 2f06f164d02db6823db70336dfdde8c1825eea7c
- Gitignore là gì?
  Gitignore là file có tên là .gitignore do thằng Git quy định, nhiệm vụ của nó là liệt kê những file mà mình không mong muốn cho vào git hoặc hiểm nôm na là thằng Git sẽ lờ những file đó đi.
- Cách thức hoạt động: Khi add 1 file mới vào git, git sẽ kiểm tra danh sách những thằng sẽ lờ đi trong file .gitignore và lờ luôn chúng nó. Đó mới chỉ là điều kiện cần, điều kiện đủ là nó không có trong git cache nữa thì thằng git nó mới lờ đi chứ nó mà nằm trong git cache thì .gitignore sẽ vô tác dụng.
- Git thấy mọi tệp trong bản sao làm việc của bạn là một trong ba điều sau:
  + Theo dõi - một tập tin đã được dàn dựng hoặc cam kết.
  + Untracked - một tập tin đã không được hiển thị hoặc cam kết. 
  + Bị bỏ qua - một tệp tin mà Git đã được nói rõ ràng để bỏ qua.
- Các tệp bị bỏ qua thường tạo các hiện vật và các tệp được máy tạo ra có thể được lấy từ nguồn lưu trữ của bạn hoặc nếu không được cam kết. Một số ví dụ phổ biến là:
  + Cache phụ thuộc, chẳng hạn như nội dung của /node_moduleshay/packages
  + Biên dịch mã, chẳng hạn như .o, .pycvà .classfile
  + Xây dựng thư mục đầu ra, chẳng hạn như /bin, /outhoặc/target
  + Tập tin được tạo trong thời gian chạy, chẳng hạn như .log, .lockhoặc.tmp
  + Tập tin hệ thống ẩn, chẳng hạn như .DS_StorehayThumbs.db
  + Tệp cấu hình IDE cá nhân, chẳng hạn như .idea/workspace.xml
- Các tệp bị bỏ qua được theo dõi trong một tệp đặc biệt có tên .gitignoređược kiểm tra tại thư mục gốc của kho lưu trữ của bạn. Không có lệnh git ignore rõ ràng: thay vào đó .gitignoretệp tin phải được chỉnh sửa và cam kết bằng tay khi bạn có các tệp mới mà bạn muốn bỏ qua. .gitignoretệp chứa các mẫu được so khớp với tên tập tin trong kho của bạn để xác định có nên bỏ qua các tệp này hay không.
<<<<<<< HEAD

=======
>>>>>>> 2f06f164d02db6823db70336dfdde8c1825eea7c
5. Cách tạo repository và cách viết file readme.md trên github
- Repository (kho chứa) nghĩa là nơi mà bạn sẽ lưu trữ mã nguồn và một người khác có thể sao chép (clone) lại mã nguồn đó nhằm làm việc. Repository có hai loại là Local Repository (Kho chứa trên máy cá nhân) và Remote Repository (Kho chứa trên một máy chủ từ xa).
- Cách tạo reppository trên github:
  + Trước tiên bạn cần đăng nhập vào Github, sau đó ấn vào dấu + trên menu và chọn New repository.
<<<<<<< HEAD
		![image](https://user-images.githubusercontent.com/35052781/34570289-d5202bb6-f19d-11e7-9c1f-1abc57843be8.png)

  + Bạn sẽ cần đặt tên cho kho chứa của bạn. Bạn có thể chọn loại kho chứa là Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
         	![image 1](https://user-images.githubusercontent.com/35052781/34570282-cbdc7ece-f19d-11e7-865b-9d37f3e49dec.png)

  + Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với kho chứa vừa tạo. Và kho chứa của bạn bây giờ sẽ có địa chỉ là https://github.com/$user-name/$repository, ví dụ https://github.com/PhamHanh96/Hanh.git
  + Việc của bạn bây giờ là hãy clone cái kho chứa này về máy của mình bằng lệnh git clone địa_chỉ
<<<<<<< HEAD

		vd: git clone https://github.com/PhamHanh96/Hanh.git
>>>>>>> 0cc844d2fc151a5b5beb445532a8a1c015b51305
=======
		vd: git clone https://github.com/PhamHanh96/Hanh.git
>>>>>>> Hanh
=======
>>>>>>> Chinh


7. Cách phân nhánh hiệu quả trong git


. Thông thường khi tạo 1 git repo bất kỳ đã có 1 nhánh (branch) mặc định là master, với các bạn thiếu kinh nghiệm thì dù team có bao nhiêu người cũng đều làm việc chung ở 1 branch này và commit conflict loạn cả lên. Hoặc tốt hơn 1 chút là phân ra các nhánh khác nhau cho từng bạn nhưng không có 1 convention hoặc model nào cụ thể cho việc merge các thay đổi giữa các branch lại với nhau. Các tập tin trong thư mục của bạn dễ dàng biến đổi từ phiên bản này sang phiên bản khác. Sự chuyển đổi này có thể làm nhiều hơn việc di chuyển trong trong lịch sử một các đơn thuần. Các tập tin của bạn có thể chuyển hình thái từ bản phát hành cuối thành phiên bản thử nghiệm, thành phiên bản phát triển hiện nay, thành phiên bản của người bạn của bạn, và cứ như thế.Liệt kê tất cả các nhánh bằng cách gõ:

$ git branch
Theo mặc định, bạn bắt đầu tại nhánh có tên “master”. Một số người chủ trương rời bỏ nhánh “master” mà không động chạm gì đến nó và tạo các nhánh mới dành cho các chỉnh sửa của riêng mình.

Các tùy chọn -d and -m cho phép bạn xóa hay di chuyển (đổi tên) các nhánh. Xem thêm git help branch.

Nhánh “master” thông thường rất hữu dụng. Những người khác sẽ nghĩ rằng kho chứa của bạn có nhánh mang tên này, và nhánh đó chứa phiên bản chính thức của dự án của bạn. Mặc dù bạn có thể đổi tên hay xóa bỏ nhánh “master”, nhưng bạn không nên làm như thế mà hãy tôn trọng thỏa thuận ngầm này.
Một lát sau bạn có lẽ nhận thức được rằng mình cần có các nhánh tạm thời vì các lý do như: mọi nhánh khác đơn thuần phục vụ cho việc ghi lại trạng thái hiện tại do vậy bạn có thể nhảy trở lại các trạng thái cũ hơn để mà sửa chữa các lỗi nghiêm trọng hay làm một cái gì đó.

Điều này cũng tương tự như việc chuyển kênh trên TV một cách tạm thời để thấy chương trình khác đang chiếu cái gì. Nhưng thay vì chỉ cần nhấn vài cái nút, bạn phải tạo, “checkout”, trộn và xóa nhánh tạm đó. May mắn thay, Git có cách ngắn gọn tiện lợi chẳng thua kém gì chiếc điều khiển từ xa của một chiếc TV:

$ git stash
Lệnh này ghi lại trạng thái hiện hành vào một vị trí tạm thời (một stash) và phục hồi lại trạng thái trước đó. Thư mục bạn đang làm việc xuất hiện chính xác như trước khi bạn chỉnh sửa, và bạn có thể sửa lỗi, pull về các thay đổi ngược dòng, và cứ như thế. Khi bạn muốn qua trở lại trạng thái đã được tạm giấu đi đó, hãy gõ:

$ git stash apply  # Bạn có thể sẽ phải giải quyết các xung đột có thể nảy sinh.
Bạn có thể có nhiều trạng thái được tạm giấu đi, và vận dụng chúng theo nhiều cách khác nhau. Xem git help stash để biết thêm chi tiết. Bạn cũng có thể đoán được, Git duy trì các nhánh ở hậu trường để thực hiện việc này.
<<<<<<< HEAD
=======

=======





>>>>>>> 2b08a51bfb7342faabb19ecbc68cb7beb07a14dd
