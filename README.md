# ReportGit_ChinhHanh


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
- Repository (kho chứa) nghĩa là nơi mà bạn sẽ lưu trữ mã nguồn và một người khác có thể sao chép (clone) lại mã nguồn đó nhằm làm việc. Repository có hai loại là Local Repository (Kho chứa trên máy cá nhân) và Remote Repository (Kho chứa trên một máy chủ từ xa).
- Cách tạo reppository trên github:
  + Trước tiên bạn cần đăng nhập vào Github, sau đó ấn vào dấu + trên menu và chọn New repository.
    ![image](https://user-images.githubusercontent.com/35052781/34603518-d466a152-f236-11e7-89dd-72765fa7516c.png)
  + Bạn sẽ cần đặt tên cho kho chứa của bạn. Bạn có thể chọn loại kho chứa là Public (ai cũng có thể clone) và Private (chỉ có những người được cấp quyền mới có thể clone).
     ![image 1](https://user-images.githubusercontent.com/35052781/34603539-e7cee402-f236-11e7-9242-25491b955f63.png)
  + Khi tạo xong nó sẽ dẫn bạn tới trang hướng dẫn làm việc với kho chứa vừa tạo. Và kho chứa của bạn bây giờ sẽ có địa chỉ là https://github.com/$user-name/$repository, ví dụ https://github.com/PhamHanh96/Hanh.git
  + Việc của bạn bây giờ là hãy clone cái kho chứa này về máy của mình bằng lệnh git clone địa_chỉ
		vd: git clone https://github.com/PhamHanh96/Hanh.git
