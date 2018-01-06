# ReportGit_ChinhHanh


# 2. Các lệnh cơ bản của git

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
 # 4. Cách sử dụng Sourcetree
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


 # 7. Cách phân nhánh hiệu quả trong git


   Thông thường khi tạo 1 git repo bất kỳ đã có 1 nhánh (branch) mặc định là master, với các bạn thiếu kinh nghiệm thì dù team có bao nhiêu người cũng đều làm việc chung ở 1 branch này và commit conflict loạn cả lên. Hoặc tốt hơn 1 chút là phân ra các nhánh khác nhau cho từng bạn nhưng không có 1 convention hoặc model nào cụ thể cho việc merge các thay đổi giữa các branch lại với nhau. Các tập tin trong thư mục của bạn dễ dàng biến đổi từ phiên bản này sang phiên bản khác. Sự chuyển đổi này có thể làm nhiều hơn việc di chuyển trong trong lịch sử một các đơn thuần. Các tập tin của bạn có thể chuyển hình thái từ bản phát hành cuối thành phiên bản thử nghiệm, thành phiên bản phát triển hiện nay, thành phiên bản của người bạn của bạn, và cứ như thế.Liệt kê tất cả các nhánh bằng cách gõ:

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



 # 8. Giới thiệu cách sử dụng gitthub
  Repository (kho chứa) nghĩa là nơi mà bạn sẽ lưu trữ mã nguồn và một người khác có thể sao chép (clone) lại mã nguồn đó nhằm làm việc.
   + Tạo repository trên gitthub
    - Trước tiên bạn cần đăng nhập vào Github, sau đó ấn vào dấu + trên menu và chọn New repository.

       ![rep1](https://user-images.githubusercontent.com/35051952/34597614-6078d632-f21a-11e7-8cda-f8f3fc78598e.PNG)

     - Bạn sẽ cần đặt tên cho kho chứa của bạn. Bạn có thể chọn loại kho chứa là Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
     
        ![rep2](https://user-images.githubusercontent.com/35051952/34597683-d695b92a-f21a-11e7-8bbc-b0f83e81fd8e.PNG)
 
     - Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với kho chứa vừa tạo. Và kho chứa của bạn bây giờ sẽ có địa chỉ là https://github.com/$user-name/$repository, ví dụ https://github.com/demogitthub/hoc-git.Và đây là trang chủ khi bạn tạo xong repository xong
     
        ![rep3](https://user-images.githubusercontent.com/35051952/34601241-a41fb33e-f22d-11e7-97d5-1f60afbf7db4.PNG)

     - Việc của bạn bây giờ là hãy clone cái kho chứa này về máy của mình bằng lệnh git clone địa_chỉ.
    + Tạo team
    Để tạo một nhóm cho nhiều người cùng làm việc ta làm như sau:
      -Truy cập URL: https://github.com/settings/organizations, chọn New Organizations
      -Đặt tên và email cho tổ chức
       
        ![rep4](https://user-images.githubusercontent.com/35051952/34601190-6e8205ec-f22d-11e7-9a45-a57faa232144.PNG)
   
    Tại mục Choose the organization’s plan chọn Open Source để miễn phí, nhưng lúc này các Repo trong tổ chức sẽ là public.
     Mời các thành viên cho tổ chức

		![rep5](https://user-images.githubusercontent.com/35051952/34601340-1a67a510-f22e-11e7-80e9-d96bb03712ad.PNG)
    Lúc này vào trang cá nhân của bạn sẽ thấy tại mục Organizations có tổ chức mới vừa tạo. Để cấu hình tổ chức này ta click thẳng vào nó.

     Ở đây tôi sẽ tạo một team mới như hình sau:
        ![rep6](https://user-images.githubusercontent.com/35051952/34601518-ea95cb5e-f22e-11e7-885d-619a18a30882.PNG)

    Để mời một người dùng khác vào team, ta click vào team đó và search tên của người dùng cần tìm

     ![rep7](https://user-images.githubusercontent.com/35051952/34601568-22750012-f22f-11e7-963a-5820e32275d3.PNG)
   Sau đó hệ thống sẽ yêu cầu bạn nhập password để xác thực, nếu thành công, một email xác nhận sẽ được gửi đến người được mời và người này sẽ xác nhận có tham gia vào tổ chức hay không


  + Tạo pull request
    Thông thường khi làm với Git mỗi lập trình viên sẽ tạo một branch mới khác với master để phát triển một tính năng mới. Giả sử nhánh mà lập trình viên tạo ra để phát triển tính năng có tên là dev. Trong trường hợp này sau khi đẩy commit trên nhánh này trên nhánh tương ứng dev ở kho chứa từ xa origin thì để các lập trình viên khác có thể kéo về được commit này thì quản trị viên trên máy chủ từ xa cần thực hiện việc gộp commit ở nhánh dev về nhánh master.
    Pull request là một yêu cầu gửi tới quản trị viên kho chứa từ xa gộp commit mới được tạo ra từ nhanh dev về nhánh master để các lập trình viên khác có thể pull về được.
      
     ![rep8](https://user-images.githubusercontent.com/35051952/34602882-22e641be-f234-11e7-8267-dd35978043bb.PNG)
    
    - Sau đó, ta click vào new pull request
      
      ![rep9](https://user-images.githubusercontent.com/35051952/34602948-70a4fb20-f234-11e7-92a0-8d50ba5e7944.PNG)
    - Nhập tiêu đề và mô tả cho full request

     ![rep11](https://user-images.githubusercontent.com/35051952/34603162-57559566-f235-11e7-9847-e9bf43965103.PNG)

     Cuối cùng ta click vào create pull request.

## 1. Sơ đồ tổng quan về hệ thống Git.

### Git là gì?

- Git là tên gọi của một Hệ thống quản lý phiên bản phân tán (Distributed Version Control System – DVCS) là một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay.
	![2color-lightbg 2x](https://user-images.githubusercontent.com/35052781/34601454-a8078070-f22e-11e7-98a9-346ff0ee4a30.png)

- DVCS nghĩa là hệ thống giúp mỗi máy tính có thể lưu trữ nhiều phiên bản khác nhau của một mã nguồn được nhân bản (clone) từ một kho chứa mã nguồn (repository), mỗi thay đổi vào mã nguồn trên máy tính sẽ có thể ủy thác (commit) rồi đưa lên máy chủ nơi đặt kho chứa chính. Và một máy tính khác (nếu họ có quyền truy cập) cũng có thể clone lại mã nguồn từ kho chứa hoặc clone lại một tập hợp các thay đổi mới nhất trên máy tính kia. Trong Git, thư mục làm việc trên máy tính gọi là Working Tree.
 	![1](https://user-images.githubusercontent.com/35052781/34603186-78fc3b70-f235-11e7-8fa1-bfffae6e95e9.jpg)

### Tại sao nên sử dụng Git?
  Có rất nhiều lợi thế để bạn nên sử dụng Git trong việc lập trình ngay từ hôm nay, bất kể là lập trình cái gì đi chăng nữa.
  + Git dễ sử dụng, an toàn và nhanh chóng.
  + Có thể giúp quy trình làm việc code theo nhóm đơn giản hơn rất nhiều bằng việc kết hợp các phân nhánh (branch).
  + Bạn có thể làm việc ở bất cứ đâu vì chỉ cần clone mã nguồn từ kho chứa hoặc clone một phiên bản thay đổi nào đó từ kho chứa, hoặc một nhánh nào đó từ kho chứa.
  + Dễ dàng trong việc deployment sản phẩm.
  
### Kho Repo (Repository)
  Repository hay được gọi tắt là Repo, đơn giản là nơi chứa tất cả những thông tin cần thiết để duy trì và quản lý các sửa đổi và lịch sử của toàn bộ project. Trong Repo có 2 cấu trúc dữ liệu chính là Object Store và Index. Tất cả dữ liệu của Repo đều được chứa trong thư mục bạn đang làm việc dưới dạng folder ẩn có tên là .git
  	![](https://4.bp.blogspot.com/-fC2tMlgfHXo/VTvNssnSP1I/AAAAAAAACWI/C6nTDooFOiE/s1600/git-repo.png)
	
### Remote repository và local repository
  - Repository của Git được phân thành 2 loại là remote repository và local repository.
    + Remote repository: Là repository để chia sẻ giữa nhiều người và bố trí trên server chuyên dụng.
    + Local repository: Là repository bố trí trên máy của bản thân mình, dành cho một người dùng sử dụng.
  - Do repository phân thành 2 loại là local và remote nên với những công việc bình thường thì có thể sử dụng local repository. Khi muốn public nội dung công việc mà mình đã làm trên local repository, thì ta sẽ upload lên remote repository rồi public. Thêm nữa, thông qua remote repository bạn cũng có thể lấy về nội dung thay đổi của người khác.
	![](https://2.bp.blogspot.com/-aBPG-ztqfk0/VTvHH59jZkI/AAAAAAAACVc/eXqR_iG3oys/s1600/basic-remote-workflow.png)
	
### Nhánh (Branch)
![](https://github.com/nghuuquyen/sociss-class-nodejs/blob/master/src/git-tutorials/images/feature-branch.png)
  - Đây là một trong những thế mạnh của git là nhánh. Với git, việc quản lý nhánh rất dễ dàng. Mỗi nhánh trong Git gần giống như một workspace. Việc nhảy vào một nhánh để làm việc trong đó tương tự việc chuyển qua ngữ cảnh làm việc mới, và sau đó có thể nhanh chóng quay lại ngữ cảnh cũ.
  - Nhánh (branch) được dùng để phát triển tính năng mới mà không làm ảnh hưởng đến code hiện tại.
  - Nhánh master là nhánh “mặc định” khi bạn tạo một repository và thông thường là nhánh chính của ứng dụng. Ví dụ khi bạn thay đổi hay tạo mới 1 file nào đó mà bạn chưa chắc chắn, bạn có thể tạo 1 nhánh mới và đưa dữ liệu lên đó, sau khi hoàn thành mới gộp dữ liệu vô nhánh master. Việc hợp nhất dữ liệu giữa 2 nhánh gọi là merge.
  
### Merge (Trộn)
  - Trộn source từ 1 nhánh khác vào nhánh hiện tại gọi là Merge.
  - Các lưu ý khi Merge: 
    + Phải kiểm tra branch trước khi merge.
    + Phải đẩy tất cả những thay đổi trên local lên Git trước khi Merge.
    + Trước khi merge phải lấy tất cả các dữ liệu mới nhất từ các branch khác về, hoặc ít nhất là từ branch cần merge.
    + Sau khi merge thành công thì nên đẩy(push) tất cả source lên server.
    
### Xung đột (Conflict)
  - Conflic là trường hợp có 2 sự thay đổi trong một dòng code và máy tính không thể tự quyết định dòng code nào là “đúng”, dòng code nào là "sai".
  - Để giải quyết mâu thuẫn bạn phải dùng “tay” để sữa các xung đột này. Bạn chỉ việc nhìn vào file bị conflict và tự quyết định dòng code nào giữ lại, dòng nào xóa bỏ.
  
### Commit
  - Để ghi lại việc thêm/thay đổi file hay thư mục vào repository thì sẽ thực hiện thao tác gọi là Commit.
  - Khi thực hiện commit, trong repository sẽ tạo ra commit (hoặc revision) đã ghi lại sự khác biệt từ trạng thái đã commit lần trước với trạng thái hiện tại.
  - Commit này đang được chứa tại repository, các commit nối tiếp với nhau theo thứ tự thời gian. Bằng việc lần theo commit này từ trạng thái mới nhất thì có thể biết được lịch sử thay đổi trong quá khứ hoặc nội dung thay đổi đó.
  	![](https://2.bp.blogspot.com/-KTRRq2Oh5m0/WGxiwltKbFI/AAAAAAAAAOU/WCl8JFMpyIAThv4BHZJYlAvWzlRwDdPHQCLcB/s1600/capture_intro1_3_1.png)
  - Mỗi commit đều có yêu cầu phải có commit message, để giải thích commit này là bạn đã làm gì trong này.
  
### Git Remote
  - Để kết nối được với một repo khác người ta sử dụng một khái niệm gọi là remote.
  - Trên thực tế khi làm việc với nhau thì không như vậy, vì không phải máy ai cũng cài một “git server” để người khác kết nối được với mình. Thông thường thì chúng ta sẽ sử dụng một repo chung và các máy kết nối vào repo đó.
  - Có 2 “git repo server” được sử dụng nhiều là github.com và bitbucket.org.
  - Trên thực tế khi có 2 người cùng làm việc với 1 project thì thông thường sẽ tạo một repo trên github hoặc gitlab hoặc bitbucket và repo trên máy người A sẽ kết nối với repo trên github/gitlab/bitbucket và máy người B cũng kết nối với repo trên github/bitbucket. Từ đó source code của người A và người B sẽ được đồng bộ với nhau thông qua repo trên github/gitlab/bitbucket.
  - Vì vậy, trước khi sử dụng git thì bạn nên đăng kí một tài khoản trên github.com hoặc bitbucket.org.
  
### Working tree và Index (hoặc staging area)
![](https://github.com/nghuuquyen/sociss-class-nodejs/blob/master/src/git-tutorials/images/git-staging-area.png)
  - Trên Git, những thư mục được đặt trong sự quản lý của Git, để mọi người thực hiện công việc trên đó, được gọi là working tree.
  - Giữa repository và working tree tồn tại một nơi gọi là index hay staging area . staging area là nơi để chuẩn bị cho việc commit vào repository.
  
### Tracked và Untracked
  - Trong Git có hai loại trạng thái chính đó là Tracked và Untracked. Nếu bạn muốn commit một tập tin đó, bạn sẽ cần phải đưa tập tin đó vào trạng thái tracked bằng lệnh git add.
    + Tracked – Là tập tin đã được đánh dấu theo dõi trong Git để bạn làm việc với nó. Và trạng thái Tracked nó sẽ có thêm các trạng thái phụ khác là Unmodified (chưa chỉnh sửa gì), Modified (đã chỉnh sửa) và Staged (đã sẵn sàng để commit).
    + Untracked – Là tập tin còn lại mà bạn sẽ không muốn làm việc với nó trong Git.
  - Nhưng nếu tập tin đó đã được Tracked nhưng đang rơi vào trạng thái (Modified) thì nó vẫn sẽ không thể commit được mà bạn phải đưa nó về Staged cũng bằng lệnh git add
  - Nếu bạn tạo ra hoặc thêm vào một tập tin mới vào trong thư mục làm việc của bạn thì nó sẽ ở trạng thái Untracked. muốn cho nó trở thành tracked thì phải dùng lệnh git add. Nếu tệp tin đó mới hoàn toàn thì nó sẽ rơi vào trạng thái staged và bạn có thể commit file đó.
  - Một khi một tập tin đã được đưa về Tracked thì nó sẽ có thể thay đổi giữa 3 trạng thái khác nhau là Modified, Unmodified và Staged.
    + Unmodified : File đươc Git quản lý nhưng không có thay đổi gì
    + Modified :File được Git quản lý nhưng đang bị thay đổi, cần dùng lệnh git add để đưa về trạng thái staged
    + staged : File được git quản lý và sẵn sàng cho việc commit.
Chú ý : Một file đã ở trạng thái Staged mà bạn lại tiếp tục sửa thì nó sẽ quay về trạng thái modified, lúc này lại cần git add để xác nhận thay đổi, và đưa file quay về trạng thái staged.

  
## 3. Cách sử dụng .gitignore
  - .gitignore Là một file cấu hình của git. Tại khai báo tất cả các file hoặc thư mục mà ta sẽ untracked. Tức là khai báo những file mà ta không muốn git quản lý, những file này sẽ không bao giờ được commit.
  - Ứng dụng của file này là để loại bỏ các tệp tin thừa do hệ điều hành, công cụ làm việc sinh ra trong lúc làm việc, những file này không có giá trị nên không bao giờ cần phải quản lý bởi Git cả.
  - Chú ý : Thường khi làm việc với một công nghệ cụ thể nào đó thì đề có một file .gitignore mẫu sẵn, ta có thể lên mạng tải về để sử dụng, trong quá trình sử dụng bạn có thể thêm vào file .gitignore các file đặc biệt mà bạn muốn bỏ ra khỏi Git tương ứng với công việc của bạn.
  - Ví dụ: Với ngôn ngữ Java, khi mã nguồn được biên dịch, thì file .class sẽ được sinh ra, nhưng file này lại không cần phải quản lý bởi Git do nó sinh ra từ file .java. Nên ta sẽ loại bỏ nó bằng cách khai báo trong .gitignore là *.class (bỏ hoàn toàn các file có phần mở rộng là .class).
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

## 5. Cách tạo repository và cách viết file readme.md trên github

### I. Repository(kho chứa - Repo)
- Repository (kho chứa) nghĩa là nơi mà bạn sẽ lưu trữ mã nguồn và một người khác có thể sao chép (clone) lại mã nguồn đó nhằm làm việc. Repository có hai loại là Local Repository (Kho chứa trên máy cá nhân) và Remote Repository (Kho chứa trên một máy chủ từ xa).
- Cách tạo reppository trên github:
  + Trước tiên bạn cần đăng nhập vào Github, sau đó ấn vào dấu + trên menu và chọn New repository.
    ![image](https://user-images.githubusercontent.com/35052781/34603518-d466a152-f236-11e7-89dd-72765fa7516c.png)
  + Bạn sẽ cần đặt tên cho kho chứa của bạn. Bạn có thể chọn loại kho chứa là Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
     ![image 1](https://user-images.githubusercontent.com/35052781/34603539-e7cee402-f236-11e7-9242-25491b955f63.png)
  + Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với kho chứa vừa tạo. Và kho chứa của bạn bây giờ sẽ có địa chỉ là https://github.com/$user-name/$repository, ví dụ https://github.com/PhamHanh96/Hanh.git
  + Việc của bạn bây giờ là hãy clone cái kho chứa này về máy của mình bằng lệnh git clone địa_chỉ
		vd: git clone https://github.com/PhamHanh96/Hanh.git

=======
		
### II. Cách viết file readme.md
  - Readme.md là 1 file chứa thông tin về các tệp khác trong thư mục hoặc kho lưu trữ phần mềm máy tính, cho một tập tin văn bản sử dụng markdown đánh dấu.
  - Nội dung trong file Readme.md thường chứa các nội dung như: hướng dẫn cài đặt, cấu hình, vận hành,cách khắc phục sự cố, thông tin bản quyền giấy phép, thông tin liên hệ...
  - File Readme.me được viết bằng ngôn ngữ Markdown, một ngôn ngữ đánh dấu với cú pháp văn bản thô, được thiết kế để có thể dễ dàng chuyển thành HTML và nhiều định dạng khác sử dụng một công cụ cùng tên.
#### Một số cơ bản về Markdown
   1. Thẻ tiêu đề (H)
     - Markdown sử dụng kí tự # để bắt đầu cho các thẻ tiêu đề, có thể dùng từ 1 đến 6 ký tự # liên tiếp. Mức độ riêu đề giảm dần từ 1 đến 6

     - Tùy mục đích và ý thích bạn có thể sử dụng cách này để thể hiện các chỉ mục khác nhau.

Ví dụ:

```
#1.Tiêu đề cấp 1
```

#1.Tiêu đề cấp 1

```
##2.Tiêu đề cấp 2
```

##2.Tiêu đề cấp 2

```
######6.Tiêu đề cấp 6
```

######6.Tiêu đề cấp 6

   2. Chèn Link, hình ảnh 
       - Để chèn hyperlink bạn chỉ cần paste luôn linh đó vào file .md (VD : https://github.com),<br>
         cũng có thể sử dụng cú pháp sau để thu ngắn đường dẫn của link
           VD : [Github](https://github.com) . khi đó hiện thị : Github , ta click vào "Github" nó sẽ dẫn đến link https://github.com.
       - Chèn ảnh : ![alt_text](Đường dẫn hình ảnh của bạn).
       
    3. In đậm , in nghiêng, bo chữ
       - In đậm text :
          Cú pháp :   ``` **Text cần in đậm** ```
       - In nghiêng text :
          Cú pháp :   ``` *Text cần in nghiêng* ```
       - Bo chữ:
          Cú pháp :  ``` `Đoạn cần bo` ```
            ```
       - Để làm nổi bật một đoạn, chẳng hạn như một đoạn shell hay file cấu hình bạn có thể sử dụng cú pháp như ví dụ sau:

    ```sh
    dòng 1
    ....
    dòng n
    ```

Kết quả như sau:

```sh
dòng 1
....
dòng n
```
	  
     4. Tạo bảng :
      ví dụ :
      cú pháp : 
```
| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |
```
     Kết quả:

| Cột 1 Hàng 1 | Cột 2 | Cột 3| Cột 4 |
|--------------|-------|------|-------|
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 | 2 x 4 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 | 3 x 4 |
| Hàng 4 | 4 x 1 | 4 x 2 | 4 x 3 | 4 x 4 |
  
<<<<<<< HEAD
<<<<<<< HEAD
## 9. Giới thiệu về cách sử dụng GitLab 

### Tạo Project
  - Trước tiên bạn cần đăng nhập vào Gitlab, sau đó ấn vào dấu + trên menu và chọn New Projecgt.
  ![image 2](https://user-images.githubusercontent.com/35052781/34641179-a454b2fe-f332-11e7-974d-07e09aa1bafa.png)
  
  - Bạn sẽ cần đặt tên cho project của bạn.
  ![image 3](https://user-images.githubusercontent.com/35052781/34641189-d8ebec08-f332-11e7-853e-1cfb739e6549.png)
  
  - Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với project vừa tạo. Ví dụ https://gitlab.com/hanhhana041096/HanhTest.git
  + Việc của bạn bây giờ là hãy clone cái kho chứa này về máy của mình bằng lệnh git clone địa_chỉ
		vd: git clone git clone https://gitlab.com/hanhhana041096/HanhTest.git

### Tạo Group
  - Trước tiên bạn cần đăng nhập vào Gitlab, sau đó ấn vào dấu + trên menu và chọn New Group.
![image 6](https://user-images.githubusercontent.com/35052781/34641251-c9a391aa-f333-11e7-8d2e-2c2b76bb865e.png)

  - Bạn cần điền tên Project, Tên Group, miêu tả Group...
  ![image 8](https://user-images.githubusercontent.com/35052781/34641272-07b74658-f334-11e7-8296-2e5d363b9f61.png)
  
  - Và cần thêm thành viên vô Group của mình.
  ![image 10](https://user-images.githubusercontent.com/35052781/34641292-539a1852-f334-11e7-98d5-e036daae43d2.png)


